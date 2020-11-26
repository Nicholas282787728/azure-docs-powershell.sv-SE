---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262570"
---
# <span data-ttu-id="7d419-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7d419-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="7d419-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d419-102">SYNOPSIS</span></span>
<span data-ttu-id="7d419-103">Skapar en Azure Firewall Network-uppsättning med nätverks regler.</span><span class="sxs-lookup"><span data-stu-id="7d419-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="7d419-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d419-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d419-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d419-105">DESCRIPTION</span></span>
<span data-ttu-id="7d419-106">Cmdleten **New-AzFirewallNetworkRuleCollection** skapar en uppsättning nätverks regler för brand väggar.</span><span class="sxs-lookup"><span data-stu-id="7d419-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="7d419-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d419-107">EXAMPLES</span></span>

### <span data-ttu-id="7d419-108">Exempel 1: skapa en nätverks samling med två regler</span><span class="sxs-lookup"><span data-stu-id="7d419-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="7d419-109">I det här exemplet skapas en samling som tillåter all trafik som matchar någon av de två reglerna.</span><span class="sxs-lookup"><span data-stu-id="7d419-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="7d419-110">Den första regeln gäller för all UDP-trafik.</span><span class="sxs-lookup"><span data-stu-id="7d419-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="7d419-111">Den andra regeln gäller för TCP-trafik från 10.0.0.0 till 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="7d419-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="7d419-112">Om det finns en annan nätverks regel samling med högre prioritet (lägre nummer) som också matchar den trafik som identifieras i $rule 1 eller $rule 2, kommer åtgärden för regel samlingen med högre prioritet att träda i kraft.</span><span class="sxs-lookup"><span data-stu-id="7d419-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="7d419-113">Exempel 2: lägga till en regel i en regel samling</span><span class="sxs-lookup"><span data-stu-id="7d419-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="7d419-114">I det här exemplet skapas en ny nätverks regel samling med en regel och därefter läggs en andra regel till i regel samlingen med metoden AddRule på regeln Collection-objektet.</span><span class="sxs-lookup"><span data-stu-id="7d419-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="7d419-115">Varje regel namn i en viss regel samling måste ha ett unikt namn och är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="7d419-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="7d419-116">Exempel 3: Hämta en regel från en regel samling</span><span class="sxs-lookup"><span data-stu-id="7d419-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="7d419-117">Det här exemplet skapar en ny nätverks regel samling med en regel och hämtar sedan regeln efter namn genom att anropa metoden GetRuleByName på principobjektet.</span><span class="sxs-lookup"><span data-stu-id="7d419-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="7d419-118">Regel namnet för metod GetRuleByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="7d419-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="7d419-119">Exempel 4: ta bort en regel från en regel samling</span><span class="sxs-lookup"><span data-stu-id="7d419-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="7d419-120">Det här exemplet skapar en ny regel samling med två regler och tar sedan bort den första regeln från regel samlingen genom att anropa metoden RemoveRuleByName på regeln.</span><span class="sxs-lookup"><span data-stu-id="7d419-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="7d419-121">Regel namnet för metod RemoveRuleByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="7d419-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="7d419-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d419-122">PARAMETERS</span></span>

### <span data-ttu-id="7d419-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="7d419-123">-ActionType</span></span>
<span data-ttu-id="7d419-124">Anger vilken åtgärd som ska vidtas för trafik matchnings villkoren för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="7d419-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="7d419-125">Accepterade åtgärder är "Tillåt" eller "Neka".</span><span class="sxs-lookup"><span data-stu-id="7d419-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d419-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d419-126">-DefaultProfile</span></span>
<span data-ttu-id="7d419-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d419-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d419-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d419-128">-Name</span></span>
<span data-ttu-id="7d419-129">Anger namnet på den här nätverks regel samlingen.</span><span class="sxs-lookup"><span data-stu-id="7d419-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="7d419-130">Namnet måste vara unikt i alla nätverks regel samlingar.</span><span class="sxs-lookup"><span data-stu-id="7d419-130">The name must be unique across all network rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d419-131">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="7d419-131">-Priority</span></span>
<span data-ttu-id="7d419-132">Anger prioriteten för regel samlingen.</span><span class="sxs-lookup"><span data-stu-id="7d419-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="7d419-133">Prioritet är ett tal mellan 100 och 65000.</span><span class="sxs-lookup"><span data-stu-id="7d419-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="7d419-134">Ju mindre siffran desto högre prioritet.</span><span class="sxs-lookup"><span data-stu-id="7d419-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d419-135">-Regel</span><span class="sxs-lookup"><span data-stu-id="7d419-135">-Rule</span></span>
<span data-ttu-id="7d419-136">Anger listan över regler som ska grupperas under den här samlingen.</span><span class="sxs-lookup"><span data-stu-id="7d419-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d419-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d419-137">-Confirm</span></span>
<span data-ttu-id="7d419-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d419-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d419-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d419-139">-WhatIf</span></span>
<span data-ttu-id="7d419-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d419-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d419-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d419-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d419-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d419-142">CommonParameters</span></span>
<span data-ttu-id="7d419-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d419-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d419-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d419-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d419-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d419-145">INPUTS</span></span>

### <span data-ttu-id="7d419-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="7d419-146">None</span></span>

## <span data-ttu-id="7d419-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d419-147">OUTPUTS</span></span>

### <span data-ttu-id="7d419-148">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7d419-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="7d419-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d419-149">NOTES</span></span>

## <span data-ttu-id="7d419-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d419-150">RELATED LINKS</span></span>

[<span data-ttu-id="7d419-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7d419-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="7d419-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7d419-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="7d419-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7d419-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)