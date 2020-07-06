---
title: Använd huvudnamn för tjänsten i Azure med Azure PowerShell
description: Lär dig hur du skapar och använder huvudnamn för tjänsten med Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.openlocfilehash: ebdc0783c43ccecbbeb315de5b5baebc9539b40e
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/25/2020
ms.locfileid: "85363584"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Skapa tjänstens huvudnamn för Azure med Azure PowerShell

Automatiserade verktyg som använder Azure-tjänster bör alltid ha begränsad behörighet. Azure erbjuder tjänstens huvudnamn i stället för att programmen loggar in som användare med fullständig behörighet.

Ett huvudnamn för tjänsten i Azure är en identitet som skapas för användning med program, värdbaserade tjänster och automatiserade verktyg för att tillgång till Azure-resurser. Åtkomsten begränsas av de roller som tilldelas tjänstens huvudnamn, vilket ger dig kontroll över vilka resurser som kan nås och på vilken nivå. Av säkerhetsskäl rekommenderar vi att du alltid använder tjänstens huvudnamn med automatiserade verktyg i stället för att tillåta inloggning med en användaridentitet.

Den här artikeln visar hur du skapar, hämtar information om och återställer ett tjänsthuvudnamn med Azure PowerShell.

## <a name="create-a-service-principal"></a>Skapa ett huvudnamn för tjänsten

Skapa ett huvudnamn för tjänsten med cmdleten [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal). När du skapar ett huvudnamn för tjänsten kan du välja vilken typ av inloggningsinformation som används.

> [!NOTE]
> Om ditt konto inte har behörighet att skapa ett tjänsthuvudnamn visar `New-AzADServicePrincipal` ett felmeddelande om att du inte har rätt behörigheter för att slutföra åtgärden.
> Kontakta Azure Active Directory-administratören om du vill skapa ett huvudnamn för tjänsten.

Det finns två typer av autentisering för tjänstens huvudnamn: lösenordsbaserad autentisering och certifikatbaserad autentisering.

### <a name="password-based-authentication"></a>Lösenordsbaserad autentisering

> [!IMPORTANT]
> Standardrollen för ett huvudnamn för tjänsten för lösenordsbaserad autentisering är **Deltagare**. Den här rollen har fullständig behörighet att läsa och skriva till ett Azure-konto. Information om hur du hanterar rolltilldelningar finns i [Hantera roller för tjänstens huvudnamn](#manage-service-principal-roles).

Om inga andra autentiseringsparametrar finns används lösenordsbaserad autentisering, och ett slumpmässigt lösenord skapas åt dig. Om du vill använda lösenordsbaserad autentisering rekommenderas den här metoden.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Det returnerade objektet innehåller medlemmen `Secret`, som är en `SecureString` som innehåller det genererade lösenordet. Se till att värdet lagras på en säker plats för autentisering med tjänstens huvudnamn. Värdet visas _inte_ i konsolens utdata. Om du tappar bort lösenordet måste du [återställa autentiseringsuppgifterna för tjänstens huvudnamn](#reset-credentials).

Med följande kod kan du exportera hemligheten:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

För lösenord som anges av användaren tar argumentet `-PasswordCredential` objekten `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`. Objekten måste ha ett giltigt `StartDate` och `EndDate` samt ett `Password` i klartext. Skapa ett starkt lösenord genom att följa [regler och begränsningar för Azure Active Directory-lösenord](/azure/active-directory/active-directory-passwords-policy).
Använd inte ett svagt lösenord och återanvänd aldrig lösenord.

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn.

> [!IMPORTANT]
> För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under. För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando _omedelbart efter_ att tjänstens huvudnamn har skapats:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a>Certifikatbaserad autentisering

> [!IMPORTANT]
> Ingen standardroll tilldelas när du skapar en certifikatbaserad autentisering för tjänstens huvudnamn. Information om hur du hanterar rolltilldelningar finns i [Hantera roller för tjänstens huvudnamn](#manage-service-principal-roles).

Tjänstens huvudnamn med certifikatbaserad autentisering skapas med parametern `-CertValue`. Denna parameter tar en base64-kodad ASCII-sträng för det offentliga certifikatet. Detta representeras av en PEM-fil eller en textkodad CRT eller CER. Binär kodning av det offentliga certifikatet stöds inte. I de här anvisningarna förutsätts att du redan har ett tillgängligt certifikat.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

Du kan också använda parametern `-KeyCredential`, som tar `PSADKeyCredential`-objekt. Objekten måste ha ett giltigt `StartDate` och `EndDate`, och medlemmen `CertValue` måste ha angetts till en base64-kodad ASCII-sträng för det offentliga certifikatet.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

Objektet som returnerades från `New-AzADServicePrincipal` innehåller medlemmarna `Id` och `DisplayName`, som båda kan användas för inloggning med tjänstens huvudnamn. Klienter som loggar in med tjänstens huvudnamn måste också ha åtkomst till certifikatets privata nyckel.

> [!IMPORTANT]
> För inloggning med tjänstens huvudnamn krävs det klientorganisations-ID som tjänstens huvudnamn skapades under. För att få den klientorganisation som var aktiv när tjänstens huvudnamn skapades kör du följande kommando _omedelbart efter_ att tjänstens huvudnamn har skapats:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a>Hämta ett befintligt tjänsthuvudnamn

En lista över tjänsthuvudnamn för den aktiva klientorganisationen kan hämtas med [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal). Som standard returnerar detta kommando _alla_ huvudnamn för tjänsten i en klientorganisation. För stora organisationer kan det ta lång tid att returnera resultat. Vi rekommenderar att du i stället använder de valfria argumenten för filtrering på serversidan:

- `-DisplayNameBeginsWith` begär tjänsthuvudnamn som har ett _prefix_ som matchar det angivna värdet. Visningsnamnet för ett tjänsthuvudnamn är det värde som anges med `-DisplayName` när det skapas.
- `-DisplayName` begär en _exakt matchning_ av tjänstens huvudnamn.

## <a name="manage-service-principal-roles"></a>Hantera roller för tjänstens huvudnamn

Azure PowerShell har följande cmdletar för hantering av rolltilldelningar:

- [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
- [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
- [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Standardrollen för ett huvudnamn för tjänsten för lösenordsbaserad autentisering är **Deltagare**. Den här rollen har fullständig behörighet att läsa och skriva till ett Azure-konto. Rollen **Läsare** är mer begränsad och ger endast läsåtkomst. Mer information om rollbaserad åtkomstkontroll (RBAC) och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).

Det här exemplet lägger till rollen **Läsare** och tar bort rollen **Deltagare**:

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> Cmdletar för rolltilldelning tar inte tjänsthuvudnamnsobjektets ID. De tar ID för det associerade programmet, som genereras vid tidpunkten för skapandet. Om du vill hämta program-ID:t för ett tjänsthuvudnamn använder du `Get-AzADServicePrincipal`.

> [!NOTE]
> Om ditt konto inte har behörighet att tilldela en roll visas ett felmeddelande om att kontot inte har behörighet att utföra åtgärden "Microsoft.Authorization/roleAssignments/write". Kontakta Azure Active Directory-administratören om du vill hantera roller.

När en roll läggs till begränsas _inte_ tidigare tilldelade behörigheter. När du begränsar behörigheter för tjänstens huvudnamn bör rollen **Deltagare** tas bort.

Du bekräftar ändringarna genom att ange de roller som är tilldelade:

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>Logga in med ett tjänsthuvudnamn

Testa det nya tjänsthuvudnamnets autentiseringsuppgifter och behörigheter genom att logga in. Om du vill logga in med ett huvudnamn för tjänsten behöver du det `applicationId`-värde som är associerat med det, och den klient som det skapades under.

Så här loggar du in med ett huvudnamn för tjänsten med lösenord:

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

För certifikatbaserad autentisering måste Azure PowerShell kunna hämta information från ett lokalt certifikatarkiv baserat på ett tumavtryck för certifikat.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

Anvisningar för hur du importerar ett certifikat i ett arkiv för autentiseringsuppgifter som är tillgängliga från PowerShell finns i [Logga in med Azure PowerShell](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>Återställ autentiseringsuppgifter

Om du glömmer bort autentiseringsuppgifterna för ett huvudnamn för tjänsten läggar du till en ny autentiseringsuppgift med ett slumpmässigt lösenord med hjälp av [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential). Denna cmdlet stöder inte användardefinierade autentiseringsuppgifter när du återställer lösenordet.

> [!IMPORTANT]
> Innan du tilldelar några nya autentiseringsuppgifter kan du ta bort befintliga autentiseringsuppgifter för att förhindra att de används för inloggning. Det gör du med cmdleten [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a>Felsökning

Om du får följande fel: _"New-AzADServicePrincipal: Ett annat objekt med samma värde för egenskapen identifierUris finns redan."_ så kontrollerar du att det inte redan finns ett tjänsthuvudnamn med samma namn.

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Om det befintliga tjänsthuvudnamnet inte längre behövs kan du ta bort det med hjälp av följande exempel.

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Det här felet kan också inträffa om du tidigare har skapat ett tjänsthuvudnamn för ett Azure Active Directory-program. Om du tar bort tjänsthuvudnamnet är programmet fortfarande tillgängligt. Det här programmet förhindrar att du skapar ett annat tjänsthuvudnamn med samma namn.

Du kan använda följande exempel för att kontrollera att det inte finns något Azure Active Directory-program med samma namn:

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

Om det finns ett program med samma namn som inte längre behövs så kan det tas bort med hjälp av följande exempel.

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

Annars väljer du ett alternativt namn för det nya huvudtjänstnamn som du försöker skapa.
