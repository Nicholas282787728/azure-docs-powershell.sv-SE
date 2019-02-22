---
title: Skapa tjänstens huvudnamn för Azure med Azure PowerShell
description: Lär dig hur du skapar ett huvudnamn för tjänsten för din app eller tjänst med Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/12/2019
ms.locfileid: "56154167"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Skapa tjänstens huvudnamn för Azure med Azure PowerShell

Om du planerar att hantera appen eller tjänsten med Azure PowerShell bör du köra denna under tjänstens huvudnamn för Azure Active Directory (AAD), i stället för dina autentiseringsuppgifter. Den här artikeln vägleder dig genom att skapa ett säkerhetsobjekt med Azure PowerShell.

## <a name="what-is-a-service-principal"></a>Vad är ett huvudnamn för tjänsten?

Ett huvudnamn för Azure-tjänsten är en säkerhetsidentitet som används av appar som skapats av användare, tjänster och automatiseringsverktyg för att få åtkomst till specifika Azure-resurser. Huvudnamn för tjänster tilldelas specifika behörigheter som är relaterade till tjänstens uppgifter, vilket ger dig bättre säkerhetskontroll. Detta skiljer sig från en allmän användaridentitet, som vanligtvis har behörighet att göra ändringar.

## <a name="verify-your-own-permission-level"></a>Kontrollera din egen behörighetsnivå

Först måste du ha tillräcklig behörighet i Azure Active Directory och Azure-prenumerationen. Du måste kunna skapa en app i Active Directory och tilldela en roll till tjänstens huvudnamn.

Det enklaste sättet att kontrollera om kontot har rätt behörighet är via portalen. Se [Kontrollera behörighet som krävs i portalen](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Skapa ett huvudnamn för tjänsten för appen

När du är inloggad på ditt Azure-konto kan du skapa tjänstens huvudnamn. Du måste ha någon av följande metoder för att identifiera den distribuerade appen:

* Den distribuerade appens unika namn, till exempel "MyDemoWebApp", i följande exempel
* Program-ID, unikt GUID som är kopplat till den distribuerade appen, tjänsten eller objektet

### <a name="get-information-about-your-application"></a>Hämta information om programmet

Cmdleten `Get-AzADApplication` kan användas för att hämta information om programmet.

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>Skapa ett huvudnamn för tjänsten för programmet

Cmdleten `New-AzADServicePrincipal` används för att skapa tjänstens huvudnamn.

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

Härifrån kan du antingen direkt använda egenskapen `$servicePrincipal.Secret` som ett argument till `Connect-AzAccount` (se ”Logga in med tjänstens huvudnamn”) eller konvertera denna `SecureString` till en oformaterad textsträng:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a>Logga in med tjänstens huvudnamn

Nu kan du logga in som det nya huvudnamnet för tjänsten för appen med hjälp av det `appId` du angav och det `password` som  
genererades. Du behöver också klient-ID:t för tjänstens huvudnamn. Ditt klient-ID visas när du loggar in på Azure med dina personliga autentiseringsuppgifter. Använd de här kommandona för att logga in med ett huvudnamn för tjänsten:

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Efter en lyckad inloggning visas utdata som liknar följande:

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Grattis! Du kan använda dessa autentiseringsuppgifter för att köra appen. Därefter måste du justera behörigheterna för tjänstens huvudnamn.

## <a name="managing-roles"></a>Hantera roller

> [!NOTE]
> Rollbaserad åtkomst i Azure (RBAC) är en modell för att definiera och hantera roller för användar- och säkerhetsobjekt. Rollerna är kopplade till en uppsättning med behörigheter, som avgör vilka resurser en princip kan läsa, få åtkomst till, skriva till eller hantera. Mer information om RBAC och roller finns i [RBAC: inbyggda roller](/azure/active-directory/role-based-access-built-in-roles).

Azure PowerShell tillhandahåller följande cmdletar för att hantera rolltilldelningar:

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Standardrollen för tjänstens huvudnamn är **Deltagare**. Det kanske inte är det bästa valet beroende på omfattningen av appens interaktioner med Azure-tjänster, med tanke på dess breda behörighet.
Rollen **Läsare** är mer begränsad och kan vara ett bra val för skrivskyddade appar. Du kan visa information om rollspecifik behörighet eller skapa anpassad behörighet via Azure Portal.

I det här exemplet lägger vi till rollen **Läsare** i vårt tidigare exempel och tar bort rollen **Deltagare**:

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Visa de tilldelade rollerna:

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

Andra Azure PowerShell-cmdletar för rollhantering:

* [Get-AzRoleDefinition](/powershell/module/az.resources/Get-azRoleDefinition)
* [New-AzRoleDefinition](/powershell/module/az.resources/New-azRoleDefinition)
* [Remove-AzRoleDefinition](/powershell/module/az.resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Ändra autentiseringsuppgifter för säkerhetsobjektet

Det är en bra säkerhetsrutin att granska behörigheter och uppdatera lösenordet regelbundet. Du kanske också vill hantera och ändra säkerhetsreferenser när appen förändras. Det går till exempel att ändra lösenordet för tjänstens huvudnamn genom att skapa ett nytt lösenord och ta bort det gamla.

### <a name="add-a-new-password-for-the-service-principal"></a>Lägga till ett nytt lösenord för tjänstens huvudnamn

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Hämta en lista över autentiseringsuppgifter för tjänstens huvudnamn

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Ta bort det gamla lösenordet för tjänstens huvudnamn

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Bekräfta listan över autentiseringsuppgifter för tjänstens huvudnamn

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a>Hämta information om tjänstens huvudnamn

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
