---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 3ff1f64bf65a4474dc9f47aa6bd419c442b49698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091489"
---
# <span data-ttu-id="75a16-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="75a16-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="75a16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75a16-102">SYNOPSIS</span></span>
<span data-ttu-id="75a16-103">Lägga till en enda VirtualNetworkRule i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="75a16-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="75a16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75a16-104">SYNTAX</span></span>

### <span data-ttu-id="75a16-105">VirtualNetworkRulePropertiesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="75a16-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75a16-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a16-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75a16-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75a16-107">DESCRIPTION</span></span>
<span data-ttu-id="75a16-108">Lägga till en enda VirtualNetworkRule i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="75a16-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="75a16-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75a16-109">EXAMPLES</span></span>

### <span data-ttu-id="75a16-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="75a16-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="75a16-111">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="75a16-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="75a16-112">Lägger till givet undernät och IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="75a16-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="75a16-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="75a16-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="75a16-114">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="75a16-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="75a16-115">Lägger till $virtualruleset 1 i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="75a16-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="75a16-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75a16-116">PARAMETERS</span></span>

### <span data-ttu-id="75a16-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a16-117">-DefaultProfile</span></span>
<span data-ttu-id="75a16-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75a16-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a16-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="75a16-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="75a16-120">ARM-ID för undernät</span><span class="sxs-lookup"><span data-stu-id="75a16-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="75a16-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="75a16-121">-Name</span></span>
<span data-ttu-id="75a16-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="75a16-122">Namespace Name</span></span>

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

### <span data-ttu-id="75a16-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a16-123">-ResourceGroupName</span></span>
<span data-ttu-id="75a16-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="75a16-124">Resource Group Name</span></span>

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

### <span data-ttu-id="75a16-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="75a16-125">-SubnetId</span></span>
<span data-ttu-id="75a16-126">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="75a16-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="75a16-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="75a16-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="75a16-128">VirtualNetworkRule-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="75a16-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a16-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75a16-129">-Confirm</span></span>
<span data-ttu-id="75a16-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75a16-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75a16-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a16-131">-WhatIf</span></span>
<span data-ttu-id="75a16-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75a16-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75a16-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75a16-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75a16-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a16-134">CommonParameters</span></span>
<span data-ttu-id="75a16-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a16-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="75a16-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a16-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a16-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75a16-137">INPUTS</span></span>

### <span data-ttu-id="75a16-138">System. String</span><span class="sxs-lookup"><span data-stu-id="75a16-138">System.String</span></span>

### <span data-ttu-id="75a16-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="75a16-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="75a16-140">Microsoft. Azure. commands. ServiceBus. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="75a16-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="75a16-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75a16-141">OUTPUTS</span></span>

### <span data-ttu-id="75a16-142">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="75a16-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="75a16-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75a16-143">NOTES</span></span>

## <span data-ttu-id="75a16-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75a16-144">RELATED LINKS</span></span>