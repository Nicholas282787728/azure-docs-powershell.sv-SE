---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102153"
---
# <span data-ttu-id="79fde-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fde-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="79fde-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79fde-102">SYNOPSIS</span></span>
<span data-ttu-id="79fde-103">Hämtar en PROBE-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="79fde-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="79fde-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79fde-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79fde-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79fde-105">DESCRIPTION</span></span>
<span data-ttu-id="79fde-106">Cmdleten **Get-AzLoadBalancerProbeConfig** hämtar en eller flera PROBE-konfigurationer för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="79fde-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="79fde-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79fde-107">EXAMPLES</span></span>

### <span data-ttu-id="79fde-108">Exempel 1: Hämta avsöknings konfigurationen för en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="79fde-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="79fde-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="79fde-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="79fde-110">Det andra kommandot får den associerade avsöknings konfigurationen som heter ' Avsök från belastningsutjämnaren i $slb.</span><span class="sxs-lookup"><span data-stu-id="79fde-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="79fde-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79fde-111">PARAMETERS</span></span>

### <span data-ttu-id="79fde-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fde-112">-DefaultProfile</span></span>
<span data-ttu-id="79fde-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79fde-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79fde-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79fde-114">-LoadBalancer</span></span>
<span data-ttu-id="79fde-115">Anger den belastningsutjämnare som är kopplad till den avsöknings konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="79fde-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="79fde-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="79fde-116">-Name</span></span>
<span data-ttu-id="79fde-117">Anger namnet på den PROBE-konfiguration som ska visas.</span><span class="sxs-lookup"><span data-stu-id="79fde-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="79fde-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fde-118">CommonParameters</span></span>
<span data-ttu-id="79fde-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79fde-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fde-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79fde-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fde-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79fde-121">INPUTS</span></span>

### <span data-ttu-id="79fde-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79fde-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="79fde-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79fde-123">OUTPUTS</span></span>

### <span data-ttu-id="79fde-124">Microsoft. Azure. commands. Networks. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="79fde-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="79fde-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79fde-125">NOTES</span></span>

## <span data-ttu-id="79fde-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79fde-126">RELATED LINKS</span></span>

[<span data-ttu-id="79fde-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fde-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="79fde-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79fde-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="79fde-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fde-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="79fde-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fde-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="79fde-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fde-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


