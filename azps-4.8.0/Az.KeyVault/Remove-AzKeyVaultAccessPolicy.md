---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e084894c26cee1a619f418437986593fe86876bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102823"
---
# <span data-ttu-id="33465-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33465-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="33465-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33465-102">SYNOPSIS</span></span>
<span data-ttu-id="33465-103">Tar bort alla behörigheter för en användare eller ett program från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="33465-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="33465-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33465-104">SYNTAX</span></span>

### <span data-ttu-id="33465-105">ByUserPrincipalName (standard)</span><span class="sxs-lookup"><span data-stu-id="33465-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="33465-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33465-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="33465-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33465-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="33465-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="33465-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="33465-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="33465-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="33465-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="33465-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="33465-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="33465-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="33465-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="33465-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="33465-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33465-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="33465-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33465-120">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33465-120">DESCRIPTION</span></span>
<span data-ttu-id="33465-121">Cmdleten **Remove-AzKeyVaultAccessPolicy** tar bort alla behörigheter för en användare eller ett program eller för alla användare och program från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="33465-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="33465-122">Även om du tar bort alla behörigheter kan ägaren av Azure-prenumerationen som innehåller nyckelordet lägga till behörigheter i Key Vault.</span><span class="sxs-lookup"><span data-stu-id="33465-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="33465-123">Observera att även om resurs gruppen är valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="33465-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="33465-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33465-124">EXAMPLES</span></span>

### <span data-ttu-id="33465-125">Exempel 1: ta bort behörigheter för en användare</span><span class="sxs-lookup"><span data-stu-id="33465-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

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

<span data-ttu-id="33465-126">Det här kommandot tar bort alla behörigheter som en användare PattiFuller@contoso.com har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="33465-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="33465-127">Om-PassThru är angivet returneras ett valv objekt.</span><span class="sxs-lookup"><span data-stu-id="33465-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="33465-128">Exempel 2: ta bort behörigheter för ett program</span><span class="sxs-lookup"><span data-stu-id="33465-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="33465-129">Det här kommandot tar bort alla behörigheter som ett program har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="33465-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="33465-130">I det här exemplet identifieras programmet med hjälp av tjänstens huvud namn som är registrerat i Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="33465-130">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="33465-131">Exempel 3: ta bort behörigheter för ett program med dess objekt-ID</span><span class="sxs-lookup"><span data-stu-id="33465-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="33465-132">Det här kommandot tar bort alla behörigheter som ett program har i det nyckelord som heter Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="33465-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="33465-133">I det här exemplet identifieras programmet av tjänstens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="33465-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="33465-134">Exempel 4: ta bort behörigheter för Microsoft. Compute Resource Provider</span><span class="sxs-lookup"><span data-stu-id="33465-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="33465-135">Det här kommandot tar bort behörigheter för Microsoft. Compute Resource Provider för att få hemligheter från Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="33465-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="33465-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33465-136">PARAMETERS</span></span>

### <span data-ttu-id="33465-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="33465-137">-ApplicationId</span></span>
<span data-ttu-id="33465-138">Anger ID för programmet vars behörigheter ska tas bort</span><span class="sxs-lookup"><span data-stu-id="33465-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="33465-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33465-139">-DefaultProfile</span></span>
<span data-ttu-id="33465-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="33465-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33465-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="33465-141">-EmailAddress</span></span>
<span data-ttu-id="33465-142">Anger användarens e-postadress för den användare vars åtkomst du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="33465-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="33465-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="33465-143">-EnabledForDeployment</span></span>
<span data-ttu-id="33465-144">Om du anger det här alternativet inaktive ras hämtning av hemligheter från det här nyckelordet av Microsoft. Compute Resource Provider när den refereras i skapa resurs.</span><span class="sxs-lookup"><span data-stu-id="33465-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="33465-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="33465-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="33465-146">Om det här alternativet anges inaktiverar hämtning av hemligheter från den här nyckeln för Azure Disk Encryption.</span><span class="sxs-lookup"><span data-stu-id="33465-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="33465-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="33465-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="33465-148">Om det här alternativet anges inaktiverar hämtning av hemligheter från det här nyckelordet av Azure Resource Manager när den refereras till i mallar.</span><span class="sxs-lookup"><span data-stu-id="33465-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="33465-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33465-149">-InputObject</span></span>
<span data-ttu-id="33465-150">Key valv-objekt.</span><span class="sxs-lookup"><span data-stu-id="33465-150">Key Vault object.</span></span>

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

### <span data-ttu-id="33465-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="33465-151">-ObjectId</span></span>
<span data-ttu-id="33465-152">Anger objekt-ID: t för användaren eller tjänstens huvud namn i Azure Active Directory som du vill ta bort behörigheter för.</span><span class="sxs-lookup"><span data-stu-id="33465-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="33465-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33465-153">-PassThru</span></span>
<span data-ttu-id="33465-154">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="33465-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="33465-155">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="33465-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="33465-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33465-156">-ResourceGroupName</span></span>
<span data-ttu-id="33465-157">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars åtkomst princip ändras.</span><span class="sxs-lookup"><span data-stu-id="33465-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="33465-158">Om det inte anges söker denna cmdlet efter det viktigaste valvet i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="33465-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="33465-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33465-159">-ResourceId</span></span>
<span data-ttu-id="33465-160">Resurs-ID för valv.</span><span class="sxs-lookup"><span data-stu-id="33465-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="33465-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="33465-161">-ServicePrincipalName</span></span>
<span data-ttu-id="33465-162">Anger huvud namnet på den tillämpning vars behörigheter du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="33465-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="33465-163">Ange program-ID, som också kallas klient-ID, för programmet i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33465-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="33465-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="33465-164">-UserPrincipalName</span></span>
<span data-ttu-id="33465-165">Anger användarens huvud namn för den användare vars åtkomst du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="33465-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="33465-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="33465-166">-VaultName</span></span>
<span data-ttu-id="33465-167">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="33465-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="33465-168">Denna cmdlet tar bort behörigheter för det Key-valv som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="33465-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="33465-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33465-169">-Confirm</span></span>
<span data-ttu-id="33465-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33465-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33465-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33465-171">-WhatIf</span></span>
<span data-ttu-id="33465-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33465-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33465-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33465-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33465-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33465-174">CommonParameters</span></span>
<span data-ttu-id="33465-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33465-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33465-176">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33465-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33465-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33465-177">INPUTS</span></span>

### <span data-ttu-id="33465-178">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="33465-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="33465-179">System. String</span><span class="sxs-lookup"><span data-stu-id="33465-179">System.String</span></span>

## <span data-ttu-id="33465-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33465-180">OUTPUTS</span></span>

### <span data-ttu-id="33465-181">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="33465-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="33465-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33465-182">NOTES</span></span>

## <span data-ttu-id="33465-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33465-183">RELATED LINKS</span></span>

[<span data-ttu-id="33465-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33465-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

