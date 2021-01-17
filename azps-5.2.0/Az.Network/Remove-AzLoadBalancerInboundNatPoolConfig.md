---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399608"
---
# <span data-ttu-id="7cf96-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7cf96-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="7cf96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cf96-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf96-103">Tar bort en inkommande konfiguration för NAT-pooler från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="7cf96-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="7cf96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cf96-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf96-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cf96-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf96-106">Cmdleten **Remove-AzLoadBalancerInboundNatPoolConfig** tar bort en inkommande konfiguration för NAT-pool från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="7cf96-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="7cf96-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cf96-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf96-108">1: ta bort</span><span class="sxs-lookup"><span data-stu-id="7cf96-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="7cf96-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cf96-109">PARAMETERS</span></span>

### <span data-ttu-id="7cf96-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf96-110">-DefaultProfile</span></span>
<span data-ttu-id="7cf96-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf96-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf96-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cf96-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="7cf96-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cf96-113">-Name</span></span>
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

### <span data-ttu-id="7cf96-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cf96-114">-Confirm</span></span>
<span data-ttu-id="7cf96-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cf96-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf96-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf96-116">-WhatIf</span></span>
<span data-ttu-id="7cf96-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7cf96-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cf96-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7cf96-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf96-119">CommonParameters</span></span>
<span data-ttu-id="7cf96-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf96-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf96-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf96-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cf96-122">INPUTS</span></span>

### <span data-ttu-id="7cf96-123">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cf96-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7cf96-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cf96-124">OUTPUTS</span></span>

### <span data-ttu-id="7cf96-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7cf96-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7cf96-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cf96-126">NOTES</span></span>

## <span data-ttu-id="7cf96-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cf96-127">RELATED LINKS</span></span>

[<span data-ttu-id="7cf96-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7cf96-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7cf96-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7cf96-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7cf96-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7cf96-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7cf96-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7cf96-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
