---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 959fcab661139a1cacae46a315db0eaa93f0c09e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754089"
---
# <span data-ttu-id="48049-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="48049-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="48049-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48049-102">SYNOPSIS</span></span>
<span data-ttu-id="48049-103">Lägga till en enda IPrule i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="48049-103">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="48049-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48049-104">SYNTAX</span></span>

### <span data-ttu-id="48049-105">IPRulePropertiesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="48049-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48049-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48049-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48049-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48049-107">DESCRIPTION</span></span>
<span data-ttu-id="48049-108">Lägga till en enda IPrule i NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="48049-108">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="48049-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48049-109">EXAMPLES</span></span>

### <span data-ttu-id="48049-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="48049-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="48049-111">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default typ: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="48049-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="48049-112">Lägg till IPRule med IpMask "11.22.33.44" och åtgärden tillåter angiven namesapce.</span><span class="sxs-lookup"><span data-stu-id="48049-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namesapce.</span></span>

### <span data-ttu-id="48049-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="48049-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="48049-114">Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default typ: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="48049-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="48049-115">Lägg till IPRule med IpMask "11.22.33.44" och åtgärden tillåter angiven namesapce.</span><span class="sxs-lookup"><span data-stu-id="48049-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namesapce.</span></span>

## <span data-ttu-id="48049-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48049-116">PARAMETERS</span></span>

### <span data-ttu-id="48049-117">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="48049-117">-Action</span></span>
<span data-ttu-id="48049-118">Åtgärden IP filter</span><span class="sxs-lookup"><span data-stu-id="48049-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="48049-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48049-119">-DefaultProfile</span></span>
<span data-ttu-id="48049-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48049-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48049-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="48049-121">-IpMask</span></span>
<span data-ttu-id="48049-122">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="48049-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="48049-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="48049-123">-IpRuleObject</span></span>
<span data-ttu-id="48049-124">IPRule-konfigurations objekt som ska läggas till</span><span class="sxs-lookup"><span data-stu-id="48049-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48049-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="48049-125">-Name</span></span>
<span data-ttu-id="48049-126">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="48049-126">Namespace Name</span></span>

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

### <span data-ttu-id="48049-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48049-127">-ResourceGroupName</span></span>
<span data-ttu-id="48049-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="48049-128">Resource Group Name</span></span>

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

### <span data-ttu-id="48049-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48049-129">-Confirm</span></span>
<span data-ttu-id="48049-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48049-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48049-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48049-131">-WhatIf</span></span>
<span data-ttu-id="48049-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48049-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48049-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48049-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48049-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48049-134">CommonParameters</span></span>
<span data-ttu-id="48049-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48049-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="48049-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48049-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48049-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48049-137">INPUTS</span></span>

### <span data-ttu-id="48049-138">System. String</span><span class="sxs-lookup"><span data-stu-id="48049-138">System.String</span></span>

### <span data-ttu-id="48049-139">Microsoft. Azure. commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="48049-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="48049-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48049-140">OUTPUTS</span></span>

### <span data-ttu-id="48049-141">Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="48049-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="48049-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48049-142">NOTES</span></span>

## <span data-ttu-id="48049-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48049-143">RELATED LINKS</span></span>