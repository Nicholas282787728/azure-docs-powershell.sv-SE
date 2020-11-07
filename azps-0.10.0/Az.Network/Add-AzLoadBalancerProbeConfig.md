---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 9abff0880be98c01b4953957e719fc4e6553f6ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922401"
---
# <span data-ttu-id="395d2-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="395d2-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="395d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="395d2-102">SYNOPSIS</span></span>
<span data-ttu-id="395d2-103">Lägger till en PROBE-konfiguration till en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="395d2-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="395d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="395d2-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="395d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="395d2-105">DESCRIPTION</span></span>
<span data-ttu-id="395d2-106">Cmdleten **Add-AzLoadBalancerProbeConfig** lägger till en PROBE-konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="395d2-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="395d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="395d2-107">EXAMPLES</span></span>

### <span data-ttu-id="395d2-108">Exempel 1 lägga till en PROBE-konfiguration till en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="395d2-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="395d2-109">Det här kommandot får belastningsutjämnaren med namnet myLb, lägger till angiven Avsök-konfiguration i den och använder sedan cmdleten **set-AzLoadBalancer** för att uppdatera belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="395d2-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="395d2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="395d2-110">PARAMETERS</span></span>

### <span data-ttu-id="395d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395d2-111">-DefaultProfile</span></span>
<span data-ttu-id="395d2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="395d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="395d2-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="395d2-113">-IntervalInSeconds</span></span>
<span data-ttu-id="395d2-114">Anger intervallet i sekunder mellan avsökningar för varje instans av den belastningsutjämnade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="395d2-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="395d2-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="395d2-115">-LoadBalancer</span></span>
<span data-ttu-id="395d2-116">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="395d2-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="395d2-117">Denna cmdlet lägger till en PROBE-konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="395d2-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="395d2-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="395d2-118">-Name</span></span>
<span data-ttu-id="395d2-119">Anger namnet på den PROBE-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="395d2-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="395d2-120">-Port</span><span class="sxs-lookup"><span data-stu-id="395d2-120">-Port</span></span>
<span data-ttu-id="395d2-121">Anger vilken port som Avsök ska anslutas till till en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="395d2-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="395d2-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="395d2-122">-ProbeCount</span></span>
<span data-ttu-id="395d2-123">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="395d2-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="395d2-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="395d2-124">-Protocol</span></span>
<span data-ttu-id="395d2-125">Anger protokollet som ska användas för sonden.</span><span class="sxs-lookup"><span data-stu-id="395d2-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="395d2-126">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="395d2-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="395d2-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="395d2-127">-RequestPath</span></span>
<span data-ttu-id="395d2-128">Anger sökvägen i den belastningsutjämnade tjänsten som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="395d2-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="395d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395d2-129">CommonParameters</span></span>
<span data-ttu-id="395d2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395d2-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="395d2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395d2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="395d2-132">INPUTS</span></span>

### <span data-ttu-id="395d2-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="395d2-133">PSLoadBalancer</span></span>
<span data-ttu-id="395d2-134">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="395d2-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="395d2-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="395d2-135">OUTPUTS</span></span>

### <span data-ttu-id="395d2-136">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="395d2-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="395d2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="395d2-137">NOTES</span></span>

## <span data-ttu-id="395d2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="395d2-138">RELATED LINKS</span></span>

[<span data-ttu-id="395d2-139">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="395d2-139">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="395d2-140">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="395d2-140">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="395d2-141">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="395d2-141">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="395d2-142">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="395d2-142">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="395d2-143">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="395d2-143">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


