---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325926"
---
# <span data-ttu-id="bd454-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd454-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="bd454-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd454-102">SYNOPSIS</span></span>
<span data-ttu-id="bd454-103">Lägger till en PROBE-konfiguration till en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="bd454-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="bd454-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd454-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd454-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd454-105">DESCRIPTION</span></span>
<span data-ttu-id="bd454-106">Cmdleten **Add-AzLoadBalancerProbeConfig** lägger till en PROBE-konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="bd454-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="bd454-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd454-107">EXAMPLES</span></span>

### <span data-ttu-id="bd454-108">Exempel 1: lägga till en PROBE-konfiguration till en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="bd454-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="bd454-109">Det här kommandot får belastningsutjämnaren med namnet myLb, lägger till angiven Avsök-konfiguration i den och använder sedan cmdleten **set-AzLoadBalancer** för att uppdatera belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="bd454-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="bd454-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd454-110">PARAMETERS</span></span>

### <span data-ttu-id="bd454-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd454-111">-DefaultProfile</span></span>
<span data-ttu-id="bd454-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd454-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd454-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="bd454-113">-IntervalInSeconds</span></span>
<span data-ttu-id="bd454-114">Anger intervallet i sekunder mellan avsökningar för varje instans av den belastningsutjämnade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bd454-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="bd454-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd454-115">-LoadBalancer</span></span>
<span data-ttu-id="bd454-116">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bd454-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="bd454-117">Denna cmdlet lägger till en PROBE-konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bd454-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="bd454-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd454-118">-Name</span></span>
<span data-ttu-id="bd454-119">Anger namnet på den PROBE-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="bd454-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="bd454-120">-Port</span><span class="sxs-lookup"><span data-stu-id="bd454-120">-Port</span></span>
<span data-ttu-id="bd454-121">Anger vilken port som Avsök ska anslutas till till en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="bd454-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="bd454-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="bd454-122">-ProbeCount</span></span>
<span data-ttu-id="bd454-123">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="bd454-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="bd454-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="bd454-124">-Protocol</span></span>
<span data-ttu-id="bd454-125">Anger protokollet som ska användas för sonden.</span><span class="sxs-lookup"><span data-stu-id="bd454-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="bd454-126">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="bd454-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="bd454-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="bd454-127">-RequestPath</span></span>
<span data-ttu-id="bd454-128">Anger sökvägen i den belastningsutjämnade tjänsten som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="bd454-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="bd454-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd454-129">-Confirm</span></span>
<span data-ttu-id="bd454-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd454-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd454-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd454-131">-WhatIf</span></span>
<span data-ttu-id="bd454-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd454-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd454-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd454-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd454-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd454-134">CommonParameters</span></span>
<span data-ttu-id="bd454-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd454-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd454-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd454-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd454-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd454-137">INPUTS</span></span>

### <span data-ttu-id="bd454-138">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd454-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="bd454-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bd454-139">System.String</span></span>

### <span data-ttu-id="bd454-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bd454-140">System.Int32</span></span>

## <span data-ttu-id="bd454-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd454-141">OUTPUTS</span></span>

### <span data-ttu-id="bd454-142">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd454-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bd454-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd454-143">NOTES</span></span>

## <span data-ttu-id="bd454-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd454-144">RELATED LINKS</span></span>

[<span data-ttu-id="bd454-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd454-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="bd454-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd454-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="bd454-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd454-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="bd454-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd454-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="bd454-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bd454-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


