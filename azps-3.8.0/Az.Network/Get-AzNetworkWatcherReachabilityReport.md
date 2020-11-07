---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 0ad2b1fa6278e085a57d94f2fec9be2c6853993d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926493"
---
# <span data-ttu-id="c1a1f-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c1a1f-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="c1a1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a1f-103">Hämtar den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="c1a1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1a1f-104">SYNTAX</span></span>

### <span data-ttu-id="c1a1f-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="c1a1f-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a1f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c1a1f-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a1f-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1a1f-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1a1f-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c1a1f-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1a1f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1a1f-109">DESCRIPTION</span></span>
<span data-ttu-id="c1a1f-110">Get-AzNetworkWatcherReachabilityReport får den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="c1a1f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1a1f-111">EXAMPLES</span></span>

### <span data-ttu-id="c1a1f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c1a1f-112">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="c1a1f-113">Hämtar relativa fördröjningar till Azure Data Center i väster från 2017-10-10 till 2017-10-12 i USA.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="c1a1f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1a1f-114">PARAMETERS</span></span>

### <span data-ttu-id="c1a1f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1a1f-115">-AsJob</span></span>
<span data-ttu-id="c1a1f-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c1a1f-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-117">-Ort</span><span class="sxs-lookup"><span data-stu-id="c1a1f-117">-City</span></span>
<span data-ttu-id="c1a1f-118">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-118">The name of the city.</span></span>

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

### <span data-ttu-id="c1a1f-119">-Country</span><span class="sxs-lookup"><span data-stu-id="c1a1f-119">-Country</span></span>
<span data-ttu-id="c1a1f-120">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-120">The name of the country.</span></span>

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

### <span data-ttu-id="c1a1f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a1f-121">-DefaultProfile</span></span>
<span data-ttu-id="c1a1f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1a1f-123">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="c1a1f-123">-EndTime</span></span>
<span data-ttu-id="c1a1f-124">Slut tiden för Azure REACH-rapporten.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-124">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="c1a1f-125">-Location</span></span>
<span data-ttu-id="c1a1f-126">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1a1f-127">-NetworkWatcher</span></span>
<span data-ttu-id="c1a1f-128">Nätverks Watcher-resursen</span><span class="sxs-lookup"><span data-stu-id="c1a1f-128">The network watcher resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="c1a1f-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="c1a1f-130">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-130">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c1a1f-131">-NetworkWatcherName</span></span>
<span data-ttu-id="c1a1f-132">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-132">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-133">-Leverantör</span><span class="sxs-lookup"><span data-stu-id="c1a1f-133">-Provider</span></span>
<span data-ttu-id="c1a1f-134">Lista över Internet leverantörer.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-134">List of Internet service providers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a1f-135">-ResourceGroupName</span></span>
<span data-ttu-id="c1a1f-136">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-136">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1a1f-137">-ResourceId</span></span>
<span data-ttu-id="c1a1f-138">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-138">The Id of network watcher resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c1a1f-139">-StartTime</span></span>
<span data-ttu-id="c1a1f-140">Start tiden för rapporten för Azure-tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-140">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a1f-141">-State</span><span class="sxs-lookup"><span data-stu-id="c1a1f-141">-State</span></span>
<span data-ttu-id="c1a1f-142">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-142">The name of the state.</span></span>

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

### <span data-ttu-id="c1a1f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a1f-143">CommonParameters</span></span>
<span data-ttu-id="c1a1f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a1f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a1f-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1a1f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a1f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1a1f-146">INPUTS</span></span>

### <span data-ttu-id="c1a1f-147">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1a1f-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c1a1f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c1a1f-148">System.String</span></span>

## <span data-ttu-id="c1a1f-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1a1f-149">OUTPUTS</span></span>

### <span data-ttu-id="c1a1f-150">Microsoft. Azure. commands. Networks. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c1a1f-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="c1a1f-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1a1f-151">NOTES</span></span>
<span data-ttu-id="c1a1f-152">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, tillgänglighet, rapport</span><span class="sxs-lookup"><span data-stu-id="c1a1f-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="c1a1f-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1a1f-153">RELATED LINKS</span></span>

[<span data-ttu-id="c1a1f-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1a1f-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c1a1f-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1a1f-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c1a1f-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1a1f-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c1a1f-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c1a1f-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c1a1f-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c1a1f-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c1a1f-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c1a1f-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c1a1f-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c1a1f-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c1a1f-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c1a1f-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c1a1f-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c1a1f-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c1a1f-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c1a1f-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c1a1f-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c1a1f-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c1a1f-165">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c1a1f-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c1a1f-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1a1f-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c1a1f-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c1a1f-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c1a1f-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c1a1f-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c1a1f-169">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1a1f-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1a1f-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1a1f-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1a1f-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1a1f-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1a1f-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c1a1f-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c1a1f-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1a1f-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1a1f-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1a1f-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1a1f-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c1a1f-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c1a1f-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c1a1f-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c1a1f-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c1a1f-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c1a1f-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c1a1f-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c1a1f-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c1a1f-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c1a1f-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1a1f-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)