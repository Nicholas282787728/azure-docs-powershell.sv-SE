---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med hanterade identiteter för Azure-resurser.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8f18af8ed67ecf2aefd353208c07bf812df732d9
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239902"
---
# <a name="sign-in-with-azure-powershell"></a>Logga in med Azure PowerShell

Azure PowerShell har stöd för flera autentiseringsmetoder. Det enklaste sättet att komma igång är med [Azure Cloud Shell](/azure/cloud-shell/overview), som automatiskt loggar in dig. Med en lokal installation kan du logga in interaktivt via webbläsaren. När du skriver skript för automatisering är den rekommenderade metoden att använda ett [tjänsthuvudnamn](create-azure-service-principal-azureps.md) med de nödvändiga behörigheterna. Du kan skydda dina Azure-resurser genom att begränsa behörigheterna för inloggning så mycket som möjligt.

Inledningsvis är du inloggad på den första prenumerationen Azure returnerar om du har åtkomst till fler än en prenumeration. Kommandon körs mot den här prenumerationen som standard. Använd cmdleten [Set-AzContext](/powershell/module/az.accounts/set-azcontext) för att ändra din aktiva prenumeration för en session. Använd [Select-AzContext](/powershell/module/az.accounts/select-azcontext)-cmdleten för att ändra din aktiva prenumeration och låta den vara permanent mellan sessioner på samma system.

> [!IMPORTANT]
> Dina autentiseringsuppgifter delas mellan flera PowerShell-sessioner så länge du är inloggad.
> Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).

## <a name="sign-in-interactively"></a>Logga in interaktivt

Använd cmdleten [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) för att logga in interaktivt.

```azurepowershell-interactive
Connect-AzAccount
```

När denna cmdlet körs från PowerShell version 6 och senare visar den en tokensträng. Logga in genom att kopiera den här strängen och klistra in den på [microsoft.com/devicelogin](https://microsoft.com/devicelogin) i en webbläsare. PowerShell-sessionen autentiseras därefter för anslutning till Azure. Du kan ange att parametern `UseDeviceAuthentication` ska ta emot en tokensträng i Windows PowerShell.

> [!IMPORTANT]
> Auktorisering med användarnamn/lösenord har tagits bort i Azure PowerShell på grund av ändringar i auktoriseringsimplementering och säkerhetsproblem i Active Directory. Om du använder autentiseringsuppgifter för automation får du i stället [skapa ett huvudnamn för tjänsten](create-azure-service-principal-azureps.md).

Använd cmdleten [Get-AzContext](/powershell/module/az.accounts/get-azcontext) för att lagra din klientorganisations ID i en variabel som ska användas i de följande två avsnitten i den här artikeln.

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a>Logga in med ett huvudnamn för tjänsten <a name="sp-signin"/>

Tjänstens huvudnamn är icke-interaktiva Azure-konton. Precis som med andra användarkonton hanteras deras behörigheter med Azure Active Directory. Genom att endast bevilja de behörigheter som krävs för tjänstens huvudnamn skyddas dina automatiseringsskript.

I [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) finns information om hur du skapar ett huvudnamn för tjänsten som ska användas med Azure PowerShell.

Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzAccount` för att logga in med ett huvudnamn för tjänsten. Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn. Hur du loggar in med ett huvudnamn för tjänsten beror på om det har konfigurerats för lösenordsbaserad eller certifikatbaserad autentisering.

### <a name="password-based-authentication"></a>Lösenordsbaserad autentisering

Skapa ett huvudnamn för tjänsten som ska användas i exemplen i det här avsnittet. Läs mer om att skapa tjänsthuvudnamn i [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn. Cmdleten visar en uppmaning om att ange användarnamn och lösenord. Använd tjänsthuvudnamnets `applicationID` som användarnamn och konvertera `secret` till oformaterad text för lösenordet.

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

I automationsscenarier måste du skapa autentiseringsuppgifter från ett tjänsthuvudnamns `applicationId` och `secret`:

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Se till att du använder metoder för säker lagring av lösenord vid automatisering av anslutningar med tjänstens huvudnamn.

### <a name="certificate-based-authentication"></a>Certifikatbaserad autentisering

För certifikatbaserad autentisering måste Azure PowerShell kunna hämta information från ett lokalt certifikatarkiv baserat på ett tumavtryck för certifikat.

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

När du använder tjänstens huvudnamn i stället för ett registrerat program, lägger du till argumentet `-ServicePrincipal` och anger program-ID:t för tjänstens huvudnamn som `-ApplicationId`-parameterns värde.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

I PowerShell 5.1 kan certifikatarkivet hanteras och kontrolleras med [PKI](/powershell/module/pkiclient)-modulen. I PowerShell Core 6.x och senare är processen mer komplicerad. Följande skript visar hur du importerar ett befintligt certifikat till det certifikatarkiv som är tillgängligt för PowerShell.

#### <a name="import-a-certificate-in-powershell-51"></a>Importera ett certifikat i PowerShell 5.1

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>Importera ett certifikat i PowerShell Core 6.x och senare

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a>Logga in med en hanterad identitet

Hanterade identiteter är en funktion i Azure Active Directory. Hanterade identiteter är tjänsthuvudnamn som tilldelats till resurser som körs i Azure. Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser. Hanterade identiteter är endast tillgängliga på resurser som körs i ett Azure-moln.

Det här exemplet ansluts med hjälp av den hanterade identiteten för värdmiljön. Om kommandot till exempel körs på en virtuell dator med en tilldelad hanterad tjänstidentitet kan koden logga in med hjälp av den tilldelade identiteten.

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Logga in med en klientorganisation som inte är standard eller som molnlösningsleverantör (CSP)

Om ditt konto är associerat med fler än en klientorganisation måste parametern `-Tenant` specificeras när du ansluter för att logga in. Den här parametern fungerar med alla inloggningsmetoder. När du loggar in kan det här parametervärdet antingen vara klientorganisationens objekt-ID för Azure (klient-ID) eller det fullständigt kvalificerade domännamnet för klientorganisationen.

Om du är [molnlösningsleverantör (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/)**måste** värdet `-Tenant` vara ett klient-ID.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Logga in på ett annat moln

Azures molntjänster erbjuder miljöer som följer regionala lagar för datahantering. För konton i ett regionalt moln anger du miljön när du loggar in med argumentet `-Environment`. Den här parametern fungerar med alla inloggningsmetoder. Om ditt konto till exempel finns i Kina-molnet:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Följande kommando hämtar en lista över tillgängliga miljöer:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
