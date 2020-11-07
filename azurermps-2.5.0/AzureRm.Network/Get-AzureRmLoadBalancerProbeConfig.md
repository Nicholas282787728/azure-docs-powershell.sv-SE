---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 30989d3b9c71821c2eae3cdfd97f9e4e5fc0cb15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931306"
---
# <span data-ttu-id="0c9a1-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c9a1-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="0c9a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9a1-103">Hämtar en PROBE-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0c9a1-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c9a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c9a1-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c9a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="0c9a1-106">Cmdleten **Get-AzureRmLoadBalancerProbeConfig** hämtar en eller flera PROBE-konfigurationer för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0c9a1-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="0c9a1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c9a1-107">EXAMPLES</span></span>

### <span data-ttu-id="0c9a1-108">Exempel 1: Hämta avsöknings konfigurationen för en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="0c9a1-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="0c9a1-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="0c9a1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="0c9a1-110">Det andra kommandot får den associerade avsöknings konfigurationen som heter ' Avsök från belastningsutjämnaren i $slb.</span><span class="sxs-lookup"><span data-stu-id="0c9a1-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="0c9a1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c9a1-111">PARAMETERS</span></span>

### <span data-ttu-id="0c9a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9a1-112">-DefaultProfile</span></span>
<span data-ttu-id="0c9a1-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c9a1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c9a1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c9a1-114">-LoadBalancer</span></span>
<span data-ttu-id="0c9a1-115">Anger den belastningsutjämnare som är kopplad till den avsöknings konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="0c9a1-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c9a1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c9a1-116">-Name</span></span>
<span data-ttu-id="0c9a1-117">Anger namnet på den PROBE-konfiguration som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0c9a1-117">Specifies the name of the probe configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c9a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9a1-118">CommonParameters</span></span>
<span data-ttu-id="0c9a1-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c9a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9a1-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c9a1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9a1-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c9a1-121">INPUTS</span></span>

### <span data-ttu-id="0c9a1-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c9a1-122">PSLoadBalancer</span></span>
<span data-ttu-id="0c9a1-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0c9a1-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0c9a1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c9a1-124">OUTPUTS</span></span>

### <span data-ttu-id="0c9a1-125">Microsoft. Azure. commands. Networks. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="0c9a1-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="0c9a1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c9a1-126">NOTES</span></span>

## <span data-ttu-id="0c9a1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c9a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="0c9a1-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c9a1-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0c9a1-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c9a1-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="0c9a1-130">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c9a1-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0c9a1-131">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c9a1-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0c9a1-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0c9a1-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


