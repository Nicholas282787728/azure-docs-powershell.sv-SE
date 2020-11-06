---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 343cea9eb3d708e802d1e06f555fd13ab1cd8c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576959"
---
# <span data-ttu-id="dae42-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dae42-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="dae42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dae42-102">SYNOPSIS</span></span>
<span data-ttu-id="dae42-103">Tar bort alla behörigheter för en användare eller ett program från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="dae42-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dae42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dae42-104">SYNTAX</span></span>

### <span data-ttu-id="dae42-105">ByUserPrincipalName (standard)</span><span class="sxs-lookup"><span data-stu-id="dae42-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dae42-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="dae42-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dae42-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dae42-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dae42-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="dae42-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="dae42-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="dae42-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dae42-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="dae42-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="dae42-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="dae42-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="dae42-115">ResourceIdByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dae42-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="dae42-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="dae42-118">ResourceIdByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae42-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="dae42-119">ResourceIdForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dae42-120">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dae42-120">DESCRIPTION</span></span>
<span data-ttu-id="dae42-121">Cmdleten **Remove-AzureRmKeyVaultAccessPolicy** tar bort alla behörigheter för en användare eller ett program eller för alla användare och program från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="dae42-121">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="dae42-122">Även om du tar bort alla behörigheter kan ägaren av Azure-prenumerationen som innehåller nyckelordet lägga till behörigheter i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="dae42-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="dae42-123">Observera att även om resurs gruppen är valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="dae42-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="dae42-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dae42-124">EXAMPLES</span></span>

### <span data-ttu-id="dae42-125">Exempel 1: ta bort behörigheter för en användare</span><span class="sxs-lookup"><span data-stu-id="dae42-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="dae42-126">Det här kommandot tar bort alla behörigheter som en användare PattiFuller@contoso.com har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="dae42-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="dae42-127">Om-PassThru är angivet returneras ett valv objekt.</span><span class="sxs-lookup"><span data-stu-id="dae42-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="dae42-128">Exempel 2: ta bort behörigheter för ett program</span><span class="sxs-lookup"><span data-stu-id="dae42-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="dae42-129">Det här kommandot tar bort alla behörigheter som ett program har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="dae42-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="dae42-130">I det här exemplet identifieras programmet med hjälp av tjänstens huvud namn som är registrerat i Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="dae42-130">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="dae42-131">Exempel 3: ta bort behörigheter för ett program med dess objekt-ID</span><span class="sxs-lookup"><span data-stu-id="dae42-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="dae42-132">Det här kommandot tar bort alla behörigheter som ett program har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="dae42-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="dae42-133">I det här exemplet identifieras programmet av tjänstens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="dae42-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="dae42-134">Exempel 4: ta bort behörigheter för Microsoft. Compute Resource Provider</span><span class="sxs-lookup"><span data-stu-id="dae42-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="dae42-135">Det här kommandot tar bort behörigheter för Microsoft. Compute Resource Provider för att få hemligheter från Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="dae42-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="dae42-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dae42-136">PARAMETERS</span></span>

### <span data-ttu-id="dae42-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dae42-137">-ApplicationId</span></span>
<span data-ttu-id="dae42-138">Anger ID för programmet vars behörigheter ska tas bort</span><span class="sxs-lookup"><span data-stu-id="dae42-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="dae42-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae42-139">-DefaultProfile</span></span>
<span data-ttu-id="dae42-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dae42-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="dae42-141">-EmailAddress</span></span>
<span data-ttu-id="dae42-142">Anger användarens e-postadress för den användare vars åtkomst du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="dae42-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="dae42-143">-EnabledForDeployment</span></span>
<span data-ttu-id="dae42-144">Om du anger det här alternativet inaktive ras hämtning av hemligheter från det här nyckelordet av Microsoft. Compute Resource Provider när den refereras i skapa resurs.</span><span class="sxs-lookup"><span data-stu-id="dae42-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="dae42-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="dae42-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="dae42-146">Om det här alternativet anges inaktiverar hämtning av hemligheter från den här nyckeln för Azure Disk Encryption.</span><span class="sxs-lookup"><span data-stu-id="dae42-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="dae42-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="dae42-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="dae42-148">Om det här alternativet anges inaktiverar hämtning av hemligheter från det här nyckelordet av Azure Resource Manager när den refereras till i mallar.</span><span class="sxs-lookup"><span data-stu-id="dae42-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="dae42-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dae42-149">-InputObject</span></span>
<span data-ttu-id="dae42-150">Key valv-objekt.</span><span class="sxs-lookup"><span data-stu-id="dae42-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dae42-151">-ObjectId</span></span>
<span data-ttu-id="dae42-152">Anger objekt-ID: t för användaren eller tjänstens huvud namn i Azure Active Directory som du vill ta bort behörigheter för.</span><span class="sxs-lookup"><span data-stu-id="dae42-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="dae42-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dae42-153">-PassThru</span></span>
<span data-ttu-id="dae42-154">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="dae42-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dae42-155">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="dae42-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dae42-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae42-156">-ResourceGroupName</span></span>
<span data-ttu-id="dae42-157">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars åtkomst princip ändras.</span><span class="sxs-lookup"><span data-stu-id="dae42-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="dae42-158">Om det inte anges söker denna cmdlet efter det viktigaste valvet i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="dae42-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dae42-159">-ResourceId</span></span>
<span data-ttu-id="dae42-160">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="dae42-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="dae42-161">-ServicePrincipalName</span></span>
<span data-ttu-id="dae42-162">Anger huvud namnet på den tillämpning vars behörigheter du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="dae42-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="dae42-163">Ange program-ID, som också kallas klient-ID, för programmet i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dae42-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="dae42-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="dae42-164">-UserPrincipalName</span></span>
<span data-ttu-id="dae42-165">Anger användarens huvud namn för den användare vars åtkomst du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="dae42-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="dae42-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dae42-166">-VaultName</span></span>
<span data-ttu-id="dae42-167">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="dae42-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="dae42-168">Denna cmdlet tar bort behörigheter för det Key-valv som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="dae42-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae42-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dae42-169">-Confirm</span></span>
<span data-ttu-id="dae42-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dae42-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae42-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae42-171">-WhatIf</span></span>
<span data-ttu-id="dae42-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dae42-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dae42-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dae42-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae42-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae42-174">CommonParameters</span></span>
<span data-ttu-id="dae42-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dae42-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae42-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dae42-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae42-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dae42-177">INPUTS</span></span>

### <span data-ttu-id="dae42-178">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="dae42-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="dae42-179">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dae42-179">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="dae42-180">System. String</span><span class="sxs-lookup"><span data-stu-id="dae42-180">System.String</span></span>

## <span data-ttu-id="dae42-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dae42-181">OUTPUTS</span></span>

### <span data-ttu-id="dae42-182">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="dae42-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="dae42-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dae42-183">NOTES</span></span>

## <span data-ttu-id="dae42-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dae42-184">RELATED LINKS</span></span>

[<span data-ttu-id="dae42-185">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dae42-185">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

