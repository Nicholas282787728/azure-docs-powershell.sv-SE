---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: df7cf094482f849782d6570b0df1af8cbadb7077
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746944"
---
# <span data-ttu-id="dbaf2-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="dbaf2-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="dbaf2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="dbaf2-103">Lägga till en enda IPrule i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="dbaf2-103">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="dbaf2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbaf2-104">SYNTAX</span></span>

### <span data-ttu-id="dbaf2-105">IPRulePropertiesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dbaf2-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbaf2-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbaf2-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbaf2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbaf2-107">DESCRIPTION</span></span>
<span data-ttu-id="dbaf2-108">Lägga till en enda IPrule i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="dbaf2-108">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="dbaf2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbaf2-109">EXAMPLES</span></span>

### <span data-ttu-id="dbaf2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dbaf2-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="dbaf2-111">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="dbaf2-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="dbaf2-112">Lägg till IPRule med IpMask "11.22.33.44" och åtgärden tillåter från givet namesapce.</span><span class="sxs-lookup"><span data-stu-id="dbaf2-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namesapce.</span></span>

### <span data-ttu-id="dbaf2-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dbaf2-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="dbaf2-114">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="dbaf2-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="dbaf2-115">Lägg till IPRule med IpMask "11.22.33.44" och åtgärden tillåter från givet namesapce.</span><span class="sxs-lookup"><span data-stu-id="dbaf2-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namesapce.</span></span>

## <span data-ttu-id="dbaf2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbaf2-116">PARAMETERS</span></span>

### <span data-ttu-id="dbaf2-117">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="dbaf2-117">-Action</span></span>
<span data-ttu-id="dbaf2-118">Åtgärden IP filter</span><span class="sxs-lookup"><span data-stu-id="dbaf2-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbaf2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbaf2-119">-DefaultProfile</span></span>
<span data-ttu-id="dbaf2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dbaf2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbaf2-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="dbaf2-121">-IpMask</span></span>
<span data-ttu-id="dbaf2-122">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="dbaf2-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbaf2-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="dbaf2-123">-IpRuleObject</span></span>
<span data-ttu-id="dbaf2-124">IPRule-konfigurations objekt som ska läggas till</span><span class="sxs-lookup"><span data-stu-id="dbaf2-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbaf2-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="dbaf2-125">-Name</span></span>
<span data-ttu-id="dbaf2-126">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="dbaf2-126">Namespace Name</span></span>

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

### <span data-ttu-id="dbaf2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbaf2-127">-ResourceGroupName</span></span>
<span data-ttu-id="dbaf2-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="dbaf2-128">Resource Group Name</span></span>

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

### <span data-ttu-id="dbaf2-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dbaf2-129">-Confirm</span></span>
<span data-ttu-id="dbaf2-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dbaf2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbaf2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbaf2-131">-WhatIf</span></span>
<span data-ttu-id="dbaf2-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dbaf2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbaf2-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dbaf2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbaf2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbaf2-134">CommonParameters</span></span>
<span data-ttu-id="dbaf2-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbaf2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dbaf2-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbaf2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbaf2-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbaf2-137">INPUTS</span></span>

### <span data-ttu-id="dbaf2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dbaf2-138">System.String</span></span>

### <span data-ttu-id="dbaf2-139">Microsoft. Azure. commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="dbaf2-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="dbaf2-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbaf2-140">OUTPUTS</span></span>

### <span data-ttu-id="dbaf2-141">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="dbaf2-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="dbaf2-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbaf2-142">NOTES</span></span>

## <span data-ttu-id="dbaf2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbaf2-143">RELATED LINKS</span></span>