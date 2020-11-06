---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 20a36e35c509ecca889d4059bd7e74ccafa22dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575633"
---
# <span data-ttu-id="0a8c7-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0a8c7-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="0a8c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8c7-103">Tilldelar eller ändrar befintliga behörigheter för en användare, program eller säkerhets grupp för att utföra operationer med ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a8c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a8c7-104">SYNTAX</span></span>

### <span data-ttu-id="0a8c7-105">ByUserPrincipalName (standard)</span><span class="sxs-lookup"><span data-stu-id="0a8c7-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c7-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="0a8c7-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c7-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0a8c7-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c7-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0a8c7-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a8c7-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="0a8c7-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c7-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="0a8c7-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c7-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0a8c7-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a8c7-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0a8c7-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a8c7-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0a8c7-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a8c7-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="0a8c7-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a8c7-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a8c7-115">DESCRIPTION</span></span>
<span data-ttu-id="0a8c7-116">Cmdleten **set-AzureRmKeyVaultAccessPolicy** beviljar eller ändrar befintliga behörigheter för en användare, program eller säkerhets grupp för att utföra de angivna åtgärderna med ett Key-valv.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-116">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="0a8c7-117">De behörigheter som andra användare, program eller säkerhets grupper har i Key-valvet ändras inte.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-117">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="0a8c7-118">Om du anger behörigheter för en säkerhets grupp påverkar den här åtgärden endast användare i den säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-118">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="0a8c7-119">Följande kataloger måste vara samma Azure-katalog:</span><span class="sxs-lookup"><span data-stu-id="0a8c7-119">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="0a8c7-120">Standard katalogen för Azure-abonnemanget som Key-valvet finns i.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-120">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="0a8c7-121">Den Azure-katalog som innehåller den användare eller program grupp som du beviljar behörigheter till.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-121">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="0a8c7-122">Exempel på scenarier om dessa villkor inte uppfylls och denna cmdlet inte fungerar:</span><span class="sxs-lookup"><span data-stu-id="0a8c7-122">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="0a8c7-123">Att auktorisera en användare från en annan organisation för att hantera ditt nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-123">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="0a8c7-124">Varje organisation har sin egen katalog.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-124">Each organization has its own directory.</span></span> 
- <span data-ttu-id="0a8c7-125">Ditt Azure-konto har flera kataloger.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-125">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="0a8c7-126">Om du registrerar ett program i en annan katalog än standard katalogen kan du inte auktorisera att programmet kan använda ditt nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-126">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="0a8c7-127">Programmet måste finnas i standard katalogen.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-127">The application must be in the default directory.</span></span>

<span data-ttu-id="0a8c7-128">Observera att även om resurs gruppen är valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-128">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="0a8c7-129">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a8c7-129">EXAMPLES</span></span>

### <span data-ttu-id="0a8c7-130">Exempel 1: bevilja behörigheter till en användare för ett nyckeltal och ändra behörigheterna</span><span class="sxs-lookup"><span data-stu-id="0a8c7-130">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="0a8c7-131">Det första kommandot tilldelar behörigheter för en användare i din Azure Active Directory, PattiFuller@contoso.com för att utföra operationer på nycklar och hemligheter med en nyckel valv med namnet Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-131">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="0a8c7-132">Det andra kommandot ändrar de behörigheter som beviljats PattiFuller@contoso.com i det första kommandot för att nu tillåta att hemligheter läggs till för att lägga till och ta bort dem.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-132">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="0a8c7-133">Behörigheten för viktiga operationer är oförändrad efter det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-133">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="0a8c7-134">Parametern *Passthru* ger det uppdaterade objektet som returneras av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-134">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="0a8c7-135">Med kommandot slut ändrar du ytterligare behörigheter för PattiFuller@contoso.com att ta bort alla behörigheter för viktiga operationer.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-135">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="0a8c7-136">Behörigheterna till hemliga funktioner ändras inte efter det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-136">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="0a8c7-137">Parametern *Passthru* ger det uppdaterade objektet som returneras av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="0a8c7-138">Exempel 2: bevilja behörigheter för en program tjänst för att läsa och skriva hemligheter</span><span class="sxs-lookup"><span data-stu-id="0a8c7-138">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="0a8c7-139">Det här kommandot ger behörighet till ett program för ett nyckeltal med namnet Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-139">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="0a8c7-140">Parametern *servicePrincipalName* anger programmet.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-140">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="0a8c7-141">Programmet måste vara registrerat i din Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-141">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="0a8c7-142">Värdet för parametern *servicePrincipalName* måste vara antingen tjänstens huvud namn eller GUID för programmets ID.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-142">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="0a8c7-143">I det här exemplet anges tjänstens huvud namn http://payroll.contoso.com och kommandot ger behörighet att läsa och skriva hemligheter.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-143">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="0a8c7-144">Exempel 3: bevilja behörigheter för ett program med dess objekt-ID</span><span class="sxs-lookup"><span data-stu-id="0a8c7-144">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="0a8c7-145">Det här kommandot ger behörighet att läsa och skriva hemligheter.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-145">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="0a8c7-146">I det här exemplet anges programmet med objekt-ID för tjänstens huvud program.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-146">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="0a8c7-147">Exempel 4: bevilja behörigheter för ett huvud namn för användare</span><span class="sxs-lookup"><span data-stu-id="0a8c7-147">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="0a8c7-148">Det här kommandot tilldelar behörigheterna get, list och Set för det angivna UPN-namnet för åtkomst till hemligheter.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-148">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="0a8c7-149">Exempel 5: Aktivera att hemligheter kan hämtas från ett nyckelord till Microsoft. Compute Resource Provider</span><span class="sxs-lookup"><span data-stu-id="0a8c7-149">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="0a8c7-150">Det här kommandot ger behörighet att hämta hemligheter från Contoso03Vault Key Vault av Microsoft. Compute Resource Provider.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-150">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="0a8c7-151">Exempel 6: bevilja behörigheter till en säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="0a8c7-151">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="0a8c7-152">I det första kommandot används cmdleten Get-AzureRmADGroup för att hämta alla Active Directory-grupper.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-152">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="0a8c7-153">Från utdata ser du 3 grupper som returneras, med namnet **Grupp1** , **group2** och **Group3**.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-153">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="0a8c7-154">Flera grupper kan ha samma namn men alltid har ett unikt ObjectId.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-154">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="0a8c7-155">Om fler än en grupp med samma namn returneras använder du ObjectId i utdata för att identifiera den du vill använda.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-155">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="0a8c7-156">Du kan sedan använda kommandots utdata med Set-AzureRmKeyVaultAccessPolicy om du vill ge behörighet till group2 för ditt nyckeltal, med namnet **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-156">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="0a8c7-157">I det här exemplet räknas grupperna ' group2 ' in i samma kommando rad.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-157">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="0a8c7-158">Det kan finnas flera grupper i den returnerade listan som heter ' group2 '.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-158">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="0a8c7-159">I det här exemplet plockas den första, som anges med index \[ 0 \] i den returnerade listan.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-159">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="0a8c7-160">Exempel 7: bevilja åtkomst för Azure information Protection till kund hanterad klient organisation (BYOK)</span><span class="sxs-lookup"><span data-stu-id="0a8c7-160">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="0a8c7-161">Det här kommandot auktoriserar Azure information Protection att använda en kundhanterad knapp (skapa en egen-eller "BYOK"-scenario) som klient organisations-knappen för Azure information Protection.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-161">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="0a8c7-162">När du kör det här kommandot ska du ange ditt eget namn på Key Vault, men du måste ange parametern *servicePrincipalName* med GUID **00000012-0000-0000-C000-000000000000** och ange behörigheterna i exemplet.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-162">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="0a8c7-163">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a8c7-163">PARAMETERS</span></span>

### <span data-ttu-id="0a8c7-164">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0a8c7-164">-ApplicationId</span></span>
<span data-ttu-id="0a8c7-165">För framtida användning.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-165">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-166">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="0a8c7-166">-BypassObjectIdValidation</span></span>
<span data-ttu-id="0a8c7-167">Gör det möjligt att ange ett objekt-ID utan att verifiera att objektet finns i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-167">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="0a8c7-168">Använd endast den här parametern om du vill bevilja åtkomst till ditt nyckeltal till ett objekt-ID som refererar till en delegerad säkerhets grupp från en annan Azure-klient.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-168">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8c7-169">-DefaultProfile</span></span>
<span data-ttu-id="0a8c7-170">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0a8c7-170">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-171">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="0a8c7-171">-EmailAddress</span></span>
<span data-ttu-id="0a8c7-172">Anger användarens e-postadress för den användare som ska bevilja behörigheter.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-172">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="0a8c7-173">Den här e-postadressen måste finnas i katalogen som är kopplad till det aktuella abonnemanget och vara unik.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-173">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-174">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="0a8c7-174">-EnabledForDeployment</span></span>
<span data-ttu-id="0a8c7-175">Gör det möjligt för Microsoft. Compute Resource-leverantören att hämta hemligheter från det här nyckelvärdet när det här nyckelvärdet refereras i resurs skapande, till exempel när du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-175">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-176">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="0a8c7-176">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="0a8c7-177">Aktiverar tjänsten Azure Disk Encryption för att få hemligheter och unwrap-nycklar från det här nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-177">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-178">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="0a8c7-178">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="0a8c7-179">Gör det möjligt för Azure Resource Manager att få hemligheter från detta viktiga valv när det här nyckelvärdet refereras till i en mall.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-179">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a8c7-180">-InputObject</span></span>
<span data-ttu-id="0a8c7-181">Key valv-objekt</span><span class="sxs-lookup"><span data-stu-id="0a8c7-181">Key Vault Object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0a8c7-182">-ObjectId</span></span>
<span data-ttu-id="0a8c7-183">Anger objekt-ID: t för användaren eller tjänstens huvud namn i Azure Active Directory för vilket behörigheter ska beviljas.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-183">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-184">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a8c7-184">-PassThru</span></span>
<span data-ttu-id="0a8c7-185">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-185">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="0a8c7-186">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-186">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-187">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="0a8c7-187">-PermissionsToCertificates</span></span>
<span data-ttu-id="0a8c7-188">Anger en matris med certifikat behörigheter som ska beviljas till en användare eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-188">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="0a8c7-189">De acceptabla värdena för den här parametern:</span><span class="sxs-lookup"><span data-stu-id="0a8c7-189">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="0a8c7-190">Lära</span><span class="sxs-lookup"><span data-stu-id="0a8c7-190">Get</span></span>
- <span data-ttu-id="0a8c7-191">Förteckning</span><span class="sxs-lookup"><span data-stu-id="0a8c7-191">List</span></span>
- <span data-ttu-id="0a8c7-192">Ta bort</span><span class="sxs-lookup"><span data-stu-id="0a8c7-192">Delete</span></span>
- <span data-ttu-id="0a8c7-193">Göra</span><span class="sxs-lookup"><span data-stu-id="0a8c7-193">Create</span></span>
- <span data-ttu-id="0a8c7-194">Importeras</span><span class="sxs-lookup"><span data-stu-id="0a8c7-194">Import</span></span>
- <span data-ttu-id="0a8c7-195">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="0a8c7-195">Update</span></span>
- <span data-ttu-id="0a8c7-196">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="0a8c7-196">Managecontacts</span></span>
- <span data-ttu-id="0a8c7-197">Getissuers</span><span class="sxs-lookup"><span data-stu-id="0a8c7-197">Getissuers</span></span>
- <span data-ttu-id="0a8c7-198">Listissuers</span><span class="sxs-lookup"><span data-stu-id="0a8c7-198">Listissuers</span></span>
- <span data-ttu-id="0a8c7-199">Setissuers</span><span class="sxs-lookup"><span data-stu-id="0a8c7-199">Setissuers</span></span>
- <span data-ttu-id="0a8c7-200">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="0a8c7-200">Deleteissuers</span></span>
- <span data-ttu-id="0a8c7-201">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="0a8c7-201">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-202">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="0a8c7-202">-PermissionsToKeys</span></span>
<span data-ttu-id="0a8c7-203">Anger en matris med viktiga behörigheter för att bevilja en användare eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-203">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="0a8c7-204">De acceptabla värdena för den här parametern:</span><span class="sxs-lookup"><span data-stu-id="0a8c7-204">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="0a8c7-205">Dekryptera</span><span class="sxs-lookup"><span data-stu-id="0a8c7-205">Decrypt</span></span>
- <span data-ttu-id="0a8c7-206">Inträffade</span><span class="sxs-lookup"><span data-stu-id="0a8c7-206">Encrypt</span></span>
- <span data-ttu-id="0a8c7-207">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="0a8c7-207">UnwrapKey</span></span>
- <span data-ttu-id="0a8c7-208">WrapKey</span><span class="sxs-lookup"><span data-stu-id="0a8c7-208">WrapKey</span></span>
- <span data-ttu-id="0a8c7-209">Kontroll</span><span class="sxs-lookup"><span data-stu-id="0a8c7-209">Verify</span></span>
- <span data-ttu-id="0a8c7-210">Logga in</span><span class="sxs-lookup"><span data-stu-id="0a8c7-210">Sign</span></span>
- <span data-ttu-id="0a8c7-211">Lära</span><span class="sxs-lookup"><span data-stu-id="0a8c7-211">Get</span></span>
- <span data-ttu-id="0a8c7-212">Förteckning</span><span class="sxs-lookup"><span data-stu-id="0a8c7-212">List</span></span>
- <span data-ttu-id="0a8c7-213">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="0a8c7-213">Update</span></span>
- <span data-ttu-id="0a8c7-214">Göra</span><span class="sxs-lookup"><span data-stu-id="0a8c7-214">Create</span></span>
- <span data-ttu-id="0a8c7-215">Importeras</span><span class="sxs-lookup"><span data-stu-id="0a8c7-215">Import</span></span>
- <span data-ttu-id="0a8c7-216">Ta bort</span><span class="sxs-lookup"><span data-stu-id="0a8c7-216">Delete</span></span>
- <span data-ttu-id="0a8c7-217">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="0a8c7-217">Backup</span></span>
- <span data-ttu-id="0a8c7-218">Terställa</span><span class="sxs-lookup"><span data-stu-id="0a8c7-218">Restore</span></span>
- <span data-ttu-id="0a8c7-219">Ã</span><span class="sxs-lookup"><span data-stu-id="0a8c7-219">Recover</span></span>
- <span data-ttu-id="0a8c7-220">Tömning</span><span class="sxs-lookup"><span data-stu-id="0a8c7-220">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-221">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="0a8c7-221">-PermissionsToSecrets</span></span>
<span data-ttu-id="0a8c7-222">Anger en matris med hemliga åtgärds behörigheter som ska beviljas till en användare eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-222">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="0a8c7-223">De acceptabla värdena för den här parametern:</span><span class="sxs-lookup"><span data-stu-id="0a8c7-223">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="0a8c7-224">Lära</span><span class="sxs-lookup"><span data-stu-id="0a8c7-224">Get</span></span>
- <span data-ttu-id="0a8c7-225">Förteckning</span><span class="sxs-lookup"><span data-stu-id="0a8c7-225">List</span></span>
- <span data-ttu-id="0a8c7-226">Ge</span><span class="sxs-lookup"><span data-stu-id="0a8c7-226">Set</span></span>
- <span data-ttu-id="0a8c7-227">Ta bort</span><span class="sxs-lookup"><span data-stu-id="0a8c7-227">Delete</span></span>
- <span data-ttu-id="0a8c7-228">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="0a8c7-228">Backup</span></span>
- <span data-ttu-id="0a8c7-229">Terställa</span><span class="sxs-lookup"><span data-stu-id="0a8c7-229">Restore</span></span>
- <span data-ttu-id="0a8c7-230">Ã</span><span class="sxs-lookup"><span data-stu-id="0a8c7-230">Recover</span></span>
- <span data-ttu-id="0a8c7-231">Tömning</span><span class="sxs-lookup"><span data-stu-id="0a8c7-231">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-232">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="0a8c7-232">-PermissionsToStorage</span></span>
<span data-ttu-id="0a8c7-233">Anger hanterat lagrings konto och behörigheter för säkerhets associationer för att bevilja användare eller tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-233">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-234">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a8c7-234">-ResourceGroupName</span></span>
<span data-ttu-id="0a8c7-235">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-235">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-236">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0a8c7-236">-ServicePrincipalName</span></span>
<span data-ttu-id="0a8c7-237">Anger tjänstens huvud namn för det program som ska bevilja behörigheter.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-237">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="0a8c7-238">Ange program-ID, som också kallas klient-ID, som är registrerat i AzureActive-katalogen.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-238">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="0a8c7-239">Programmet med SPN-namnet som den här parametern anger måste vara registrerat i Azure-katalogen som innehåller ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-239">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-240">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0a8c7-240">-UserPrincipalName</span></span>
<span data-ttu-id="0a8c7-241">Anger användarens huvud namn för den användare som ska bevilja behörigheter.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-241">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="0a8c7-242">Det här UPN-namnet måste finnas i katalogen som är kopplad till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-242">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-243">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0a8c7-243">-VaultName</span></span>
<span data-ttu-id="0a8c7-244">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-244">Specifies the name of a key vault.</span></span>

<span data-ttu-id="0a8c7-245">Denna cmdlet ändrar åtkomst principen för det Key-valv som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-245">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-246">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a8c7-246">-Confirm</span></span>
<span data-ttu-id="0a8c7-247">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-247">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-248">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a8c7-248">-WhatIf</span></span>
<span data-ttu-id="0a8c7-249">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-249">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a8c7-250">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-250">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c7-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8c7-251">CommonParameters</span></span>
<span data-ttu-id="0a8c7-252">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a8c7-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8c7-253">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a8c7-253">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8c7-254">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a8c7-254">INPUTS</span></span>

### <span data-ttu-id="0a8c7-255">Sträng, GUID, sträng [], växel</span><span class="sxs-lookup"><span data-stu-id="0a8c7-255">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="0a8c7-256">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a8c7-256">OUTPUTS</span></span>

### <span data-ttu-id="0a8c7-257">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a8c7-257">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="0a8c7-258">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a8c7-258">NOTES</span></span>

## <span data-ttu-id="0a8c7-259">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a8c7-259">RELATED LINKS</span></span>

[<span data-ttu-id="0a8c7-260">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a8c7-260">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="0a8c7-261">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0a8c7-261">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

