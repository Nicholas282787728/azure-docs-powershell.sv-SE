---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a9a76af9eaee36913fd22c8003d6f4b9ba8c7b77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919013"
---
# <span data-ttu-id="d4458-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d4458-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d4458-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4458-102">SYNOPSIS</span></span>
<span data-ttu-id="d4458-103">Tar bort en inkommande konfiguration för NAT-pooler från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="d4458-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="d4458-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4458-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4458-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4458-105">DESCRIPTION</span></span>
<span data-ttu-id="d4458-106">Cmdleten **Remove-AzLoadBalancerInboundNatPoolConfig** tar bort en inkommande konfiguration för NAT-pool från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="d4458-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="d4458-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4458-107">EXAMPLES</span></span>

### <span data-ttu-id="d4458-108">1: ta bort</span><span class="sxs-lookup"><span data-stu-id="d4458-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="d4458-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4458-109">PARAMETERS</span></span>

### <span data-ttu-id="d4458-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4458-110">-DefaultProfile</span></span>
<span data-ttu-id="d4458-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4458-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4458-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d4458-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="d4458-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4458-113">-Name</span></span>
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

### <span data-ttu-id="d4458-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4458-114">-Confirm</span></span>
<span data-ttu-id="d4458-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4458-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4458-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4458-116">-WhatIf</span></span>
<span data-ttu-id="d4458-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4458-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4458-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4458-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4458-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4458-119">CommonParameters</span></span>
<span data-ttu-id="d4458-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4458-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4458-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4458-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4458-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4458-122">INPUTS</span></span>

### <span data-ttu-id="d4458-123">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d4458-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d4458-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4458-124">OUTPUTS</span></span>

### <span data-ttu-id="d4458-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d4458-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d4458-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4458-126">NOTES</span></span>

## <span data-ttu-id="d4458-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4458-127">RELATED LINKS</span></span>

[<span data-ttu-id="d4458-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d4458-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d4458-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d4458-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d4458-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d4458-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d4458-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d4458-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)