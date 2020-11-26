---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: 6d264ff7e2f12777845edbf2d56cae3d8b59ddb0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259419"
---
# <span data-ttu-id="c3e6e-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3e6e-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="c3e6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e6e-103">Uppdaterar nätverks regeln som är inställd på ett Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="c3e6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3e6e-104">SYNTAX</span></span>

### <span data-ttu-id="c3e6e-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="c3e6e-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3e6e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3e6e-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3e6e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3e6e-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e6e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3e6e-108">DESCRIPTION</span></span>
<span data-ttu-id="c3e6e-109">Kommandot **Update-AzKeyVaultNetworkRuleSet** uppdaterar de nätverks regler som tillämpas på det angivna Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="c3e6e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3e6e-110">EXAMPLES</span></span>

### <span data-ttu-id="c3e6e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c3e6e-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
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


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="c3e6e-112">Det här kommandot uppdaterar nätverks-ruleset för valvet med namnet "för valv" för det angivna IP-adressintervallet och det virtuella nätverket, vilket möjliggör förbikoppling av nätverks regeln för Azure-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="c3e6e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c3e6e-113">Example 2</span></span>

<span data-ttu-id="c3e6e-114">Uppdaterar nätverks regeln som är inställd på ett Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="c3e6e-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="c3e6e-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="c3e6e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3e6e-116">PARAMETERS</span></span>

### <span data-ttu-id="c3e6e-117">-Kringgå</span><span class="sxs-lookup"><span data-stu-id="c3e6e-117">-Bypass</span></span>
<span data-ttu-id="c3e6e-118">Anger kringgående av nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-118">Specifies bypass of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum]
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6e-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="c3e6e-119">-DefaultAction</span></span>
<span data-ttu-id="c3e6e-120">Anger standard åtgärd för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-120">Specifies default action of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum]
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e6e-121">-DefaultProfile</span></span>
<span data-ttu-id="c3e6e-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e6e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3e6e-123">-InputObject</span></span>
<span data-ttu-id="c3e6e-124">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="c3e6e-124">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6e-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="c3e6e-125">-IpAddressRange</span></span>
<span data-ttu-id="c3e6e-126">Anger tillåtet nätverks-IP-adressintervall för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-126">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3e6e-127">-PassThru</span></span>
<span data-ttu-id="c3e6e-128">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c3e6e-129">Om den här växeln är angiven returneras det uppdaterade nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="c3e6e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e6e-130">-ResourceGroupName</span></span>
<span data-ttu-id="c3e6e-131">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3e6e-132">-ResourceId</span></span>
<span data-ttu-id="c3e6e-133">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="c3e6e-133">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6e-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c3e6e-134">-VaultName</span></span>
<span data-ttu-id="c3e6e-135">Anger namnet på ett huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6e-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="c3e6e-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="c3e6e-137">Anger tillåtet virtuellt nätverks-ID för nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6e-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3e6e-138">-Confirm</span></span>
<span data-ttu-id="c3e6e-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e6e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e6e-140">-WhatIf</span></span>
<span data-ttu-id="c3e6e-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e6e-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e6e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e6e-143">CommonParameters</span></span>
<span data-ttu-id="c3e6e-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e6e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e6e-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3e6e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e6e-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3e6e-146">INPUTS</span></span>

### <span data-ttu-id="c3e6e-147">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c3e6e-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c3e6e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c3e6e-148">System.String</span></span>

### <span data-ttu-id="c3e6e-149">System. Nullable ' 1 [[Microsoft. Azure. commands. publicKeyToken. PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft. Azure. PowerShell. cmdletar. valv, version = 1.0.0.0, Culture = neutral, = null]]</span><span class="sxs-lookup"><span data-stu-id="c3e6e-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c3e6e-150">System. Nullable ' 1 [[Microsoft. Azure. commands. publicKeyToken. PSKeyVaultNetworkRuleBypassEnum, Microsoft. Azure. PowerShell. cmdletar. valv, version = 1.0.0.0, Culture = neutral, = null]]</span><span class="sxs-lookup"><span data-stu-id="c3e6e-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c3e6e-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3e6e-151">OUTPUTS</span></span>

### <span data-ttu-id="c3e6e-152">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c3e6e-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="c3e6e-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3e6e-153">NOTES</span></span>

## <span data-ttu-id="c3e6e-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3e6e-154">RELATED LINKS</span></span>