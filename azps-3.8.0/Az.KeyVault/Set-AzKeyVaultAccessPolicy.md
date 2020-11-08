---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 15ee05260a4714831808b68b1bc8b1784d9ffdd2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100604"
---
# <span data-ttu-id="8a80f-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8a80f-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="8a80f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a80f-102">SYNOPSIS</span></span>
<span data-ttu-id="8a80f-103">Tilldelar eller ändrar befintliga behörigheter för en användare, program eller säkerhets grupp för att utföra operationer med ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="8a80f-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="8a80f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a80f-104">SYNTAX</span></span>

### <span data-ttu-id="8a80f-105">ByUserPrincipalName (standard)</span><span class="sxs-lookup"><span data-stu-id="8a80f-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a80f-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="8a80f-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a80f-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a80f-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a80f-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8a80f-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a80f-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="8a80f-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a80f-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="8a80f-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a80f-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a80f-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a80f-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a80f-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a80f-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8a80f-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a80f-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="8a80f-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a80f-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="8a80f-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a80f-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a80f-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a80f-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a80f-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a80f-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8a80f-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a80f-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="8a80f-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a80f-120">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a80f-120">DESCRIPTION</span></span>
<span data-ttu-id="8a80f-121">Cmdleten **set-AzKeyVaultAccessPolicy** beviljar eller ändrar befintliga behörigheter för en användare, program eller säkerhets grupp för att utföra de angivna åtgärderna med ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="8a80f-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="8a80f-122">De behörigheter som andra användare, program eller säkerhets grupper har i Key-valvet ändras inte.</span><span class="sxs-lookup"><span data-stu-id="8a80f-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="8a80f-123">Om du anger behörigheter för en säkerhets grupp påverkar den här åtgärden endast användare i den säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="8a80f-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="8a80f-124">Följande kataloger måste vara samma Azure-katalog:</span><span class="sxs-lookup"><span data-stu-id="8a80f-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="8a80f-125">Standard katalogen för Azure-abonnemanget som Key-valvet finns i.</span><span class="sxs-lookup"><span data-stu-id="8a80f-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="8a80f-126">Den Azure-katalog som innehåller den användare eller program grupp som du beviljar behörigheter till.</span><span class="sxs-lookup"><span data-stu-id="8a80f-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="8a80f-127">Exempel på scenarier om dessa villkor inte uppfylls och denna cmdlet inte fungerar:</span><span class="sxs-lookup"><span data-stu-id="8a80f-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="8a80f-128">Att auktorisera en användare från en annan organisation för att hantera ditt nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="8a80f-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="8a80f-129">Varje organisation har sin egen katalog.</span><span class="sxs-lookup"><span data-stu-id="8a80f-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="8a80f-130">Ditt Azure-konto har flera kataloger.</span><span class="sxs-lookup"><span data-stu-id="8a80f-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="8a80f-131">Om du registrerar ett program i en annan katalog än standard katalogen kan du inte auktorisera att programmet kan använda ditt nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="8a80f-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="8a80f-132">Programmet måste finnas i standard katalogen.</span><span class="sxs-lookup"><span data-stu-id="8a80f-132">The application must be in the default directory.</span></span>
<span data-ttu-id="8a80f-133">Observera att även om resurs gruppen är valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="8a80f-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="8a80f-134">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a80f-134">EXAMPLES</span></span>

### <span data-ttu-id="8a80f-135">Exempel 1: bevilja behörigheter till en användare för ett nyckeltal och ändra behörigheterna</span><span class="sxs-lookup"><span data-stu-id="8a80f-135">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="8a80f-136">Det första kommandot tilldelar behörigheter för en användare i din Azure Active Directory, PattiFuller@contoso.com för att utföra operationer på nycklar och hemligheter med en nyckel valv med namnet Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8a80f-136">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="8a80f-137">Parametern *Passthru* ger det uppdaterade objektet som returneras av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a80f-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="8a80f-138">Det andra kommandot ändrar de behörigheter som beviljats PattiFuller@contoso.com i det första kommandot för att nu tillåta att hemligheter läggs till för att lägga till och ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="8a80f-138">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="8a80f-139">Behörigheten för viktiga operationer är oförändrad efter det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="8a80f-139">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="8a80f-140">Med kommandot slut ändrar du ytterligare behörigheter för PattiFuller@contoso.com att ta bort alla behörigheter för viktiga operationer.</span><span class="sxs-lookup"><span data-stu-id="8a80f-140">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="8a80f-141">Behörigheterna till hemliga funktioner ändras inte efter det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="8a80f-141">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="8a80f-142">Exempel 2: bevilja behörigheter för en program tjänst för att läsa och skriva hemligheter</span><span class="sxs-lookup"><span data-stu-id="8a80f-142">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="8a80f-143">Det här kommandot ger behörighet till ett program för ett nyckeltal med namnet Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8a80f-143">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="8a80f-144">Parametern *servicePrincipalName* anger programmet.</span><span class="sxs-lookup"><span data-stu-id="8a80f-144">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="8a80f-145">Programmet måste vara registrerat i din Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8a80f-145">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="8a80f-146">Värdet för parametern *servicePrincipalName* måste vara antingen tjänstens huvud namn eller GUID för programmets ID.</span><span class="sxs-lookup"><span data-stu-id="8a80f-146">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="8a80f-147">I det här exemplet anges tjänstens huvud namn `http://payroll.contoso.com` och kommandot ger behörighet att läsa och skriva hemligheter.</span><span class="sxs-lookup"><span data-stu-id="8a80f-147">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="8a80f-148">Exempel 3: bevilja behörigheter för ett program med dess objekt-ID</span><span class="sxs-lookup"><span data-stu-id="8a80f-148">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="8a80f-149">Det här kommandot ger behörighet att läsa och skriva hemligheter.</span><span class="sxs-lookup"><span data-stu-id="8a80f-149">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="8a80f-150">I det här exemplet anges programmet med objekt-ID för tjänstens huvud program.</span><span class="sxs-lookup"><span data-stu-id="8a80f-150">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="8a80f-151">Exempel 4: bevilja behörigheter för ett huvud namn för användare</span><span class="sxs-lookup"><span data-stu-id="8a80f-151">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="8a80f-152">Det här kommandot tilldelar behörigheterna get, list och Set för det angivna UPN-namnet för åtkomst till hemligheter.</span><span class="sxs-lookup"><span data-stu-id="8a80f-152">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="8a80f-153">Exempel 5: Aktivera att hemligheter kan hämtas från ett nyckelord till Microsoft. Compute Resource Provider</span><span class="sxs-lookup"><span data-stu-id="8a80f-153">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="8a80f-154">Det här kommandot ger behörighet att hämta hemligheter från Contoso03Vault Key Vault av Microsoft. Compute Resource Provider.</span><span class="sxs-lookup"><span data-stu-id="8a80f-154">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="8a80f-155">Exempel 6: bevilja behörigheter till en säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="8a80f-155">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="8a80f-156">I det första kommandot används cmdleten Get-AzADGroup för att hämta alla Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="8a80f-156">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="8a80f-157">Från utdata ser du 3 grupper som returneras, med namnet **Grupp1** , **group2** och **Group3**.</span><span class="sxs-lookup"><span data-stu-id="8a80f-157">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="8a80f-158">Flera grupper kan ha samma namn men alltid har ett unikt ObjectId.</span><span class="sxs-lookup"><span data-stu-id="8a80f-158">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="8a80f-159">Om fler än en grupp med samma namn returneras använder du ObjectId i utdata för att identifiera den du vill använda.</span><span class="sxs-lookup"><span data-stu-id="8a80f-159">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="8a80f-160">Du kan sedan använda kommandots utdata med Set-AzKeyVaultAccessPolicy om du vill ge behörighet till group2 för ditt nyckeltal, med namnet **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="8a80f-160">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="8a80f-161">I det här exemplet räknas grupperna ' group2 ' in i samma kommando rad.</span><span class="sxs-lookup"><span data-stu-id="8a80f-161">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="8a80f-162">Det kan finnas flera grupper i den returnerade listan som heter ' group2 '.</span><span class="sxs-lookup"><span data-stu-id="8a80f-162">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="8a80f-163">I det här exemplet plockas den första, som anges med index \[ 0 \] i den returnerade listan.</span><span class="sxs-lookup"><span data-stu-id="8a80f-163">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="8a80f-164">Exempel 7: bevilja åtkomst för Azure information Protection till kund hanterad klient organisation (BYOK)</span><span class="sxs-lookup"><span data-stu-id="8a80f-164">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="8a80f-165">Det här kommandot auktoriserar Azure information Protection att använda en kundhanterad knapp (skapa en egen-eller "BYOK"-scenario) som klient organisations-knappen för Azure information Protection.</span><span class="sxs-lookup"><span data-stu-id="8a80f-165">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="8a80f-166">När du kör det här kommandot ska du ange ditt eget namn på Key Vault, men du måste ange parametern *servicePrincipalName* med GUID **00000012-0000-0000-C000-000000000000** och ange behörigheterna i exemplet.</span><span class="sxs-lookup"><span data-stu-id="8a80f-166">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="8a80f-167">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a80f-167">PARAMETERS</span></span>

### <span data-ttu-id="8a80f-168">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8a80f-168">-ApplicationId</span></span>
<span data-ttu-id="8a80f-169">För framtida användning.</span><span class="sxs-lookup"><span data-stu-id="8a80f-169">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-170">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="8a80f-170">-BypassObjectIdValidation</span></span>
<span data-ttu-id="8a80f-171">Gör det möjligt att ange ett objekt-ID utan att verifiera att objektet finns i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8a80f-171">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="8a80f-172">Använd endast den här parametern om du vill bevilja åtkomst till ditt nyckeltal till ett objekt-ID som refererar till en delegerad säkerhets grupp från en annan Azure-klient.</span><span class="sxs-lookup"><span data-stu-id="8a80f-172">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a80f-173">-DefaultProfile</span></span>
<span data-ttu-id="8a80f-174">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8a80f-174">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a80f-175">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8a80f-175">-EmailAddress</span></span>
<span data-ttu-id="8a80f-176">Anger användarens e-postadress för den användare som ska bevilja behörigheter.</span><span class="sxs-lookup"><span data-stu-id="8a80f-176">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="8a80f-177">Den här e-postadressen måste finnas i katalogen som är kopplad till det aktuella abonnemanget och vara unik.</span><span class="sxs-lookup"><span data-stu-id="8a80f-177">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-178">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="8a80f-178">-EnabledForDeployment</span></span>
<span data-ttu-id="8a80f-179">Gör det möjligt för Microsoft. Compute Resource-leverantören att hämta hemligheter från det här nyckelvärdet när det här nyckelvärdet refereras i resurs skapande, till exempel när du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8a80f-179">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-180">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8a80f-180">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="8a80f-181">Aktiverar tjänsten Azure Disk Encryption för att få hemligheter och unwrap-nycklar från det här nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="8a80f-181">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-182">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="8a80f-182">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="8a80f-183">Gör det möjligt för Azure Resource Manager att få hemligheter från detta viktiga valv när det här nyckelvärdet refereras till i en mall.</span><span class="sxs-lookup"><span data-stu-id="8a80f-183">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-184">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a80f-184">-InputObject</span></span>
<span data-ttu-id="8a80f-185">Key valv-objekt</span><span class="sxs-lookup"><span data-stu-id="8a80f-185">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-186">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8a80f-186">-ObjectId</span></span>
<span data-ttu-id="8a80f-187">Anger objekt-ID: t för användaren eller tjänstens huvud namn i Azure Active Directory för vilket behörigheter ska beviljas.</span><span class="sxs-lookup"><span data-stu-id="8a80f-187">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-188">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a80f-188">-PassThru</span></span>
<span data-ttu-id="8a80f-189">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="8a80f-189">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a80f-190">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="8a80f-190">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-191">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="8a80f-191">-PermissionsToCertificates</span></span>
<span data-ttu-id="8a80f-192">Anger en matris med certifikat behörigheter som ska beviljas till en användare eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="8a80f-192">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8a80f-193">De acceptabla värdena för den här parametern:</span><span class="sxs-lookup"><span data-stu-id="8a80f-193">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="8a80f-194">Lära</span><span class="sxs-lookup"><span data-stu-id="8a80f-194">Get</span></span>
- <span data-ttu-id="8a80f-195">Förteckning</span><span class="sxs-lookup"><span data-stu-id="8a80f-195">List</span></span>
- <span data-ttu-id="8a80f-196">Ta bort</span><span class="sxs-lookup"><span data-stu-id="8a80f-196">Delete</span></span>
- <span data-ttu-id="8a80f-197">Göra</span><span class="sxs-lookup"><span data-stu-id="8a80f-197">Create</span></span>
- <span data-ttu-id="8a80f-198">Importeras</span><span class="sxs-lookup"><span data-stu-id="8a80f-198">Import</span></span>
- <span data-ttu-id="8a80f-199">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="8a80f-199">Update</span></span>
- <span data-ttu-id="8a80f-200">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="8a80f-200">Managecontacts</span></span>
- <span data-ttu-id="8a80f-201">Getissuers</span><span class="sxs-lookup"><span data-stu-id="8a80f-201">Getissuers</span></span>
- <span data-ttu-id="8a80f-202">Listissuers</span><span class="sxs-lookup"><span data-stu-id="8a80f-202">Listissuers</span></span>
- <span data-ttu-id="8a80f-203">Setissuers</span><span class="sxs-lookup"><span data-stu-id="8a80f-203">Setissuers</span></span>
- <span data-ttu-id="8a80f-204">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="8a80f-204">Deleteissuers</span></span>
- <span data-ttu-id="8a80f-205">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="8a80f-205">Manageissuers</span></span>
- <span data-ttu-id="8a80f-206">Ã</span><span class="sxs-lookup"><span data-stu-id="8a80f-206">Recover</span></span>
- <span data-ttu-id="8a80f-207">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="8a80f-207">Backup</span></span>
- <span data-ttu-id="8a80f-208">Terställa</span><span class="sxs-lookup"><span data-stu-id="8a80f-208">Restore</span></span>
- <span data-ttu-id="8a80f-209">Tömning</span><span class="sxs-lookup"><span data-stu-id="8a80f-209">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-210">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="8a80f-210">-PermissionsToKeys</span></span>
<span data-ttu-id="8a80f-211">Anger en matris med viktiga behörigheter för att bevilja en användare eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="8a80f-211">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8a80f-212">De acceptabla värdena för den här parametern:</span><span class="sxs-lookup"><span data-stu-id="8a80f-212">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="8a80f-213">Dekryptera</span><span class="sxs-lookup"><span data-stu-id="8a80f-213">Decrypt</span></span>
- <span data-ttu-id="8a80f-214">Inträffade</span><span class="sxs-lookup"><span data-stu-id="8a80f-214">Encrypt</span></span>
- <span data-ttu-id="8a80f-215">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="8a80f-215">UnwrapKey</span></span>
- <span data-ttu-id="8a80f-216">WrapKey</span><span class="sxs-lookup"><span data-stu-id="8a80f-216">WrapKey</span></span>
- <span data-ttu-id="8a80f-217">Kontroll</span><span class="sxs-lookup"><span data-stu-id="8a80f-217">Verify</span></span>
- <span data-ttu-id="8a80f-218">Logga in</span><span class="sxs-lookup"><span data-stu-id="8a80f-218">Sign</span></span>
- <span data-ttu-id="8a80f-219">Lära</span><span class="sxs-lookup"><span data-stu-id="8a80f-219">Get</span></span>
- <span data-ttu-id="8a80f-220">Förteckning</span><span class="sxs-lookup"><span data-stu-id="8a80f-220">List</span></span>
- <span data-ttu-id="8a80f-221">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="8a80f-221">Update</span></span>
- <span data-ttu-id="8a80f-222">Göra</span><span class="sxs-lookup"><span data-stu-id="8a80f-222">Create</span></span>
- <span data-ttu-id="8a80f-223">Importeras</span><span class="sxs-lookup"><span data-stu-id="8a80f-223">Import</span></span>
- <span data-ttu-id="8a80f-224">Ta bort</span><span class="sxs-lookup"><span data-stu-id="8a80f-224">Delete</span></span>
- <span data-ttu-id="8a80f-225">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="8a80f-225">Backup</span></span>
- <span data-ttu-id="8a80f-226">Terställa</span><span class="sxs-lookup"><span data-stu-id="8a80f-226">Restore</span></span>
- <span data-ttu-id="8a80f-227">Ã</span><span class="sxs-lookup"><span data-stu-id="8a80f-227">Recover</span></span>
- <span data-ttu-id="8a80f-228">Tömning</span><span class="sxs-lookup"><span data-stu-id="8a80f-228">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-229">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="8a80f-229">-PermissionsToSecrets</span></span>
<span data-ttu-id="8a80f-230">Anger en matris med hemliga åtgärds behörigheter som ska beviljas till en användare eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="8a80f-230">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8a80f-231">De acceptabla värdena för den här parametern:</span><span class="sxs-lookup"><span data-stu-id="8a80f-231">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="8a80f-232">Lära</span><span class="sxs-lookup"><span data-stu-id="8a80f-232">Get</span></span>
- <span data-ttu-id="8a80f-233">Förteckning</span><span class="sxs-lookup"><span data-stu-id="8a80f-233">List</span></span>
- <span data-ttu-id="8a80f-234">Ge</span><span class="sxs-lookup"><span data-stu-id="8a80f-234">Set</span></span>
- <span data-ttu-id="8a80f-235">Ta bort</span><span class="sxs-lookup"><span data-stu-id="8a80f-235">Delete</span></span>
- <span data-ttu-id="8a80f-236">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="8a80f-236">Backup</span></span>
- <span data-ttu-id="8a80f-237">Terställa</span><span class="sxs-lookup"><span data-stu-id="8a80f-237">Restore</span></span>
- <span data-ttu-id="8a80f-238">Ã</span><span class="sxs-lookup"><span data-stu-id="8a80f-238">Recover</span></span>
- <span data-ttu-id="8a80f-239">Tömning</span><span class="sxs-lookup"><span data-stu-id="8a80f-239">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-240">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="8a80f-240">-PermissionsToStorage</span></span>
<span data-ttu-id="8a80f-241">Anger hanterat lagrings konto och behörigheter för säkerhets associationer för att bevilja användare eller tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="8a80f-241">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-242">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a80f-242">-ResourceGroupName</span></span>
<span data-ttu-id="8a80f-243">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8a80f-243">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-244">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a80f-244">-ResourceId</span></span>
<span data-ttu-id="8a80f-245">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="8a80f-245">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-246">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a80f-246">-ServicePrincipalName</span></span>
<span data-ttu-id="8a80f-247">Anger tjänstens huvud namn för det program som ska bevilja behörigheter.</span><span class="sxs-lookup"><span data-stu-id="8a80f-247">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="8a80f-248">Ange program-ID, som också kallas klient-ID, som är registrerat i AzureActive-katalogen.</span><span class="sxs-lookup"><span data-stu-id="8a80f-248">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="8a80f-249">Programmet med SPN-namnet som den här parametern anger måste vara registrerat i Azure-katalogen som innehåller ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="8a80f-249">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-250">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a80f-250">-UserPrincipalName</span></span>
<span data-ttu-id="8a80f-251">Anger användarens huvud namn för den användare som ska bevilja behörigheter.</span><span class="sxs-lookup"><span data-stu-id="8a80f-251">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="8a80f-252">Det här UPN-namnet måste finnas i katalogen som är kopplad till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8a80f-252">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-253">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8a80f-253">-VaultName</span></span>
<span data-ttu-id="8a80f-254">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="8a80f-254">Specifies the name of a key vault.</span></span>
<span data-ttu-id="8a80f-255">Denna cmdlet ändrar åtkomst principen för det Key-valv som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8a80f-255">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a80f-256">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a80f-256">-Confirm</span></span>
<span data-ttu-id="8a80f-257">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a80f-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a80f-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a80f-258">-WhatIf</span></span>
<span data-ttu-id="8a80f-259">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a80f-259">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a80f-260">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a80f-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a80f-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a80f-261">CommonParameters</span></span>
<span data-ttu-id="8a80f-262">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a80f-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a80f-263">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a80f-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a80f-264">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a80f-264">INPUTS</span></span>

### <span data-ttu-id="8a80f-265">Microsoft. Azure. commands. valv. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8a80f-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="8a80f-266">System. String</span><span class="sxs-lookup"><span data-stu-id="8a80f-266">System.String</span></span>

## <span data-ttu-id="8a80f-267">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a80f-267">OUTPUTS</span></span>

### <span data-ttu-id="8a80f-268">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8a80f-268">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8a80f-269">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a80f-269">NOTES</span></span>

## <span data-ttu-id="8a80f-270">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a80f-270">RELATED LINKS</span></span>

[<span data-ttu-id="8a80f-271">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8a80f-271">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="8a80f-272">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8a80f-272">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

