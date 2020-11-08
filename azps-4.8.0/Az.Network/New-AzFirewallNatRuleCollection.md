---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 4ba57fd922319eb2be6ba001c723b3e668bce59e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262574"
---
# <span data-ttu-id="0efcd-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0efcd-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="0efcd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0efcd-102">SYNOPSIS</span></span>
<span data-ttu-id="0efcd-103">Skapar en samling NAT-regler.</span><span class="sxs-lookup"><span data-stu-id="0efcd-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="0efcd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0efcd-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0efcd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0efcd-105">DESCRIPTION</span></span>
<span data-ttu-id="0efcd-106">Cmdleten **New-AzFirewallNatRuleCollection** skapar en samling NAT-regler.</span><span class="sxs-lookup"><span data-stu-id="0efcd-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="0efcd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0efcd-107">EXAMPLES</span></span>

### <span data-ttu-id="0efcd-108">Exempel 1: skapa en samling med en regel</span><span class="sxs-lookup"><span data-stu-id="0efcd-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="0efcd-109">I det här exemplet skapas en samling med en regel.</span><span class="sxs-lookup"><span data-stu-id="0efcd-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="0efcd-110">All trafik som matchar villkoren i $rule 1 kommer att vara DNAT'ed till översatt adress och port.</span><span class="sxs-lookup"><span data-stu-id="0efcd-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="0efcd-111">Exempel 2: lägga till en regel i en regel samling</span><span class="sxs-lookup"><span data-stu-id="0efcd-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="0efcd-112">I det här exemplet skapas en ny NAT-regel med en regel och därefter läggs en andra regel till i regel samlingen med metoden AddRule på regeln Collection-objektet.</span><span class="sxs-lookup"><span data-stu-id="0efcd-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="0efcd-113">Varje regel namn i en viss regel samling måste ha ett unikt namn och är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="0efcd-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="0efcd-114">Exempel 3: Hämta en regel från en regel samling</span><span class="sxs-lookup"><span data-stu-id="0efcd-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="0efcd-115">Det här exemplet skapar en ny NAT-regel med en regel och hämtar sedan regeln efter namn, som anropar metoden GetRuleByName på principobjektet.</span><span class="sxs-lookup"><span data-stu-id="0efcd-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="0efcd-116">Regel namnet för metod GetRuleByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="0efcd-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="0efcd-117">Exempel 4: ta bort en regel från en regel samling</span><span class="sxs-lookup"><span data-stu-id="0efcd-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="0efcd-118">Det här exemplet skapar en ny NAT-regel med två regler och tar sedan bort den första regeln från regel samlingen genom att anropa metoden RemoveRuleByName på regeln.</span><span class="sxs-lookup"><span data-stu-id="0efcd-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="0efcd-119">Regel namnet för metod RemoveRuleByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="0efcd-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="0efcd-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0efcd-120">PARAMETERS</span></span>

### <span data-ttu-id="0efcd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efcd-121">-DefaultProfile</span></span>
<span data-ttu-id="0efcd-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0efcd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0efcd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0efcd-123">-Name</span></span>
<span data-ttu-id="0efcd-124">Anger namnet på denna NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="0efcd-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="0efcd-125">Namnet måste vara unikt i en regel samling.</span><span class="sxs-lookup"><span data-stu-id="0efcd-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="0efcd-126">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="0efcd-126">-Priority</span></span>
<span data-ttu-id="0efcd-127">Anger prioriteten för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="0efcd-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="0efcd-128">Prioritet är ett tal mellan 100 och 65000.</span><span class="sxs-lookup"><span data-stu-id="0efcd-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="0efcd-129">Ju mindre siffran desto större prioritet.</span><span class="sxs-lookup"><span data-stu-id="0efcd-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="0efcd-130">-Regel</span><span class="sxs-lookup"><span data-stu-id="0efcd-130">-Rule</span></span>
<span data-ttu-id="0efcd-131">Anger listan över regler som ska grupperas under den här samlingen.</span><span class="sxs-lookup"><span data-stu-id="0efcd-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0efcd-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0efcd-132">-Confirm</span></span>
<span data-ttu-id="0efcd-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0efcd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efcd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efcd-134">-WhatIf</span></span>
<span data-ttu-id="0efcd-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0efcd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0efcd-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0efcd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efcd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efcd-137">CommonParameters</span></span>
<span data-ttu-id="0efcd-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efcd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efcd-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0efcd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efcd-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0efcd-140">INPUTS</span></span>

### <span data-ttu-id="0efcd-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="0efcd-141">None</span></span>

## <span data-ttu-id="0efcd-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0efcd-142">OUTPUTS</span></span>

### <span data-ttu-id="0efcd-143">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0efcd-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="0efcd-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0efcd-144">NOTES</span></span>

## <span data-ttu-id="0efcd-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0efcd-145">RELATED LINKS</span></span>

[<span data-ttu-id="0efcd-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="0efcd-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="0efcd-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0efcd-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="0efcd-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0efcd-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
