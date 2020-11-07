---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 902fa7e266583fe52c516ac3704bdc394215e2c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930906"
---
# <span data-ttu-id="0f4d6-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f4d6-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="0f4d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4d6-103">Anger mål tillstånd för en avsöknings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f4d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f4d6-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f4d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="0f4d6-106">Cmdleten **set-AzureRmLoadBalancerProbeConfig** anger mål tillståndet för en PROBE-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="0f4d6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="0f4d6-108">Exempel 1: ändra sondens konfiguration på en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="0f4d6-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="0f4d6-109">Det första kommandot får belastningsutjämnarens namn MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="0f4d6-110">Det andra kommandot använder pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzureRmLoadBalancerProbeConfig, vilket lägger till en ny avsöknings konfiguration för den.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="0f4d6-111">Det tredje kommandot skickar belastningsutjämnaren till **set-AzureRmLoadBalancerProbeConfig** , som anger den nya konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="0f4d6-112">Observera att du måste ange flera av de parametrar som angavs i föregående kommando eftersom de är obligatoriska med den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="0f4d6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f4d6-113">PARAMETERS</span></span>

### <span data-ttu-id="0f4d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f4d6-114">-DefaultProfile</span></span>
<span data-ttu-id="0f4d6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f4d6-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0f4d6-116">-IntervalInSeconds</span></span>
<span data-ttu-id="0f4d6-117">Anger intervallet i sekunder mellan avsökningar för varje instans av den belastningsutjämnade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4d6-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f4d6-118">-LoadBalancer</span></span>
<span data-ttu-id="0f4d6-119">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-119">Specifies a load balancer.</span></span>
<span data-ttu-id="0f4d6-120">Denna cmdlet anger mål tillståndet för en avsöknings konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f4d6-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f4d6-121">-Name</span></span>
<span data-ttu-id="0f4d6-122">Anger namnet på den avsöknings konfiguration som cmdleten ställer in.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4d6-123">-Port</span><span class="sxs-lookup"><span data-stu-id="0f4d6-123">-Port</span></span>
<span data-ttu-id="0f4d6-124">Anger vilken port som Avsök ska anslutas till till en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4d6-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="0f4d6-125">-ProbeCount</span></span>
<span data-ttu-id="0f4d6-126">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4d6-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0f4d6-127">-Protocol</span></span>
<span data-ttu-id="0f4d6-128">Anger det protokoll som ska användas för sökning.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="0f4d6-129">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4d6-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="0f4d6-130">-RequestPath</span></span>
<span data-ttu-id="0f4d6-131">Anger sökvägen i den belastningsutjämnade tjänsten som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="0f4d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4d6-132">CommonParameters</span></span>
<span data-ttu-id="0f4d6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f4d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4d6-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f4d6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4d6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f4d6-135">INPUTS</span></span>

### <span data-ttu-id="0f4d6-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f4d6-136">PSLoadBalancer</span></span>
<span data-ttu-id="0f4d6-137">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0f4d6-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0f4d6-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f4d6-138">OUTPUTS</span></span>

### <span data-ttu-id="0f4d6-139">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f4d6-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0f4d6-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f4d6-140">NOTES</span></span>

## <span data-ttu-id="0f4d6-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f4d6-141">RELATED LINKS</span></span>

[<span data-ttu-id="0f4d6-142">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f4d6-142">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0f4d6-143">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f4d6-143">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="0f4d6-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f4d6-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0f4d6-145">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f4d6-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0f4d6-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0f4d6-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


