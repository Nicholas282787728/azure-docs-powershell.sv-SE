---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 60c54895d4bff7f8825964b32c96e2d3c8b69798
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925817"
---
# <span data-ttu-id="e9f72-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9f72-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e9f72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9f72-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f72-103">Skapar en PROBE-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e9f72-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="e9f72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9f72-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9f72-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9f72-105">DESCRIPTION</span></span>
<span data-ttu-id="e9f72-106">Cmdleten **New-AzLoadBalancerProbeConfig** skapar en PROBE-konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="e9f72-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e9f72-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9f72-107">EXAMPLES</span></span>

### <span data-ttu-id="e9f72-108">Exempel 1: skapa en PROBE-konfiguration</span><span class="sxs-lookup"><span data-stu-id="e9f72-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="e9f72-109">Det här kommandot skapar en PROBE-konfiguration med namnet min PROBE med HTTP-protokollet.</span><span class="sxs-lookup"><span data-stu-id="e9f72-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="e9f72-110">Den nya avsökningen ansluter till en belastningsutjämnad tjänst på port 80.</span><span class="sxs-lookup"><span data-stu-id="e9f72-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="e9f72-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9f72-111">PARAMETERS</span></span>

### <span data-ttu-id="e9f72-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f72-112">-DefaultProfile</span></span>
<span data-ttu-id="e9f72-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9f72-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9f72-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e9f72-114">-IntervalInSeconds</span></span>
<span data-ttu-id="e9f72-115">Anger intervallet i sekunder mellan avsökningar för varje instans av en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="e9f72-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="e9f72-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9f72-116">-Name</span></span>
<span data-ttu-id="e9f72-117">Anger namnet på den PROBE-konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e9f72-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="e9f72-118">-Port</span><span class="sxs-lookup"><span data-stu-id="e9f72-118">-Port</span></span>
<span data-ttu-id="e9f72-119">Anger den port som den nya avvägdheten ska anslutas till med en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="e9f72-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="e9f72-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="e9f72-120">-ProbeCount</span></span>
<span data-ttu-id="e9f72-121">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="e9f72-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="e9f72-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e9f72-122">-Protocol</span></span>
<span data-ttu-id="e9f72-123">Anger protokollet som ska användas för sondens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e9f72-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="e9f72-124">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="e9f72-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="e9f72-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="e9f72-125">-RequestPath</span></span>
<span data-ttu-id="e9f72-126">Anger sökvägen i en belastningsutjämnad tjänst som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="e9f72-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="e9f72-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9f72-127">-Confirm</span></span>
<span data-ttu-id="e9f72-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9f72-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f72-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f72-129">-WhatIf</span></span>
<span data-ttu-id="e9f72-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9f72-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9f72-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9f72-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f72-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f72-132">CommonParameters</span></span>
<span data-ttu-id="e9f72-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f72-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f72-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f72-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f72-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9f72-135">INPUTS</span></span>

### <span data-ttu-id="e9f72-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e9f72-136">System.String</span></span>

### <span data-ttu-id="e9f72-137">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e9f72-137">System.Int32</span></span>

## <span data-ttu-id="e9f72-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9f72-138">OUTPUTS</span></span>

### <span data-ttu-id="e9f72-139">Microsoft. Azure. commands. Networks. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="e9f72-139">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="e9f72-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9f72-140">NOTES</span></span>

## <span data-ttu-id="e9f72-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9f72-141">RELATED LINKS</span></span>

[<span data-ttu-id="e9f72-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9f72-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e9f72-143">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9f72-143">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e9f72-144">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9f72-144">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e9f72-145">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e9f72-145">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


