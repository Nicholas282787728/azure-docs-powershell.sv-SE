---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 3c96ab0cdcc25e0e1c9b4a343cd68420654d934c
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/05/2020
ms.locfileid: "94326147"
---
# <span data-ttu-id="4172c-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4172c-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="4172c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4172c-102">SYNOPSIS</span></span>
<span data-ttu-id="4172c-103">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4172c-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="4172c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4172c-104">SYNTAX</span></span>

### <span data-ttu-id="4172c-105">SimpleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4172c-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4172c-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4172c-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4172c-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4172c-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4172c-120">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4172c-120">DESCRIPTION</span></span>

<span data-ttu-id="4172c-121">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4172c-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="4172c-122">Standard parameter uppsättningen använder standardvärden för parametrar om de inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="4172c-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="4172c-123">Mer information om standardvärden finns i beskrivningen för varje parameter.</span><span class="sxs-lookup"><span data-stu-id="4172c-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="4172c-124">Denna cmdlet har möjlighet att tilldela tjänstens huvud namn rollen med **roll** -och **omfattnings** parametrarna.</span><span class="sxs-lookup"><span data-stu-id="4172c-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="4172c-125">Om båda utelämnas är rollen deltagare kopplad till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="4172c-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="4172c-126">Standardvärdena för **roll** -och **omfattnings** parametrarna är **deltagare** för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4172c-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="4172c-127">Cmdleten skapar ett program och anger dess egenskaper om en ApplicationId inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="4172c-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="4172c-128">Om du vill uppdatera de programspecifika parametrarna använder du cmdleten [Update-AzADApplication](./update-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="4172c-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="4172c-129">När du skapar ett tjänst huvud med kommandot **New-AzADServicePrincipal** innehåller utdata de autentiseringsuppgifter du måste skydda.</span><span class="sxs-lookup"><span data-stu-id="4172c-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="4172c-130">Se till att du inte tar med de här uppgifterna i koden eller kontrol lera uppgifterna i käll kontrollen.</span><span class="sxs-lookup"><span data-stu-id="4172c-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="4172c-131">Som ett alternativ bör du överväga att använda [hanterade identiteter](/azure/active-directory/managed-identities-azure-resources/overview) för att undvika att behöva använda autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="4172c-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="4172c-132">Som standard tilldelar **AzADServicePrincipal** rollen [deltagare](/azure/role-based-access-control/built-in-roles#contributor) till tjänstens huvud namn i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="4172c-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="4172c-133">För att minska risken för en komprometterad tjänstens huvud konto tilldelar du en mer specifik roll och begränsar omfattningen till en resurs eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4172c-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="4172c-134">Mer information finns i [steg för att lägga till en roll tilldelning](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="4172c-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="4172c-135">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4172c-135">EXAMPLES</span></span>

### <span data-ttu-id="4172c-136">Exempel 1: simple Active Directory Service-huvudobjekt</span><span class="sxs-lookup"><span data-stu-id="4172c-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="4172c-137">I följande exempel skapas ett AD-huvudobjekt med standardvärden för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="4172c-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="4172c-138">Eftersom inget program-ID anges skapas ett program för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="4172c-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="4172c-139">Eftersom det inte finns några värden för **rollen** eller **omfattningen** tilldelas den skapade tjänstens huvud namn rollen **deltagare** för den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4172c-139">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="4172c-140">Exempel 2: simple Active Directory-huvudfunktionen skapa med en viss roll och standard omfattning</span><span class="sxs-lookup"><span data-stu-id="4172c-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="4172c-141">I följande exempel skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="4172c-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="4172c-142">Eftersom inget program-ID anges skapas ett program för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="4172c-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="4172c-143">Tjänstens huvud namn skapas med **läsar** behörigheter för det aktuella abonnemanget eftersom inget värde har ställts in för parametern **scope** .</span><span class="sxs-lookup"><span data-stu-id="4172c-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="4172c-144">Exempel 3: simple skapa AD-tjänstens huvud objekt med ett angivet omfattning och standard roll</span><span class="sxs-lookup"><span data-stu-id="4172c-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="4172c-145">I följande exempel skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="4172c-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="4172c-146">Eftersom inget program-ID anges skapas ett program för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="4172c-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="4172c-147">Tjänstens huvud namn skapas med **deltagar** behörigheter för det tillhandahållna resurs grupp omfånget eftersom inget värde är angivet för parametern **Role** .</span><span class="sxs-lookup"><span data-stu-id="4172c-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="4172c-148">Exempel 4: simple Active Directory-huvudfunktionen skapa med ett angivet omfång och en viss roll</span><span class="sxs-lookup"><span data-stu-id="4172c-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="4172c-149">I följande exempel skapas ett AD-huvudobjekt med standardvärdena för parametrar som inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="4172c-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="4172c-150">Eftersom inget program-ID anges skapas ett program för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="4172c-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="4172c-151">Tjänstens huvud namn skapas med **läsar** behörigheter för den tillhandahållna resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="4172c-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="4172c-152">Exempel 5: skapa ett nytt AD tjänst-huvudobjekt med program-ID med roll tilldelning</span><span class="sxs-lookup"><span data-stu-id="4172c-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="4172c-153">I följande exempel skapas ett nytt AD-huvudhuvudprogram för programmet med program-ID ' 00000000-0000-0000-0000-000000000000 '.</span><span class="sxs-lookup"><span data-stu-id="4172c-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="4172c-154">Eftersom det inte finns några värden för **rollen** eller **omfattningen** tilldelas den skapade tjänstens huvud namn rollen **deltagare** för den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4172c-154">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="4172c-155">Exempel 6: skapa ett nytt AD service-huvudobjekt med ledning</span><span class="sxs-lookup"><span data-stu-id="4172c-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="4172c-156">I följande exempel hämtas programmet med objekt-ID ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' med cmdleten [Get-AzADApplication](./get-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="4172c-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="4172c-157">Resultaten är piped till `New-AzADServicePrincipal` cmdleten för att skapa ett nytt AD-huvudhuvudprogram för det programmet.</span><span class="sxs-lookup"><span data-stu-id="4172c-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="4172c-158">Exempel 7: skapa ett nytt AD service-huvudobjekt med DisplayName och lösen ords identifiering</span><span class="sxs-lookup"><span data-stu-id="4172c-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="4172c-159">I följande exempel skapas ett nytt program med namnet **servicePrincipalName** och ett lösen ord på **StrongPassworld! 23**.</span><span class="sxs-lookup"><span data-stu-id="4172c-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="4172c-160">Den tjänstens huvud namn skapas baserat på det skapade programmet.</span><span class="sxs-lookup"><span data-stu-id="4172c-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="4172c-161">Start datum och slutdatum läggs till i lösen ords informationen.</span><span class="sxs-lookup"><span data-stu-id="4172c-161">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="4172c-162">Exempel 8: skapa ett nytt AD service-huvudobjekt med DisplayName och vanliga autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="4172c-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="4172c-163">I följande exempel skapas ett nytt program med namnet **servicePrincipalName** och ett certifikat **$cert**. Den tjänstens huvud namn skapas baserat på programmet som skapades.</span><span class="sxs-lookup"><span data-stu-id="4172c-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="4172c-164">Slutdatumet läggs till för viktiga autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="4172c-164">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="4172c-165">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4172c-165">PARAMETERS</span></span>

### <span data-ttu-id="4172c-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4172c-166">-ApplicationId</span></span>

<span data-ttu-id="4172c-167">Unikt program-ID för tjänstens huvud namn i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="4172c-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="4172c-168">Det går inte att ändra egenskapen när den har skapats.</span><span class="sxs-lookup"><span data-stu-id="4172c-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="4172c-169">Om inget program-ID för ett befintligt program anges skapas ett program.</span><span class="sxs-lookup"><span data-stu-id="4172c-169">If an application ID for an existing application is not specified, an application is created.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="4172c-170">-ApplicationObject</span></span>

<span data-ttu-id="4172c-171">Det objekt som representerar det program som tjänstens huvud namn skapas för.</span><span class="sxs-lookup"><span data-stu-id="4172c-171">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="4172c-172">-CertValue</span></span>

<span data-ttu-id="4172c-173">Värdet för typen asymmetrisk autentiseringstyp.</span><span class="sxs-lookup"><span data-stu-id="4172c-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="4172c-174">Den representerar det Base64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="4172c-174">It represents the Base64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4172c-175">-DefaultProfile</span></span>

<span data-ttu-id="4172c-176">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4172c-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4172c-177">-DisplayName</span></span>

<span data-ttu-id="4172c-178">Eget namn på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="4172c-178">The friendly name of the service principal.</span></span> <span data-ttu-id="4172c-179">Om inget visnings namn anges används det här värdet för **Azure-PowerShell-mm-dd-yyyy – HH-mm-SS** där suffixet har skapats.</span><span class="sxs-lookup"><span data-stu-id="4172c-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4172c-180">-EndDate</span></span>

<span data-ttu-id="4172c-181">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="4172c-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="4172c-182">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="4172c-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="4172c-183">För en asymmetrisk datatyp måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="4172c-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-184">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="4172c-184">-KeyCredential</span></span>

<span data-ttu-id="4172c-185">Insamling av viktiga autentiseringsuppgifter associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="4172c-185">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="4172c-186">-PasswordCredential</span></span>

<span data-ttu-id="4172c-187">Den uppsättning autentiseringsuppgifter för lösen ord som är associerad med programmet.</span><span class="sxs-lookup"><span data-stu-id="4172c-187">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-188">-Roll</span><span class="sxs-lookup"><span data-stu-id="4172c-188">-Role</span></span>

<span data-ttu-id="4172c-189">Rollen som tjänstens huvud namn har.</span><span class="sxs-lookup"><span data-stu-id="4172c-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="4172c-190">Om inget värde anges används rollen **deltagare** **som standard.**</span><span class="sxs-lookup"><span data-stu-id="4172c-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-191">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="4172c-191">-Scope</span></span>

<span data-ttu-id="4172c-192">Omfattningen som tjänstens huvud namn har behörighet för.</span><span class="sxs-lookup"><span data-stu-id="4172c-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="4172c-193">Om inget värde anges används den aktuella prenumerationen **som standard.**</span><span class="sxs-lookup"><span data-stu-id="4172c-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="4172c-194">-SkipAssignment</span></span>

<span data-ttu-id="4172c-195">Om den är aktive rad kan du hoppa över skapandet av standard roll tilldelningen för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="4172c-195">If set, skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-196">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4172c-196">-StartDate</span></span>

<span data-ttu-id="4172c-197">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="4172c-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="4172c-198">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="4172c-198">The default start date value is today.</span></span> <span data-ttu-id="4172c-199">För en asymmetrisk datatyp måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="4172c-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-200">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4172c-200">-Confirm</span></span>

<span data-ttu-id="4172c-201">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4172c-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4172c-202">-WhatIf</span></span>

<span data-ttu-id="4172c-203">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4172c-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4172c-204">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4172c-204">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4172c-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4172c-205">CommonParameters</span></span>
<span data-ttu-id="4172c-206">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4172c-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4172c-207">Mer information finns i [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="4172c-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="4172c-208">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4172c-208">INPUTS</span></span>

### <span data-ttu-id="4172c-209">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4172c-209">System.Guid</span></span>

### <span data-ttu-id="4172c-210">System. String</span><span class="sxs-lookup"><span data-stu-id="4172c-210">System.String</span></span>

### <span data-ttu-id="4172c-211">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="4172c-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="4172c-212">Microsoft. Azure. commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="4172c-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="4172c-213">Microsoft. Azure. commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="4172c-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="4172c-214">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="4172c-214">System.DateTime</span></span>

## <span data-ttu-id="4172c-215">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4172c-215">OUTPUTS</span></span>

### <span data-ttu-id="4172c-216">Microsoft. Azure. commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4172c-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="4172c-217">Microsoft. Azure. kommandon. sources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="4172c-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="4172c-218">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4172c-218">NOTES</span></span>

<span data-ttu-id="4172c-219">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="4172c-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4172c-220">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4172c-220">RELATED LINKS</span></span>

[<span data-ttu-id="4172c-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4172c-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="4172c-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4172c-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="4172c-223">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="4172c-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="4172c-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="4172c-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="4172c-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4172c-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="4172c-226">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4172c-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="4172c-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4172c-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)
