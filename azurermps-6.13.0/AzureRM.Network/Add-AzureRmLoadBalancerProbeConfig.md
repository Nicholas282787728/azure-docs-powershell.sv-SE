---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 62ed11a2819a2b0c31756c90ce4ab623a1feae91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582615"
---
# <span data-ttu-id="30827-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30827-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="30827-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30827-102">SYNOPSIS</span></span>
<span data-ttu-id="30827-103">Lägger till en PROBE-konfiguration till en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="30827-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30827-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30827-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30827-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30827-105">DESCRIPTION</span></span>
<span data-ttu-id="30827-106">Cmdleten **Add-AzureRmLoadBalancerProbeConfig** lägger till en PROBE-konfiguration i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="30827-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="30827-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30827-107">EXAMPLES</span></span>

### <span data-ttu-id="30827-108">Exempel 1 lägga till en PROBE-konfiguration till en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="30827-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="30827-109">Det här kommandot får belastningsutjämnaren med namnet myLb, lägger till angiven Avsök-konfiguration i den och använder sedan cmdleten **set-AzureRmLoadBalancer** för att uppdatera belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="30827-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="30827-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30827-110">PARAMETERS</span></span>

### <span data-ttu-id="30827-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30827-111">-DefaultProfile</span></span>
<span data-ttu-id="30827-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30827-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30827-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="30827-113">-IntervalInSeconds</span></span>
<span data-ttu-id="30827-114">Anger intervallet i sekunder mellan avsökningar för varje instans av den belastningsutjämnade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="30827-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="30827-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30827-115">-LoadBalancer</span></span>
<span data-ttu-id="30827-116">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="30827-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="30827-117">Denna cmdlet lägger till en PROBE-konfiguration för belastningsutjämnaren som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="30827-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="30827-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="30827-118">-Name</span></span>
<span data-ttu-id="30827-119">Anger namnet på den PROBE-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="30827-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="30827-120">-Port</span><span class="sxs-lookup"><span data-stu-id="30827-120">-Port</span></span>
<span data-ttu-id="30827-121">Anger vilken port som Avsök ska anslutas till till en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="30827-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="30827-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="30827-122">-ProbeCount</span></span>
<span data-ttu-id="30827-123">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="30827-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="30827-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="30827-124">-Protocol</span></span>
<span data-ttu-id="30827-125">Anger protokollet som ska användas för sonden.</span><span class="sxs-lookup"><span data-stu-id="30827-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="30827-126">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="30827-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="30827-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="30827-127">-RequestPath</span></span>
<span data-ttu-id="30827-128">Anger sökvägen i den belastningsutjämnade tjänsten som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="30827-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="30827-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30827-129">-Confirm</span></span>
<span data-ttu-id="30827-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30827-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30827-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30827-131">-WhatIf</span></span>
<span data-ttu-id="30827-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30827-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30827-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30827-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30827-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30827-134">CommonParameters</span></span>
<span data-ttu-id="30827-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30827-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30827-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30827-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30827-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30827-137">INPUTS</span></span>

### <span data-ttu-id="30827-138">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30827-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="30827-139">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30827-139">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="30827-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30827-140">OUTPUTS</span></span>

### <span data-ttu-id="30827-141">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30827-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="30827-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30827-142">NOTES</span></span>

## <span data-ttu-id="30827-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30827-143">RELATED LINKS</span></span>

[<span data-ttu-id="30827-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30827-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="30827-145">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30827-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="30827-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30827-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="30827-147">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30827-147">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="30827-148">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30827-148">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


