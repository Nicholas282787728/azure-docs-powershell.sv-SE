---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393123"
---
# <span data-ttu-id="4a4ee-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4ee-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="4a4ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4ee-103">Tar bort en konfiguration för utgående regel från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="4a4ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a4ee-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a4ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a4ee-105">DESCRIPTION</span></span>
<span data-ttu-id="4a4ee-106">Cmdleten **Remove-AzLoadBalancerOutboundRuleConfig** tar bort en konfiguration för utgående regel från en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="4a4ee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a4ee-107">EXAMPLES</span></span>

### <span data-ttu-id="4a4ee-108">Exempel 1: ta bort en regel för utgående trafik från en Azure-belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="4a4ee-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="4a4ee-109">Det första kommandot får belastningsutjämnaren som är kopplad till den utgående regel konfiguration som du vill ta bort och sedan spara den i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="4a4ee-110">Det andra kommandot tar bort den associerade konfigurationen för utgående trafik från belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="4a4ee-111">Det tredje kommandot uppdaterar belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="4a4ee-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a4ee-112">PARAMETERS</span></span>

### <span data-ttu-id="4a4ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4ee-113">-DefaultProfile</span></span>
<span data-ttu-id="4a4ee-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a4ee-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4a4ee-115">-LoadBalancer</span></span>
<span data-ttu-id="4a4ee-116">Referensen för belastnings Utjämnings resursen.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="4a4ee-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a4ee-117">-Name</span></span>
<span data-ttu-id="4a4ee-118">Namnet på regeln för utgående trafik</span><span class="sxs-lookup"><span data-stu-id="4a4ee-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="4a4ee-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a4ee-119">-Confirm</span></span>
<span data-ttu-id="4a4ee-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a4ee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a4ee-121">-WhatIf</span></span>
<span data-ttu-id="4a4ee-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a4ee-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a4ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4ee-124">CommonParameters</span></span>
<span data-ttu-id="4a4ee-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a4ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4ee-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a4ee-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4ee-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a4ee-127">INPUTS</span></span>

### <span data-ttu-id="4a4ee-128">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4a4ee-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4a4ee-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a4ee-129">OUTPUTS</span></span>

### <span data-ttu-id="4a4ee-130">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4a4ee-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4a4ee-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a4ee-131">NOTES</span></span>

## <span data-ttu-id="4a4ee-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a4ee-132">RELATED LINKS</span></span>

[<span data-ttu-id="4a4ee-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4ee-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="4a4ee-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4ee-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="4a4ee-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4ee-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="4a4ee-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a4ee-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
