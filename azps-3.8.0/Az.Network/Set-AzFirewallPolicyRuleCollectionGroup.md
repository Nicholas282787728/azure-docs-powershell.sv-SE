---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090235"
---
# <span data-ttu-id="0a9c8-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="0a9c8-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="0a9c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a9c8-102">SYNOPSIS</span></span>
<span data-ttu-id="0a9c8-103">sparar en ändrad grupp för regel samling för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="0a9c8-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="0a9c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a9c8-104">SYNTAX</span></span>

### <span data-ttu-id="0a9c8-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a9c8-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a9c8-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a9c8-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a9c8-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a9c8-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a9c8-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a9c8-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a9c8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a9c8-109">DESCRIPTION</span></span>
<span data-ttu-id="0a9c8-110">Cmdleten **set-AzFirewallPolicyRuleCollectionGroup** uppdaterar en regel samlings grupper i en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="0a9c8-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="0a9c8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a9c8-111">EXAMPLES</span></span>

### <span data-ttu-id="0a9c8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0a9c8-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="0a9c8-113">Det här exemplet uppdaterar en regel samlings grupp i brand Väggs princip $fp</span><span class="sxs-lookup"><span data-stu-id="0a9c8-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="0a9c8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a9c8-114">PARAMETERS</span></span>

### <span data-ttu-id="0a9c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a9c8-115">-DefaultProfile</span></span>
<span data-ttu-id="0a9c8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a9c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a9c8-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="0a9c8-117">-FirewallPolicyName</span></span>
<span data-ttu-id="0a9c8-118">Namnet på brand Väggs principen</span><span class="sxs-lookup"><span data-stu-id="0a9c8-118">The name of the firewall policy</span></span>

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

### <span data-ttu-id="0a9c8-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0a9c8-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="0a9c8-120">Brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="0a9c8-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a9c8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a9c8-121">-InputObject</span></span>
<span data-ttu-id="0a9c8-122">Listan med regler</span><span class="sxs-lookup"><span data-stu-id="0a9c8-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a9c8-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a9c8-123">-Name</span></span>
<span data-ttu-id="0a9c8-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0a9c8-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a9c8-125">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="0a9c8-125">-Priority</span></span>
<span data-ttu-id="0a9c8-126">Regel gruppens prioritet</span><span class="sxs-lookup"><span data-stu-id="0a9c8-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a9c8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a9c8-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a9c8-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0a9c8-128">The resource group name.</span></span>

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

### <span data-ttu-id="0a9c8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a9c8-129">-ResourceId</span></span>
<span data-ttu-id="0a9c8-130">Resurs-ID för regel samlings gruppen</span><span class="sxs-lookup"><span data-stu-id="0a9c8-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a9c8-131">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="0a9c8-131">-RuleCollection</span></span>
<span data-ttu-id="0a9c8-132">Listan med regel samlingar</span><span class="sxs-lookup"><span data-stu-id="0a9c8-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a9c8-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a9c8-133">-Confirm</span></span>
<span data-ttu-id="0a9c8-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a9c8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a9c8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a9c8-135">-WhatIf</span></span>
<span data-ttu-id="0a9c8-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a9c8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a9c8-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a9c8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a9c8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a9c8-138">CommonParameters</span></span>
<span data-ttu-id="0a9c8-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a9c8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a9c8-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a9c8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a9c8-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a9c8-141">INPUTS</span></span>

### <span data-ttu-id="0a9c8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0a9c8-142">System.String</span></span>

### <span data-ttu-id="0a9c8-143">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0a9c8-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="0a9c8-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a9c8-144">OUTPUTS</span></span>

### <span data-ttu-id="0a9c8-145">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="0a9c8-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="0a9c8-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a9c8-146">NOTES</span></span>

## <span data-ttu-id="0a9c8-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a9c8-147">RELATED LINKS</span></span>
