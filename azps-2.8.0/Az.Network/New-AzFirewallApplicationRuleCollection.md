---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 2c88e38bba0b4242ff0b268936fbe246214d1921
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918632"
---
# <span data-ttu-id="48a05-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="48a05-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="48a05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48a05-102">SYNOPSIS</span></span>
<span data-ttu-id="48a05-103">Skapar en uppsättning regler för brand Väggs program.</span><span class="sxs-lookup"><span data-stu-id="48a05-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="48a05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48a05-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48a05-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48a05-105">DESCRIPTION</span></span>
<span data-ttu-id="48a05-106">Cmdleten **New-AzFirewallApplicationRuleCollection** skapar en samling med brand Väggs program regler.</span><span class="sxs-lookup"><span data-stu-id="48a05-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="48a05-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48a05-107">EXAMPLES</span></span>

### <span data-ttu-id="48a05-108">1: skapa en samling med en regel</span><span class="sxs-lookup"><span data-stu-id="48a05-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="48a05-109">I det här exemplet skapas en samling med en regel.</span><span class="sxs-lookup"><span data-stu-id="48a05-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="48a05-110">All trafik som matchar villkoren i $rule 1 tillåts.</span><span class="sxs-lookup"><span data-stu-id="48a05-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="48a05-111">Den första regeln gäller för all HTTPS-trafik på port 443 från 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="48a05-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="48a05-112">Om det finns en annan program regel samling med högre prioritet (lägre nummer) som också matchar den trafik som identifieras i $rule 1, kommer åtgärden för regel samlingen med högre prioritet att träda i kraft.</span><span class="sxs-lookup"><span data-stu-id="48a05-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="48a05-113">2: lägga till en regel i en regel samling</span><span class="sxs-lookup"><span data-stu-id="48a05-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="48a05-114">I det här exemplet skapas en ny program regel samling med en regel och därefter läggs en andra regel till i regel samlingen med metoden AddRule på regeln Collection-objektet.</span><span class="sxs-lookup"><span data-stu-id="48a05-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="48a05-115">Varje regel namn i en viss regel samling måste ha ett unikt namn och är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="48a05-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="48a05-116">3: Hämta en regel från en regel samling</span><span class="sxs-lookup"><span data-stu-id="48a05-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="48a05-117">I det här exemplet skapas en ny program regel samling med en regel och regeln visas efter namn, som anropar metoden GetRuleByName på principobjektet.</span><span class="sxs-lookup"><span data-stu-id="48a05-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="48a05-118">Regel namnet för metod GetRuleByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="48a05-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="48a05-119">4: ta bort en regel från en regel samling</span><span class="sxs-lookup"><span data-stu-id="48a05-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="48a05-120">Det här exemplet skapar en ny program regel samling med två regler och tar sedan bort den första regeln från regel samlingen genom att anropa metoden RemoveRuleByName på regeln.</span><span class="sxs-lookup"><span data-stu-id="48a05-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="48a05-121">Regel namnet för metod RemoveRuleByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="48a05-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="48a05-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48a05-122">PARAMETERS</span></span>

### <span data-ttu-id="48a05-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="48a05-123">-ActionType</span></span>
<span data-ttu-id="48a05-124">Åtgärden för regel samlingen</span><span class="sxs-lookup"><span data-stu-id="48a05-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="48a05-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a05-125">-DefaultProfile</span></span>
<span data-ttu-id="48a05-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48a05-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48a05-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="48a05-127">-Name</span></span>
<span data-ttu-id="48a05-128">Anger namnet på den här program regeln.</span><span class="sxs-lookup"><span data-stu-id="48a05-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="48a05-129">Namnet måste vara unikt i en regel samling.</span><span class="sxs-lookup"><span data-stu-id="48a05-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="48a05-130">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="48a05-130">-Priority</span></span>
<span data-ttu-id="48a05-131">Anger prioriteten för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="48a05-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="48a05-132">Prioritet är ett tal mellan 100 och 65000.</span><span class="sxs-lookup"><span data-stu-id="48a05-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="48a05-133">Ju mindre siffran desto större prioritet.</span><span class="sxs-lookup"><span data-stu-id="48a05-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="48a05-134">-Regel</span><span class="sxs-lookup"><span data-stu-id="48a05-134">-Rule</span></span>
<span data-ttu-id="48a05-135">Anger listan över regler som ska grupperas under den här samlingen.</span><span class="sxs-lookup"><span data-stu-id="48a05-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a05-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48a05-136">-Confirm</span></span>
<span data-ttu-id="48a05-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48a05-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48a05-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48a05-138">-WhatIf</span></span>
<span data-ttu-id="48a05-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48a05-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48a05-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48a05-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48a05-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a05-141">CommonParameters</span></span>
<span data-ttu-id="48a05-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48a05-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a05-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48a05-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a05-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48a05-144">INPUTS</span></span>

### <span data-ttu-id="48a05-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="48a05-145">None</span></span>

## <span data-ttu-id="48a05-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48a05-146">OUTPUTS</span></span>

### <span data-ttu-id="48a05-147">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="48a05-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="48a05-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48a05-148">NOTES</span></span>

## <span data-ttu-id="48a05-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48a05-149">RELATED LINKS</span></span>

[<span data-ttu-id="48a05-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="48a05-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="48a05-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="48a05-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="48a05-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="48a05-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
