---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: 7eb4265042083135f8306f601e2a14818aaacb06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269409"
---
# <span data-ttu-id="05608-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="05608-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="05608-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05608-102">SYNOPSIS</span></span>
<span data-ttu-id="05608-103">Lägga till en enda IP-regel i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="05608-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="05608-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05608-104">SYNTAX</span></span>

### <span data-ttu-id="05608-105">IPRulePropertiesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="05608-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05608-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05608-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05608-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05608-107">DESCRIPTION</span></span>
<span data-ttu-id="05608-108">Lägga till en enda IP-regel i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="05608-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="05608-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05608-109">EXAMPLES</span></span>

### <span data-ttu-id="05608-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="05608-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="05608-111">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="05608-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="05608-112">Lägg till IPRule med IpMask "11.22.33.44" och åtgärden tillåter från det givna namn området.</span><span class="sxs-lookup"><span data-stu-id="05608-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="05608-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="05608-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="05608-114">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="05608-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="05608-115">Lägg till IPRule med IpMask "11.22.33.44" och åtgärden tillåter från det givna namn området.</span><span class="sxs-lookup"><span data-stu-id="05608-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="05608-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05608-116">PARAMETERS</span></span>

### <span data-ttu-id="05608-117">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="05608-117">-Action</span></span>
<span data-ttu-id="05608-118">Åtgärden IP filter</span><span class="sxs-lookup"><span data-stu-id="05608-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="05608-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05608-119">-DefaultProfile</span></span>
<span data-ttu-id="05608-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05608-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05608-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="05608-121">-IpMask</span></span>
<span data-ttu-id="05608-122">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="05608-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="05608-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="05608-123">-IpRuleObject</span></span>
<span data-ttu-id="05608-124">IPRule-konfigurations objekt som ska läggas till</span><span class="sxs-lookup"><span data-stu-id="05608-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="05608-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="05608-125">-Name</span></span>
<span data-ttu-id="05608-126">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="05608-126">Namespace Name</span></span>

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

### <span data-ttu-id="05608-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05608-127">-ResourceGroupName</span></span>
<span data-ttu-id="05608-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="05608-128">Resource Group Name</span></span>

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

### <span data-ttu-id="05608-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05608-129">-Confirm</span></span>
<span data-ttu-id="05608-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05608-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05608-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05608-131">-WhatIf</span></span>
<span data-ttu-id="05608-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05608-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05608-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05608-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05608-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05608-134">CommonParameters</span></span>
<span data-ttu-id="05608-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05608-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="05608-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05608-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05608-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05608-137">INPUTS</span></span>

### <span data-ttu-id="05608-138">System. String</span><span class="sxs-lookup"><span data-stu-id="05608-138">System.String</span></span>

### <span data-ttu-id="05608-139">Microsoft. Azure. commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="05608-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="05608-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05608-140">OUTPUTS</span></span>

### <span data-ttu-id="05608-141">Microsoft. Azure. commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="05608-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="05608-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05608-142">NOTES</span></span>

## <span data-ttu-id="05608-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05608-143">RELATED LINKS</span></span>