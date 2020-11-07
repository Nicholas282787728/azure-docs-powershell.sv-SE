---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 01e132dab83931a48254bb8483cc794d7c619a6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919012"
---
# <span data-ttu-id="42eb6-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42eb6-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="42eb6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="42eb6-103">Tar bort en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="42eb6-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="42eb6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42eb6-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42eb6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="42eb6-106">Cmdleten **Remove-AzLoadBalancerRuleConfig** tar bort en regel konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="42eb6-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="42eb6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42eb6-107">EXAMPLES</span></span>

### <span data-ttu-id="42eb6-108">Exempel 1: ta bort en regel konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="42eb6-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="42eb6-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="42eb6-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="42eb6-110">Det andra kommandot tar bort regel konfigurationen med namnet MyLBruleName från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="42eb6-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="42eb6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42eb6-111">PARAMETERS</span></span>

### <span data-ttu-id="42eb6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42eb6-112">-DefaultProfile</span></span>
<span data-ttu-id="42eb6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42eb6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42eb6-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42eb6-114">-LoadBalancer</span></span>
<span data-ttu-id="42eb6-115">Anger det **Loadbalancer** -objekt som innehåller regel konfigurationen som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42eb6-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42eb6-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="42eb6-116">-Name</span></span>
<span data-ttu-id="42eb6-117">Anger namnet på den regel för belastnings utjämning som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="42eb6-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42eb6-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42eb6-118">-Confirm</span></span>
<span data-ttu-id="42eb6-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42eb6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42eb6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42eb6-120">-WhatIf</span></span>
<span data-ttu-id="42eb6-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42eb6-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42eb6-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42eb6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42eb6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42eb6-123">CommonParameters</span></span>
<span data-ttu-id="42eb6-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42eb6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42eb6-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42eb6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42eb6-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42eb6-126">INPUTS</span></span>

### <span data-ttu-id="42eb6-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42eb6-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="42eb6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42eb6-128">OUTPUTS</span></span>

### <span data-ttu-id="42eb6-129">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42eb6-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="42eb6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42eb6-130">NOTES</span></span>

## <span data-ttu-id="42eb6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42eb6-131">RELATED LINKS</span></span>

[<span data-ttu-id="42eb6-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42eb6-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="42eb6-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="42eb6-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="42eb6-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42eb6-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="42eb6-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42eb6-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="42eb6-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42eb6-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


