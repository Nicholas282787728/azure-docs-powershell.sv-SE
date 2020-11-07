---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a14196a98be2f901cc120926e716efe884a747a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924202"
---
# <span data-ttu-id="b4575-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b4575-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="b4575-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4575-102">SYNOPSIS</span></span>
<span data-ttu-id="b4575-103">Anger mål tillstånd för en avsöknings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b4575-103">Sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="b4575-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4575-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4575-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4575-105">DESCRIPTION</span></span>
<span data-ttu-id="b4575-106">Cmdleten **set-AzLoadBalancerProbeConfig** anger mål tillståndet för en PROBE-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b4575-106">The **Set-AzLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="b4575-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4575-107">EXAMPLES</span></span>

### <span data-ttu-id="b4575-108">Exempel 1: ändra sondens konfiguration på en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="b4575-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="b4575-109">Det första kommandot får belastningsutjämnarens namn MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="b4575-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="b4575-110">Det andra kommandot använder pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzLoadBalancerProbeConfig, vilket lägger till en ny avsöknings konfiguration för den.</span><span class="sxs-lookup"><span data-stu-id="b4575-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="b4575-111">Det tredje kommandot skickar belastningsutjämnaren till **set-AzLoadBalancerProbeConfig** , som anger den nya konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b4575-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="b4575-112">Observera att du måste ange flera av de parametrar som angavs i föregående kommando eftersom de är obligatoriska med den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4575-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="b4575-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4575-113">PARAMETERS</span></span>

### <span data-ttu-id="b4575-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4575-114">-DefaultProfile</span></span>
<span data-ttu-id="b4575-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4575-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4575-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b4575-116">-IntervalInSeconds</span></span>
<span data-ttu-id="b4575-117">Anger intervallet i sekunder mellan avsökningar för varje instans av den belastningsutjämnade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b4575-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="b4575-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4575-118">-LoadBalancer</span></span>
<span data-ttu-id="b4575-119">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="b4575-119">Specifies a load balancer.</span></span>
<span data-ttu-id="b4575-120">Denna cmdlet anger mål tillståndet för en avsöknings konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b4575-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4575-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4575-121">-Name</span></span>
<span data-ttu-id="b4575-122">Anger namnet på den avsöknings konfiguration som cmdleten ställer in.</span><span class="sxs-lookup"><span data-stu-id="b4575-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="b4575-123">-Port</span><span class="sxs-lookup"><span data-stu-id="b4575-123">-Port</span></span>
<span data-ttu-id="b4575-124">Anger vilken port som Avsök ska anslutas till till en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="b4575-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="b4575-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="b4575-125">-ProbeCount</span></span>
<span data-ttu-id="b4575-126">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="b4575-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="b4575-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="b4575-127">-Protocol</span></span>
<span data-ttu-id="b4575-128">Anger det protokoll som ska användas för sökning.</span><span class="sxs-lookup"><span data-stu-id="b4575-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="b4575-129">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="b4575-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="b4575-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="b4575-130">-RequestPath</span></span>
<span data-ttu-id="b4575-131">Anger sökvägen i den belastningsutjämnade tjänsten som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="b4575-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="b4575-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4575-132">CommonParameters</span></span>
<span data-ttu-id="b4575-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4575-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4575-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4575-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4575-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4575-135">INPUTS</span></span>

### <span data-ttu-id="b4575-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4575-136">PSLoadBalancer</span></span>
<span data-ttu-id="b4575-137">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b4575-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b4575-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4575-138">OUTPUTS</span></span>

### <span data-ttu-id="b4575-139">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4575-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b4575-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4575-140">NOTES</span></span>

## <span data-ttu-id="b4575-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4575-141">RELATED LINKS</span></span>

[<span data-ttu-id="b4575-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b4575-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="b4575-143">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4575-143">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b4575-144">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b4575-144">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="b4575-145">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b4575-145">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="b4575-146">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b4575-146">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


