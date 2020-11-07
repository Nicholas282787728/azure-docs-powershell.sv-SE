---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 0e5216f88cc860244cf11a693a73e30ba6e83390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580344"
---
# <span data-ttu-id="f812d-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f812d-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="f812d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f812d-102">SYNOPSIS</span></span>
<span data-ttu-id="f812d-103">Skapar en PROBE-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="f812d-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f812d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f812d-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f812d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f812d-105">DESCRIPTION</span></span>
<span data-ttu-id="f812d-106">Cmdleten **New-AzureRmLoadBalancerProbeConfig** skapar en PROBE-konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f812d-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f812d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f812d-107">EXAMPLES</span></span>

### <span data-ttu-id="f812d-108">Exempel 1: skapa en PROBE-konfiguration</span><span class="sxs-lookup"><span data-stu-id="f812d-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="f812d-109">Det här kommandot skapar en PROBE-konfiguration med namnet min PROBE med HTTP-protokollet.</span><span class="sxs-lookup"><span data-stu-id="f812d-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="f812d-110">Den nya avsökningen ansluter till en belastningsutjämnad tjänst på port 80.</span><span class="sxs-lookup"><span data-stu-id="f812d-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="f812d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f812d-111">PARAMETERS</span></span>

### <span data-ttu-id="f812d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f812d-112">-DefaultProfile</span></span>
<span data-ttu-id="f812d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f812d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f812d-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f812d-114">-IntervalInSeconds</span></span>
<span data-ttu-id="f812d-115">Anger intervallet i sekunder mellan avsökningar för varje instans av en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="f812d-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="f812d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="f812d-116">-Name</span></span>
<span data-ttu-id="f812d-117">Anger namnet på den PROBE-konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f812d-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="f812d-118">-Port</span><span class="sxs-lookup"><span data-stu-id="f812d-118">-Port</span></span>
<span data-ttu-id="f812d-119">Anger den port som den nya avvägdheten ska anslutas till med en belastningsutjämnad tjänst.</span><span class="sxs-lookup"><span data-stu-id="f812d-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="f812d-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="f812d-120">-ProbeCount</span></span>
<span data-ttu-id="f812d-121">Anger antalet enskilda förekomster av varje instans för att en instans ska betraktas som ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="f812d-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="f812d-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f812d-122">-Protocol</span></span>
<span data-ttu-id="f812d-123">Anger protokollet som ska användas för sondens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f812d-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="f812d-124">De acceptabla värdena för denna parameter är: TCP eller http.</span><span class="sxs-lookup"><span data-stu-id="f812d-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="f812d-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="f812d-125">-RequestPath</span></span>
<span data-ttu-id="f812d-126">Anger sökvägen i en belastningsutjämnad tjänst som ska avsökas för att fastställa hälsa.</span><span class="sxs-lookup"><span data-stu-id="f812d-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="f812d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f812d-127">CommonParameters</span></span>
<span data-ttu-id="f812d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f812d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f812d-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f812d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f812d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f812d-130">INPUTS</span></span>

### <span data-ttu-id="f812d-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="f812d-131">None</span></span>
<span data-ttu-id="f812d-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f812d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f812d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f812d-133">OUTPUTS</span></span>

### <span data-ttu-id="f812d-134">Microsoft. Azure. commands. Networks. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="f812d-134">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="f812d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f812d-135">NOTES</span></span>

## <span data-ttu-id="f812d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f812d-136">RELATED LINKS</span></span>

[<span data-ttu-id="f812d-137">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f812d-137">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="f812d-138">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f812d-138">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="f812d-139">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f812d-139">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="f812d-140">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f812d-140">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)

