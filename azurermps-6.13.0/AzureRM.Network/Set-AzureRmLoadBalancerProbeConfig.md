---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 3fe5345e6d3cbad90d99f5a94e72873beaca7c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756024"
---
# <span data-ttu-id="45f16-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45f16-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="45f16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45f16-102">SYNOPSIS</span></span>
<span data-ttu-id="45f16-103">Anger mål tillstånd för en avsöknings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="45f16-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45f16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45f16-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45f16-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45f16-105">DESCRIPTION</span></span>
<span data-ttu-id="45f16-106">Cmdleten **set-AzureRmLoadBalancerProbeConfig** anger mål tillståndet för en PROBE-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="45f16-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="45f16-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45f16-107">EXAMPLES</span></span>

### <span data-ttu-id="45f16-108">Exempel 1: ändra sondens konfiguration på en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="45f16-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="45f16-109">Det första kommandot får belastningsutjämnarens namn MyLoadBalancer och lagrar det sedan i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="45f16-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="45f16-110">Det andra kommandot använder pipeline-operatorn för att överföra belastningsutjämnaren i $slb till Add-AzureRmLoadBalancerProbeConfig, vilket lägger till en ny avsöknings konfiguration för den.</span><span class="sxs-lookup"><span data-stu-id="45f16-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="45f16-111">Det tredje kommandot skickar belastningsutjämnaren till **set-AzureRmLoadBalancerProbeConfig** , som anger den nya konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="45f16-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="45f16-112">Observera att du måste ange flera av de parametrar som angavs i föregående kommando eftersom de är obligatoriska med den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45f16-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="45f16-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45f16-113">PARAMETERS</span></span>

### <span data-ttu-id="45f16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45f16-114">-DefaultProfile</span></span>
<span data-ttu-id="45f16-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45f16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45f16-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="45f16-116">-IntervalInSeconds</span></span>
<span data-ttu-id="45f16-117">Anger intervallet i sekunder mellan avsökningar för varje instans av den belastningsutjämnade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="45f16-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="45f16-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45f16-118">-LoadBalancer</span></span>
<span data-ttu-id="45f16-119">Anger en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="45f16-119">Specifies a load balancer.</span></span>
<span data-ttu-id="45f16-120">Denna cmdlet anger mål tillståndet för en avsöknings konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="45f16-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="45f16-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="45f16-121">-Name</span></span>
<span data-ttu-id="45f16-122">Anger namnet på den avsöknings konfiguration som cmdleten ställer in.</span><span class="sxs-lookup"><span data-stu-id="45f16-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="45f16-123">-Port</span><span class="sxs-lookup"><span data-stu-id="45f16-123">-Port</span></span>
<span data-ttu-id="45f16-124">Anger vilken port som Avsök ska anslutas till till en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="45f16-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="45f16-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="45f16-125">-ProbeCount</span></span>
<span data-ttu-id="45f16-126">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="45f16-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="45f16-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="45f16-127">-Protocol</span></span>
<span data-ttu-id="45f16-128">Anger det protokoll som ska användas för sökning.</span><span class="sxs-lookup"><span data-stu-id="45f16-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="45f16-129">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="45f16-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="45f16-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="45f16-130">-RequestPath</span></span>
<span data-ttu-id="45f16-131">Anger sökvägen i den belastningsutjämnade tjänsten som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="45f16-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="45f16-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45f16-132">-Confirm</span></span>
<span data-ttu-id="45f16-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45f16-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45f16-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45f16-134">-WhatIf</span></span>
<span data-ttu-id="45f16-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45f16-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45f16-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45f16-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45f16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f16-137">CommonParameters</span></span>
<span data-ttu-id="45f16-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45f16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f16-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45f16-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f16-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45f16-140">INPUTS</span></span>

### <span data-ttu-id="45f16-141">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45f16-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="45f16-142">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="45f16-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="45f16-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45f16-143">OUTPUTS</span></span>

### <span data-ttu-id="45f16-144">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45f16-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="45f16-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45f16-145">NOTES</span></span>

## <span data-ttu-id="45f16-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45f16-146">RELATED LINKS</span></span>

[<span data-ttu-id="45f16-147">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45f16-147">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="45f16-148">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45f16-148">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="45f16-149">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45f16-149">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="45f16-150">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45f16-150">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="45f16-151">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="45f16-151">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


