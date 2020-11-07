---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 57c0d491d5e330f45550381b099e20e5d02fd8f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756918"
---
# <span data-ttu-id="4c8f3-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4c8f3-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="4c8f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4c8f3-103">Skapar en PROBE-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c8f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c8f3-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c8f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c8f3-105">DESCRIPTION</span></span>
<span data-ttu-id="4c8f3-106">Cmdleten **New-AzureRmLoadBalancerProbeConfig** skapar en PROBE-konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="4c8f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c8f3-107">EXAMPLES</span></span>

### <span data-ttu-id="4c8f3-108">Exempel 1: skapa en PROBE-konfiguration</span><span class="sxs-lookup"><span data-stu-id="4c8f3-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="4c8f3-109">Det här kommandot skapar en PROBE-konfiguration med namnet min PROBE med HTTP-protokollet.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="4c8f3-110">Den nya avsökningen ansluter till en belastningsutjämnad tjänst på port 80.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="4c8f3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c8f3-111">PARAMETERS</span></span>

### <span data-ttu-id="4c8f3-112">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4c8f3-112">-IntervalInSeconds</span></span>
<span data-ttu-id="4c8f3-113">Anger intervallet i sekunder mellan avsökningar för varje instans av en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-113">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="4c8f3-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c8f3-114">-Name</span></span>
<span data-ttu-id="4c8f3-115">Anger namnet på den PROBE-konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-115">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="4c8f3-116">-Port</span><span class="sxs-lookup"><span data-stu-id="4c8f3-116">-Port</span></span>
<span data-ttu-id="4c8f3-117">Anger den port som den nya avvägdheten ska anslutas till med en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-117">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="4c8f3-118">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="4c8f3-118">-ProbeCount</span></span>
<span data-ttu-id="4c8f3-119">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-119">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="4c8f3-120">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4c8f3-120">-Protocol</span></span>
<span data-ttu-id="4c8f3-121">Anger protokollet som ska användas för sondens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-121">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="4c8f3-122">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-122">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="4c8f3-123">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="4c8f3-123">-RequestPath</span></span>
<span data-ttu-id="4c8f3-124">Anger sökvägen i en belastningsutjämnad tjänst som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-124">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="4c8f3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c8f3-125">-DefaultProfile</span></span>
<span data-ttu-id="4c8f3-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c8f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c8f3-127">CommonParameters</span></span>
<span data-ttu-id="4c8f3-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c8f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c8f3-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c8f3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c8f3-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c8f3-130">INPUTS</span></span>

## <span data-ttu-id="4c8f3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c8f3-131">OUTPUTS</span></span>

### <span data-ttu-id="4c8f3-132">Microsoft. Azure. commands. Networks. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="4c8f3-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="4c8f3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c8f3-133">NOTES</span></span>

## <span data-ttu-id="4c8f3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c8f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="4c8f3-135">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4c8f3-135">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="4c8f3-136">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4c8f3-136">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="4c8f3-137">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4c8f3-137">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="4c8f3-138">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4c8f3-138">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


