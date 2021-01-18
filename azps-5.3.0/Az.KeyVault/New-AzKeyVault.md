---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522606"
---
# <span data-ttu-id="486b2-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="486b2-101">New-AzKeyVault</span></span>

## <span data-ttu-id="486b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="486b2-102">SYNOPSIS</span></span>
<span data-ttu-id="486b2-103">Skapar ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="486b2-103">Creates a key vault.</span></span>

## <span data-ttu-id="486b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="486b2-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="486b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="486b2-105">DESCRIPTION</span></span>
<span data-ttu-id="486b2-106">Cmdleten **New-AzKeyVault** skapar ett huvud valv i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="486b2-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="486b2-107">Denna cmdlet beviljar också behörigheter till den inloggade användaren för att lägga till, ta bort eller lista nycklar och hemligheter i nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="486b2-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="486b2-108">Obs! Om du får ett fel meddelande om **att prenumerationen inte är registrerad för att använda namn området ' Microsoft. Key valv '** när du försöker skapa ett nytt Key-valv kör du **register-AzResourceProvider-ProviderNamespace "Microsoft. Key Vault"** och kör sedan kommandot **ny-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="486b2-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="486b2-109">Mer information finns i registrera-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="486b2-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="486b2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="486b2-110">EXAMPLES</span></span>

### <span data-ttu-id="486b2-111">Exempel 1: skapa ett standard nyckeltal</span><span class="sxs-lookup"><span data-stu-id="486b2-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
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
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="486b2-112">Det här kommandot skapar ett nyckelord med namnet Contoso03Vault i Azure-regionen öst.</span><span class="sxs-lookup"><span data-stu-id="486b2-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="486b2-113">Kommandot lägger till Key Vault i resurs gruppen med namnet Group14.</span><span class="sxs-lookup"><span data-stu-id="486b2-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="486b2-114">Eftersom kommandot inte anger ett värde för parametern *SKU* skapar det ett standard-Key-valv.</span><span class="sxs-lookup"><span data-stu-id="486b2-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="486b2-115">Exempel 2: skapa ett Premium Key-valv</span><span class="sxs-lookup"><span data-stu-id="486b2-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="486b2-116">Det här kommandot skapar ett nyckeltal, precis som i föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="486b2-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="486b2-117">Men det anger ett Premium-värde för parametern *SKU* för att skapa ett Premium Key-valv.</span><span class="sxs-lookup"><span data-stu-id="486b2-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="486b2-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="486b2-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="486b2-119">Skapa ett nyckelord och ange nätverks regler för att tillåta åtkomst till angiven IP-adress från det virtuella nätverk som identifieras av $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="486b2-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="486b2-120">Mer `New-AzKeyVaultNetworkRuleSetObject` information finns i.</span><span class="sxs-lookup"><span data-stu-id="486b2-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="486b2-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="486b2-121">PARAMETERS</span></span>

### <span data-ttu-id="486b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486b2-122">-DefaultProfile</span></span>
<span data-ttu-id="486b2-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="486b2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="486b2-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="486b2-124">-EnabledForDeployment</span></span>
<span data-ttu-id="486b2-125">Gör det möjligt för Microsoft. Compute Resource-leverantören att hämta hemligheter från det här nyckelvärdet när det här nyckelvärdet refereras i resurs skapande, till exempel när du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="486b2-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="486b2-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="486b2-127">Aktiverar tjänsten Azure Disk Encryption för att få hemligheter och unwrap-nycklar från det här nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="486b2-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="486b2-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="486b2-129">Gör det möjligt för Azure Resource Manager att få hemligheter från detta viktiga valv när det här nyckelvärdet refereras till i en mall.</span><span class="sxs-lookup"><span data-stu-id="486b2-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="486b2-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="486b2-131">Om det anges är skyddet mot omedelbar borttagning aktiverat för det här valvet. kräver att mjuka Delete är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="486b2-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="486b2-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="486b2-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="486b2-133">Om du anger det här alternativet aktiverar du data åtgärder via RBAC (rollbaserad åtkomst kontroll) och sedan kommer de åtkomst principer som angetts i valv egenskaperna att ignoreras.</span><span class="sxs-lookup"><span data-stu-id="486b2-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="486b2-134">Observera att hanterings åtgärder alltid är auktoriserade med RBAC.</span><span class="sxs-lookup"><span data-stu-id="486b2-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="486b2-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="486b2-135">-Location</span></span>
<span data-ttu-id="486b2-136">Anger det Azure-område där du vill skapa huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="486b2-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="486b2-137">Använd kommandot [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) för att se dina val.</span><span class="sxs-lookup"><span data-stu-id="486b2-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="486b2-138">-Name</span></span>
<span data-ttu-id="486b2-139">Anger ett namn på det Key Vault som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="486b2-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="486b2-140">Namnet kan vara en kombination av bokstäver, siffror och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="486b2-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="486b2-141">Namnet måste börja och sluta med en bokstav eller en siffra.</span><span class="sxs-lookup"><span data-stu-id="486b2-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="486b2-142">Namnet måste vara globalt unikt.</span><span class="sxs-lookup"><span data-stu-id="486b2-142">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="486b2-143">-NetworkRuleSet</span></span>
<span data-ttu-id="486b2-144">Anger nätverkets regel uppsättning för valvet.</span><span class="sxs-lookup"><span data-stu-id="486b2-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="486b2-145">Den styr tillgängligheten för viktiga valv från specifika nätverks platser.</span><span class="sxs-lookup"><span data-stu-id="486b2-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="486b2-146">Skapad av `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="486b2-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="486b2-147">-ResourceGroupName</span></span>
<span data-ttu-id="486b2-148">Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="486b2-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="486b2-149">-Sku</span></span>
<span data-ttu-id="486b2-150">Anger SKU för Key valv-instansen.</span><span class="sxs-lookup"><span data-stu-id="486b2-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="486b2-151">Information om vilka funktioner som är tillgängliga för varje SKU finns på webbplatsen för Azure Key Vault prissättning ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="486b2-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="486b2-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="486b2-153">Anger hur länge borttagna resurser behålls och hur länge ett valv eller ett objekt i det borttagna läget kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="486b2-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="486b2-154">Standardvärdet är 90 dagar.</span><span class="sxs-lookup"><span data-stu-id="486b2-154">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-155">-Tagg</span><span class="sxs-lookup"><span data-stu-id="486b2-155">-Tag</span></span>
<span data-ttu-id="486b2-156">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="486b2-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="486b2-157">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="486b2-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486b2-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="486b2-158">-Confirm</span></span>
<span data-ttu-id="486b2-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="486b2-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="486b2-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="486b2-160">-WhatIf</span></span>
<span data-ttu-id="486b2-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="486b2-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="486b2-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="486b2-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="486b2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486b2-163">CommonParameters</span></span>
<span data-ttu-id="486b2-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="486b2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486b2-165">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="486b2-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486b2-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="486b2-166">INPUTS</span></span>

### <span data-ttu-id="486b2-167">System. String</span><span class="sxs-lookup"><span data-stu-id="486b2-167">System.String</span></span>

### <span data-ttu-id="486b2-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="486b2-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="486b2-169">Microsoft. Azure. Management. valv. SkuName</span><span class="sxs-lookup"><span data-stu-id="486b2-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="486b2-170">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="486b2-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="486b2-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="486b2-171">OUTPUTS</span></span>

### <span data-ttu-id="486b2-172">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="486b2-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="486b2-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="486b2-173">NOTES</span></span>

## <span data-ttu-id="486b2-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="486b2-174">RELATED LINKS</span></span>

[<span data-ttu-id="486b2-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="486b2-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="486b2-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="486b2-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
