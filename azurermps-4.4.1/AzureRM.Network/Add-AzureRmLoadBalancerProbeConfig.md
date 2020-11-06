---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 79e9d856825e174bc8667f99e7b25b301230dec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581392"
---
# <span data-ttu-id="e3b49-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3b49-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e3b49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3b49-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b49-103">Lägger till en PROBE-konfiguration till en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e3b49-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3b49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3b49-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3b49-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3b49-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b49-106">Cmdleten **Add-AzureRmLoadBalancerProbeConfig** lägger till en PROBE-konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="e3b49-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="e3b49-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3b49-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b49-108">Exempel 1 lägga till en PROBE-konfiguration till en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="e3b49-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="e3b49-109">Det här kommandot får belastningsutjämnaren med namnet myLb, lägger till angiven Avsök-konfiguration i den och använder sedan cmdleten **set-AzureRmLoadBalancer** för att uppdatera belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="e3b49-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="e3b49-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3b49-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b49-111">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e3b49-111">-IntervalInSeconds</span></span>
<span data-ttu-id="e3b49-112">Anger intervallet i sekunder mellan avsökningar för varje instans av den belastningsutjämnade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e3b49-112">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b49-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e3b49-113">-LoadBalancer</span></span>
<span data-ttu-id="e3b49-114">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e3b49-114">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="e3b49-115">Denna cmdlet lägger till en PROBE-konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e3b49-115">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b49-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3b49-116">-Name</span></span>
<span data-ttu-id="e3b49-117">Anger namnet på den PROBE-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="e3b49-117">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="e3b49-118">-Port</span><span class="sxs-lookup"><span data-stu-id="e3b49-118">-Port</span></span>
<span data-ttu-id="e3b49-119">Anger vilken port som Avsök ska anslutas till till en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="e3b49-119">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b49-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="e3b49-120">-ProbeCount</span></span>
<span data-ttu-id="e3b49-121">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="e3b49-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b49-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e3b49-122">-Protocol</span></span>
<span data-ttu-id="e3b49-123">Anger protokollet som ska användas för sonden.</span><span class="sxs-lookup"><span data-stu-id="e3b49-123">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="e3b49-124">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="e3b49-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b49-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="e3b49-125">-RequestPath</span></span>
<span data-ttu-id="e3b49-126">Anger sökvägen i den belastningsutjämnade tjänsten som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="e3b49-126">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="e3b49-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b49-127">-DefaultProfile</span></span>
<span data-ttu-id="e3b49-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b49-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b49-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b49-129">CommonParameters</span></span>
<span data-ttu-id="e3b49-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b49-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b49-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b49-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b49-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3b49-132">INPUTS</span></span>

### <span data-ttu-id="e3b49-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e3b49-133">PSLoadBalancer</span></span>
<span data-ttu-id="e3b49-134">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e3b49-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e3b49-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3b49-135">OUTPUTS</span></span>

### <span data-ttu-id="e3b49-136">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e3b49-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e3b49-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3b49-137">NOTES</span></span>

## <span data-ttu-id="e3b49-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3b49-138">RELATED LINKS</span></span>

[<span data-ttu-id="e3b49-139">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3b49-139">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e3b49-140">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3b49-140">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e3b49-141">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3b49-141">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e3b49-142">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e3b49-142">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="e3b49-143">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e3b49-143">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


