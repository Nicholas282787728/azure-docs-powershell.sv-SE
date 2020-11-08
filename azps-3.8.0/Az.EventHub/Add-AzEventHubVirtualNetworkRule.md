---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090590"
---
# <span data-ttu-id="9b247-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9b247-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="9b247-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b247-102">SYNOPSIS</span></span>
<span data-ttu-id="9b247-103">Lägga till en enda VirtualNetworkRule i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="9b247-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="9b247-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b247-104">SYNTAX</span></span>

### <span data-ttu-id="9b247-105">VirtualNetworkRulePropertiesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9b247-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b247-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b247-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b247-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b247-107">DESCRIPTION</span></span>
<span data-ttu-id="9b247-108">Lägga till en enda VirtualNetworkRule i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="9b247-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="9b247-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b247-109">EXAMPLES</span></span>

### <span data-ttu-id="9b247-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b247-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="9b247-111">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default typ: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="9b247-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="9b247-112">Lägger till givet undernät och IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="9b247-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="9b247-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9b247-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="9b247-114">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default typ: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="9b247-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="9b247-115">Lägger till $virtualruleset 1 i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="9b247-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="9b247-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b247-116">PARAMETERS</span></span>

### <span data-ttu-id="9b247-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b247-117">-DefaultProfile</span></span>
<span data-ttu-id="9b247-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b247-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b247-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b247-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="9b247-120">ARM-ID för undernät</span><span class="sxs-lookup"><span data-stu-id="9b247-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b247-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b247-121">-Name</span></span>
<span data-ttu-id="9b247-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="9b247-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b247-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b247-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b247-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9b247-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b247-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9b247-125">-SubnetId</span></span>
<span data-ttu-id="9b247-126">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="9b247-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b247-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9b247-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="9b247-128">VirtualNetworkRule-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="9b247-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b247-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b247-129">-Confirm</span></span>
<span data-ttu-id="9b247-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b247-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b247-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b247-131">-WhatIf</span></span>
<span data-ttu-id="9b247-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b247-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b247-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b247-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b247-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b247-134">CommonParameters</span></span>
<span data-ttu-id="9b247-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b247-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9b247-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b247-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b247-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b247-137">INPUTS</span></span>

### <span data-ttu-id="9b247-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9b247-138">System.String</span></span>

### <span data-ttu-id="9b247-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9b247-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9b247-140">Microsoft. Azure. commands. EventHub. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="9b247-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="9b247-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b247-141">OUTPUTS</span></span>

### <span data-ttu-id="9b247-142">Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="9b247-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="9b247-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b247-143">NOTES</span></span>

## <span data-ttu-id="9b247-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b247-144">RELATED LINKS</span></span>
