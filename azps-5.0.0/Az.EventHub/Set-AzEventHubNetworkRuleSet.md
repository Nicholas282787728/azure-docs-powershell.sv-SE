---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263183"
---
# <span data-ttu-id="dcf30-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcf30-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="dcf30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dcf30-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf30-103">Uppdatera NetworkruleSet för det angivna namn området i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dcf30-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="dcf30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dcf30-104">SYNTAX</span></span>

### <span data-ttu-id="dcf30-105">NetworkRuleSetPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dcf30-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf30-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dcf30-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcf30-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcf30-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcf30-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dcf30-108">DESCRIPTION</span></span>
<span data-ttu-id="dcf30-109">Uppdatera NetworkruleSet för det angivna namn området i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dcf30-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="dcf30-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dcf30-110">EXAMPLES</span></span>

### <span data-ttu-id="dcf30-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dcf30-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="dcf30-112">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="dcf30-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="dcf30-113">Uppdatera NetworkRuleSet med-IPRule och-VirtualNetworkRule-parametrar</span><span class="sxs-lookup"><span data-stu-id="dcf30-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="dcf30-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dcf30-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="dcf30-115">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="dcf30-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="dcf30-116">Uppdatera NetworkRuleSet med-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcf30-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="dcf30-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="dcf30-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="dcf30-118">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="dcf30-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="dcf30-119">Uppdatera NetworkRuleSet med-ResourceId för det andra namn området.</span><span class="sxs-lookup"><span data-stu-id="dcf30-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="dcf30-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dcf30-120">PARAMETERS</span></span>

### <span data-ttu-id="dcf30-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="dcf30-121">-DefaultAction</span></span>
<span data-ttu-id="dcf30-122">Standard åtgärd för NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcf30-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf30-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf30-123">-DefaultProfile</span></span>
<span data-ttu-id="dcf30-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf30-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf30-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcf30-125">-InputObject</span></span>
<span data-ttu-id="dcf30-126">NetworkruleSet-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="dcf30-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf30-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="dcf30-127">-IPRule</span></span>
<span data-ttu-id="dcf30-128">Lista över IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcf30-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf30-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="dcf30-129">-Name</span></span>
<span data-ttu-id="dcf30-130">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="dcf30-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf30-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf30-131">-ResourceGroupName</span></span>
<span data-ttu-id="dcf30-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="dcf30-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf30-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcf30-133">-ResourceId</span></span>
<span data-ttu-id="dcf30-134">Resurs-ID för namn området</span><span class="sxs-lookup"><span data-stu-id="dcf30-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf30-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="dcf30-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="dcf30-136">Anger om TrustedServiceAccessEnabled är aktiverat</span><span class="sxs-lookup"><span data-stu-id="dcf30-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf30-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dcf30-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="dcf30-138">Lista över VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="dcf30-138">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf30-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dcf30-139">-Confirm</span></span>
<span data-ttu-id="dcf30-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dcf30-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf30-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf30-141">-WhatIf</span></span>
<span data-ttu-id="dcf30-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dcf30-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcf30-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dcf30-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf30-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf30-144">CommonParameters</span></span>
<span data-ttu-id="dcf30-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf30-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dcf30-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf30-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf30-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dcf30-147">INPUTS</span></span>

### <span data-ttu-id="dcf30-148">Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="dcf30-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="dcf30-149">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf30-149">System.String</span></span>

## <span data-ttu-id="dcf30-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dcf30-150">OUTPUTS</span></span>

### <span data-ttu-id="dcf30-151">Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="dcf30-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="dcf30-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dcf30-152">NOTES</span></span>

## <span data-ttu-id="dcf30-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dcf30-153">RELATED LINKS</span></span>