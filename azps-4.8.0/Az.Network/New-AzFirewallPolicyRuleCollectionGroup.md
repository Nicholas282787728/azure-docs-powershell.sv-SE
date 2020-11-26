---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8d60b8f7ff28e6c2a4f5a177f5cad222b1a3014c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261847"
---
# <span data-ttu-id="db3ea-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="db3ea-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="db3ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="db3ea-103">Skapa en ny grupp för regel insamling för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="db3ea-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="db3ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db3ea-104">SYNTAX</span></span>

### <span data-ttu-id="db3ea-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db3ea-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db3ea-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db3ea-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db3ea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db3ea-107">DESCRIPTION</span></span>
<span data-ttu-id="db3ea-108">Cmdleten **New-AzFirewallPolicyRuleCollectionGroup** skapar en regel samlings grupp i en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="db3ea-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="db3ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db3ea-109">EXAMPLES</span></span>

### <span data-ttu-id="db3ea-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db3ea-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="db3ea-111">I det här exemplet skapas en regel samlings grupp i brand Väggs princip $fp</span><span class="sxs-lookup"><span data-stu-id="db3ea-111">This example creates a rule collection group in the firewall policy $fp</span></span>

### <span data-ttu-id="db3ea-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="db3ea-112">Example 2</span></span>

<span data-ttu-id="db3ea-113">Skapa en ny grupp för regel insamling för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="db3ea-113">Create a new Azure Firewall Policy Rule Collection Group.</span></span> <span data-ttu-id="db3ea-114">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="db3ea-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzFirewallPolicyRuleCollectionGroup -FirewallPolicyName <String> -Name rg1 -Priority 200 -ResourceGroupName TestRg
```

## <span data-ttu-id="db3ea-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db3ea-115">PARAMETERS</span></span>

### <span data-ttu-id="db3ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3ea-116">-DefaultProfile</span></span>
<span data-ttu-id="db3ea-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db3ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db3ea-118">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="db3ea-118">-FirewallPolicyName</span></span>
<span data-ttu-id="db3ea-119">Namnet på brand Väggs principen</span><span class="sxs-lookup"><span data-stu-id="db3ea-119">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ea-120">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="db3ea-120">-FirewallPolicyObject</span></span>
<span data-ttu-id="db3ea-121">Brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="db3ea-121">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ea-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="db3ea-122">-Name</span></span>
<span data-ttu-id="db3ea-123">Namnet på regel gruppen</span><span class="sxs-lookup"><span data-stu-id="db3ea-123">The name of the Rule Group</span></span>

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

### <span data-ttu-id="db3ea-124">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="db3ea-124">-Priority</span></span>
<span data-ttu-id="db3ea-125">Regel gruppens prioritet</span><span class="sxs-lookup"><span data-stu-id="db3ea-125">The priority of the rule group</span></span>

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

### <span data-ttu-id="db3ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db3ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="db3ea-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="db3ea-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ea-128">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="db3ea-128">-RuleCollection</span></span>
<span data-ttu-id="db3ea-129">Listan med regler</span><span class="sxs-lookup"><span data-stu-id="db3ea-129">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db3ea-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db3ea-130">-Confirm</span></span>
<span data-ttu-id="db3ea-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db3ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db3ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db3ea-132">-WhatIf</span></span>
<span data-ttu-id="db3ea-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db3ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db3ea-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db3ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db3ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3ea-135">CommonParameters</span></span>
<span data-ttu-id="db3ea-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db3ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3ea-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db3ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3ea-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db3ea-138">INPUTS</span></span>

### <span data-ttu-id="db3ea-139">System. String</span><span class="sxs-lookup"><span data-stu-id="db3ea-139">System.String</span></span>

### <span data-ttu-id="db3ea-140">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="db3ea-140">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="db3ea-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db3ea-141">OUTPUTS</span></span>

### <span data-ttu-id="db3ea-142">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="db3ea-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="db3ea-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db3ea-143">NOTES</span></span>

## <span data-ttu-id="db3ea-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db3ea-144">RELATED LINKS</span></span>