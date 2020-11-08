---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: a11e962e2af6beaa3f3004cec104530f7603bb3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259462"
---
# <span data-ttu-id="f9547-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9547-101">New-AzKeyVault</span></span>

## <span data-ttu-id="f9547-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9547-102">SYNOPSIS</span></span>
<span data-ttu-id="f9547-103">Skapar ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="f9547-103">Creates a key vault.</span></span>

## <span data-ttu-id="f9547-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9547-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-DisableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9547-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9547-105">DESCRIPTION</span></span>
<span data-ttu-id="f9547-106">Cmdleten **New-AzKeyVault** skapar ett huvud valv i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f9547-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="f9547-107">Denna cmdlet beviljar också behörigheter till den inloggade användaren för att lägga till, ta bort eller lista nycklar och hemligheter i nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="f9547-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="f9547-108">Obs! Om du får ett fel meddelande om **att prenumerationen inte är registrerad för att använda namn området ' Microsoft. Key valv '** när du försöker skapa ett nytt Key-valv kör du **register-AzResourceProvider-ProviderNamespace "Microsoft. Key Vault"** och kör sedan kommandot **ny-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="f9547-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="f9547-109">Mer information finns i registrera-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="f9547-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="f9547-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9547-110">EXAMPLES</span></span>

### <span data-ttu-id="f9547-111">Exempel 1: skapa ett standard nyckeltal</span><span class="sxs-lookup"><span data-stu-id="f9547-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="f9547-112">Det här kommandot skapar ett nyckelord med namnet Contoso03Vault i Azure-regionen öst.</span><span class="sxs-lookup"><span data-stu-id="f9547-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="f9547-113">Kommandot lägger till Key Vault i resurs gruppen med namnet Group14.</span><span class="sxs-lookup"><span data-stu-id="f9547-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="f9547-114">Eftersom kommandot inte anger ett värde för parametern *SKU* skapar det ett standard-Key-valv.</span><span class="sxs-lookup"><span data-stu-id="f9547-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="f9547-115">Exempel 2: skapa ett Premium Key-valv</span><span class="sxs-lookup"><span data-stu-id="f9547-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="f9547-116">Det här kommandot skapar ett nyckeltal, precis som i föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="f9547-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="f9547-117">Men det anger ett Premium-värde för parametern *SKU* för att skapa ett Premium Key-valv.</span><span class="sxs-lookup"><span data-stu-id="f9547-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="f9547-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="f9547-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="f9547-119">Skapa ett nyckelord och ange nätverks regler för att tillåta åtkomst till angiven IP-adress från det virtuella nätverk som identifieras av $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="f9547-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="f9547-120">Mer `New-AzKeyVaultNetworkRuleSetObject` information finns i.</span><span class="sxs-lookup"><span data-stu-id="f9547-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="f9547-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9547-121">PARAMETERS</span></span>

### <span data-ttu-id="f9547-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9547-122">-DefaultProfile</span></span>
<span data-ttu-id="f9547-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f9547-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9547-124">-DisableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="f9547-124">-DisableSoftDelete</span></span>
<span data-ttu-id="f9547-125">Om det här alternativet anges är funktionen "mjuk borttagning" inaktive rad för detta nyckeltal.</span><span class="sxs-lookup"><span data-stu-id="f9547-125">If specified, 'soft delete' functionality is disabled for this key vault.</span></span>

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

### <span data-ttu-id="f9547-126">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="f9547-126">-EnabledForDeployment</span></span>
<span data-ttu-id="f9547-127">Gör det möjligt för Microsoft. Compute Resource-leverantören att hämta hemligheter från det här nyckelvärdet när det här nyckelvärdet refereras i resurs skapande, till exempel när du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f9547-127">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="f9547-128">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f9547-128">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="f9547-129">Aktiverar tjänsten Azure Disk Encryption för att få hemligheter och unwrap-nycklar från det här nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="f9547-129">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="f9547-130">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="f9547-130">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="f9547-131">Gör det möjligt för Azure Resource Manager att få hemligheter från detta viktiga valv när det här nyckelvärdet refereras till i en mall.</span><span class="sxs-lookup"><span data-stu-id="f9547-131">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="f9547-132">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="f9547-132">-EnablePurgeProtection</span></span>
<span data-ttu-id="f9547-133">Om det anges är skyddet mot omedelbar borttagning aktiverat för det här valvet. kräver att mjuka Delete är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="f9547-133">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="f9547-134">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="f9547-134">-EnableRbacAuthorization</span></span>
<span data-ttu-id="f9547-135">Om du anger det här alternativet aktiverar du data åtgärder via RBAC (rollbaserad åtkomst kontroll) och sedan kommer de åtkomst principer som angetts i valv egenskaperna att ignoreras.</span><span class="sxs-lookup"><span data-stu-id="f9547-135">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="f9547-136">Observera att hanterings åtgärder alltid är auktoriserade med RBAC.</span><span class="sxs-lookup"><span data-stu-id="f9547-136">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="f9547-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="f9547-137">-Location</span></span>
<span data-ttu-id="f9547-138">Anger det Azure-område där du vill skapa huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="f9547-138">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="f9547-139">Använd kommandot [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) för att se dina val.</span><span class="sxs-lookup"><span data-stu-id="f9547-139">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="f9547-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9547-140">-Name</span></span>
<span data-ttu-id="f9547-141">Anger ett namn på det Key Vault som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f9547-141">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="f9547-142">Namnet kan vara en kombination av bokstäver, siffror och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="f9547-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="f9547-143">Namnet måste börja och sluta med en bokstav eller en siffra.</span><span class="sxs-lookup"><span data-stu-id="f9547-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="f9547-144">Namnet måste vara globalt unikt.</span><span class="sxs-lookup"><span data-stu-id="f9547-144">The name must be universally unique.</span></span>

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

### <span data-ttu-id="f9547-145">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9547-145">-NetworkRuleSet</span></span>
<span data-ttu-id="f9547-146">Anger nätverkets regel uppsättning för valvet.</span><span class="sxs-lookup"><span data-stu-id="f9547-146">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="f9547-147">Den styr tillgängligheten för viktiga valv från specifika nätverks platser.</span><span class="sxs-lookup"><span data-stu-id="f9547-147">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="f9547-148">Skapad av `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="f9547-148">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="f9547-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9547-149">-ResourceGroupName</span></span>
<span data-ttu-id="f9547-150">Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f9547-150">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="f9547-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="f9547-151">-Sku</span></span>
<span data-ttu-id="f9547-152">Anger SKU för Key valv-instansen.</span><span class="sxs-lookup"><span data-stu-id="f9547-152">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="f9547-153">Information om vilka funktioner som är tillgängliga för varje SKU finns på webbplatsen för Azure Key Vault prissättning ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="f9547-153">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9547-154">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f9547-154">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="f9547-155">Anger hur länge borttagna resurser behålls och hur länge ett valv eller ett objekt i det borttagna läget kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="f9547-155">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="f9547-156">Standardvärdet är 90 dagar.</span><span class="sxs-lookup"><span data-stu-id="f9547-156">The default is 90 days.</span></span>

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

### <span data-ttu-id="f9547-157">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f9547-157">-Tag</span></span>
<span data-ttu-id="f9547-158">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f9547-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f9547-159">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f9547-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f9547-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f9547-160">-Confirm</span></span>
<span data-ttu-id="f9547-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f9547-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9547-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9547-162">-WhatIf</span></span>
<span data-ttu-id="f9547-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f9547-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9547-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f9547-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9547-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9547-165">CommonParameters</span></span>
<span data-ttu-id="f9547-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9547-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9547-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9547-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9547-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9547-168">INPUTS</span></span>

### <span data-ttu-id="f9547-169">System. String</span><span class="sxs-lookup"><span data-stu-id="f9547-169">System.String</span></span>

### <span data-ttu-id="f9547-170">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9547-170">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f9547-171">Microsoft. Azure. Management. valv. SkuName</span><span class="sxs-lookup"><span data-stu-id="f9547-171">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="f9547-172">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f9547-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f9547-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9547-173">OUTPUTS</span></span>

### <span data-ttu-id="f9547-174">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9547-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f9547-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9547-175">NOTES</span></span>

## <span data-ttu-id="f9547-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9547-176">RELATED LINKS</span></span>

[<span data-ttu-id="f9547-177">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9547-177">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="f9547-178">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9547-178">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
