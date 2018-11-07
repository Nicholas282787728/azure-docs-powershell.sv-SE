---
title: Skapa tjänstens huvudnamn för Azure med Azure PowerShell
description: Lär dig hur du skapar ett huvudnamn för tjänsten för din app eller tjänst med Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 2333338a1c2de9dd2d1f3231918399190e249575
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211408"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Skapa tjänstens huvudnamn för Azure med Azure PowerShell

Om du planerar att hantera appen eller tjänsten med Azure PowerShell bör du köra denna under tjänstens huvudnamn för Azure Active Directory (AAD), i stället för dina autentiseringsuppgifter. Den här artikeln vägleder dig genom att skapa en säkerhetsprincip med Azure PowerShell.

> [!NOTE]
> Du kan också skapa ett huvudnamn för tjänsten via Azure Portal. Läs [Använd portalen för att skapa Active Directory-program och ett huvudnamn för tjänsten som får åtkomst till resurser](/azure/azure-resource-manager/resource-group-create-service-principal-portal) för mer information.

## <a name="what-is-a-service-principal"></a>Vad är ett huvudnamn för tjänsten?

Ett huvudnamn för Azure-tjänsten är en säkerhetsidentitet som används av appar som skapats av användare, tjänster och automatiseringsverktyg för att få åtkomst till specifika Azure-resurser. Se det som en användaridentitet (användarnamn och lösenord eller certifikat) med en specifik roll och väl kontrollerade behörigheter. Den behöver bara kunna utföra vissa åtgärder, till skillnad från en allmän användaridentitet. Det ger bättre säkerhet om du bara ger den lägsta behörighetsnivån som krävs för att den ska kunna utföra sina administrativa uppgifter.

## <a name="verify-your-own-permission-level"></a>Kontrollera din egen behörighetsnivå

Först måste du ha tillräcklig behörighet i Azure Active Directory och Azure-prenumerationen. Du måste specifikt kunna skapa en app i Active Directory och tilldela en roll till tjänstens huvudnamn.

Det enklaste sättet att kontrollera om kontot har tillräcklig behörighet är via portalen. Se [Kontrollera behörighet som krävs i portalen](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Skapa ett huvudnamn för tjänsten för appen

När du är inloggad på ditt Azure-konto, kan du skapa tjänstens huvudnamn. Du måste ha någon av följande metoder för att identifiera den distribuerade appen:

* Det unika namnet för den distribuerade appen, t.ex. "MyDemoWebApp" i följande exempel, eller
* program-ID, unikt GUID som är kopplat till den distribuerade appen, tjänsten eller objektet

### <a name="get-information-about-your-application"></a>Hämta information om programmet

Cmdleten `Get-AzureRmADApplication` kan användas för att identifiera information om programmet.

```powershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
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

Cmdleten `New-AzureRmADServicePrincipal` används för att skapa tjänstens huvudnamn.

```powershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>Hämta information om tjänstens huvudnamn

```powershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>Logga in med tjänstens huvudnamn

Du kan nu logga in som det nya huvudnamnet för tjänsten för appen med hjälp av det *appId* och *lösenord* du angav. Du måste ange klient-ID för kontot. Klient-ID visas när du loggar in på Azure med dina personliga autentiseringsuppgifter.

```powershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Kör detta kommando från en ny PowerShell-session. När registreringen är klar ser du något som liknar följande:

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

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

Standardrollen för tjänstens huvudnamn är **Deltagare**. Det kanske inte är det bästa valet beroende på omfattningen av appens interaktioner med Azure-tjänster, med tanke på dess breda behörighet.
Rollen **Läsare** är mer begränsad och kan vara ett bra val för skrivskyddade appar. Du kan visa information om rollspecifik behörighet eller skapa anpassad behörighet via Azure Portal.

I det här exemplet lägger vi till rollen **Läsare** i vårt tidigare exempel och tar bort rollen **Deltagare**:

```powershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
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

```powershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Visa de tilldelade rollerna:

```powershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
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

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Ändra autentiseringsuppgifter för säkerhetsobjektet

Det är en bra säkerhetsrutin att granska behörigheter och uppdatera lösenordet regelbundet. Du kanske också vill hantera och ändra säkerhetsreferenser när appen förändras. Det går till exempel att ändra lösenordet för tjänstens huvudnamn genom att skapa ett nytt lösenord och ta bort det gamla.

### <a name="add-a-new-password-for-the-service-principal"></a>Lägga till ett nytt lösenord för tjänstens huvudnamn

```powershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Hämta en lista över autentiseringsuppgifter för tjänstens huvudnamn

```powershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Ta bort det gamla lösenordet för tjänstens huvudnamn

```powershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Bekräfta listan över autentiseringsuppgifter för tjänstens huvudnamn

```powershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
