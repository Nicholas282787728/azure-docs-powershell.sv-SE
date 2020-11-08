---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089538"
---
# <span data-ttu-id="3e263-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="3e263-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="3e263-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e263-102">SYNOPSIS</span></span>
<span data-ttu-id="3e263-103">Skapa en ny grupp för regel insamling för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="3e263-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="3e263-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e263-104">SYNTAX</span></span>

### <span data-ttu-id="3e263-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e263-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e263-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e263-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e263-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e263-107">DESCRIPTION</span></span>
<span data-ttu-id="3e263-108">Cmdleten **New-AzFirewallPolicyRuleCollectionGroup** skapar en regel samlings grupp i en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="3e263-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="3e263-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e263-109">EXAMPLES</span></span>

### <span data-ttu-id="3e263-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e263-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="3e263-111">I det här exemplet skapas en regel samlings grupp i brand Väggs princip $fp</span><span class="sxs-lookup"><span data-stu-id="3e263-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="3e263-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e263-112">PARAMETERS</span></span>

### <span data-ttu-id="3e263-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e263-113">-DefaultProfile</span></span>
<span data-ttu-id="3e263-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e263-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e263-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="3e263-115">-FirewallPolicyName</span></span>
<span data-ttu-id="3e263-116">Namnet på brand Väggs principen</span><span class="sxs-lookup"><span data-stu-id="3e263-116">The name of the firewall policy</span></span>

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

### <span data-ttu-id="3e263-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="3e263-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="3e263-118">Brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="3e263-118">Firewall Policy.</span></span>

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

### <span data-ttu-id="3e263-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e263-119">-Name</span></span>
<span data-ttu-id="3e263-120">Namnet på regel gruppen</span><span class="sxs-lookup"><span data-stu-id="3e263-120">The name of the Rule Group</span></span>

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

### <span data-ttu-id="3e263-121">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="3e263-121">-Priority</span></span>
<span data-ttu-id="3e263-122">Regel gruppens prioritet</span><span class="sxs-lookup"><span data-stu-id="3e263-122">The priority of the rule group</span></span>

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

### <span data-ttu-id="3e263-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e263-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e263-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3e263-124">The resource group name.</span></span>

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

### <span data-ttu-id="3e263-125">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="3e263-125">-RuleCollection</span></span>
<span data-ttu-id="3e263-126">Listan med regler</span><span class="sxs-lookup"><span data-stu-id="3e263-126">The list of rules</span></span>

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

### <span data-ttu-id="3e263-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e263-127">-Confirm</span></span>
<span data-ttu-id="3e263-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e263-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e263-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e263-129">-WhatIf</span></span>
<span data-ttu-id="3e263-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e263-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e263-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e263-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e263-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e263-132">CommonParameters</span></span>
<span data-ttu-id="3e263-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e263-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e263-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e263-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e263-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e263-135">INPUTS</span></span>

### <span data-ttu-id="3e263-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3e263-136">System.String</span></span>

### <span data-ttu-id="3e263-137">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3e263-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="3e263-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e263-138">OUTPUTS</span></span>

### <span data-ttu-id="3e263-139">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="3e263-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="3e263-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e263-140">NOTES</span></span>

## <span data-ttu-id="3e263-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e263-141">RELATED LINKS</span></span>
