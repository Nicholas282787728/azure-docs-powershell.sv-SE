---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271206"
---
# <span data-ttu-id="70045-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="70045-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="70045-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70045-102">SYNOPSIS</span></span>
<span data-ttu-id="70045-103">Uppdaterar en PROBE-konfiguration för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="70045-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="70045-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70045-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70045-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70045-105">DESCRIPTION</span></span>
<span data-ttu-id="70045-106">Cmdleten **set-AzLoadBalancerProbeConfig** uppdaterar en PROBE-konfiguration för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="70045-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="70045-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70045-107">EXAMPLES</span></span>

### <span data-ttu-id="70045-108">Exempel 1: ändra sondens konfiguration på en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="70045-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="70045-109">Det första kommandot får belastningsutjämnarens namn MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="70045-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="70045-110">Det andra kommandot använder pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzLoadBalancerProbeConfig, vilket lägger till en ny avsöknings konfiguration för den.</span><span class="sxs-lookup"><span data-stu-id="70045-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="70045-111">Det tredje kommandot skickar belastningsutjämnaren till **set-AzLoadBalancerProbeConfig** , som anger den nya konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="70045-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="70045-112">Observera att du måste ange flera av de parametrar som angavs i föregående kommando eftersom de är obligatoriska med den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70045-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="70045-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70045-113">PARAMETERS</span></span>

### <span data-ttu-id="70045-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70045-114">-DefaultProfile</span></span>
<span data-ttu-id="70045-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70045-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70045-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="70045-116">-IntervalInSeconds</span></span>
<span data-ttu-id="70045-117">Anger intervallet i sekunder mellan avsökningar för varje instans av den belastningsutjämnade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="70045-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70045-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70045-118">-LoadBalancer</span></span>
<span data-ttu-id="70045-119">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="70045-119">Specifies a load balancer.</span></span>
<span data-ttu-id="70045-120">Denna cmdlet uppdaterar en PROBE-konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="70045-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="70045-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="70045-121">-Name</span></span>
<span data-ttu-id="70045-122">Anger namnet på den avsöknings konfiguration som cmdleten ställer in.</span><span class="sxs-lookup"><span data-stu-id="70045-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="70045-123">-Port</span><span class="sxs-lookup"><span data-stu-id="70045-123">-Port</span></span>
<span data-ttu-id="70045-124">Anger vilken port som Avsök ska anslutas till till en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="70045-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70045-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="70045-125">-ProbeCount</span></span>
<span data-ttu-id="70045-126">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="70045-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70045-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="70045-127">-Protocol</span></span>
<span data-ttu-id="70045-128">Anger det protokoll som ska användas för sökning.</span><span class="sxs-lookup"><span data-stu-id="70045-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="70045-129">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="70045-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70045-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="70045-130">-RequestPath</span></span>
<span data-ttu-id="70045-131">Anger sökvägen i den belastningsutjämnade tjänsten som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="70045-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70045-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70045-132">-Confirm</span></span>
<span data-ttu-id="70045-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70045-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70045-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70045-134">-WhatIf</span></span>
<span data-ttu-id="70045-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70045-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70045-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70045-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70045-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70045-137">CommonParameters</span></span>
<span data-ttu-id="70045-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70045-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70045-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70045-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70045-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70045-140">INPUTS</span></span>

### <span data-ttu-id="70045-141">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70045-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="70045-142">System. String</span><span class="sxs-lookup"><span data-stu-id="70045-142">System.String</span></span>

### <span data-ttu-id="70045-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="70045-143">System.Int32</span></span>

## <span data-ttu-id="70045-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70045-144">OUTPUTS</span></span>

### <span data-ttu-id="70045-145">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70045-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="70045-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70045-146">NOTES</span></span>

## <span data-ttu-id="70045-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70045-147">RELATED LINKS</span></span>

[<span data-ttu-id="70045-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="70045-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="70045-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70045-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="70045-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="70045-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="70045-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="70045-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="70045-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="70045-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

