---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 09d75e73cc6139bfa2c3d0d6293b07060a709f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757575"
---
# <span data-ttu-id="7be86-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7be86-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="7be86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7be86-102">SYNOPSIS</span></span>
<span data-ttu-id="7be86-103">Hämtar den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="7be86-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7be86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7be86-104">SYNTAX</span></span>

### <span data-ttu-id="7be86-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="7be86-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7be86-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7be86-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7be86-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7be86-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7be86-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7be86-108">SetByLocation</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherLocation <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7be86-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7be86-109">DESCRIPTION</span></span>
<span data-ttu-id="7be86-110">Get-AzureRmNetworkWatcherReachabilityReport får den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="7be86-110">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="7be86-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7be86-111">EXAMPLES</span></span>

### <span data-ttu-id="7be86-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7be86-112">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="7be86-113">Hämtar relativa fördröjningar till Azure Data Center i väster från 2017-10-10 till 2017-10-12 i USA.</span><span class="sxs-lookup"><span data-stu-id="7be86-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="7be86-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7be86-114">PARAMETERS</span></span>

### <span data-ttu-id="7be86-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7be86-115">-AsJob</span></span>
<span data-ttu-id="7be86-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7be86-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7be86-117">-Ort</span><span class="sxs-lookup"><span data-stu-id="7be86-117">-City</span></span>
<span data-ttu-id="7be86-118">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="7be86-118">The name of the city.</span></span>

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

### <span data-ttu-id="7be86-119">-Country</span><span class="sxs-lookup"><span data-stu-id="7be86-119">-Country</span></span>
<span data-ttu-id="7be86-120">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="7be86-120">The name of the country.</span></span>

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

### <span data-ttu-id="7be86-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be86-121">-DefaultProfile</span></span>
<span data-ttu-id="7be86-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7be86-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7be86-123">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="7be86-123">-EndTime</span></span>
<span data-ttu-id="7be86-124">Slut tiden för Azure REACH-rapporten.</span><span class="sxs-lookup"><span data-stu-id="7be86-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="7be86-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="7be86-125">-Location</span></span>
<span data-ttu-id="7be86-126">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="7be86-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be86-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be86-127">-NetworkWatcher</span></span>
<span data-ttu-id="7be86-128">Nätverks Watcher-resursen</span><span class="sxs-lookup"><span data-stu-id="7be86-128">The network watcher resource</span></span>

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

### <span data-ttu-id="7be86-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="7be86-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="7be86-130">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="7be86-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7be86-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7be86-131">-NetworkWatcherName</span></span>
<span data-ttu-id="7be86-132">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="7be86-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="7be86-133">-Leverantör</span><span class="sxs-lookup"><span data-stu-id="7be86-133">-Provider</span></span>
<span data-ttu-id="7be86-134">Lista över Internet leverantörer.</span><span class="sxs-lookup"><span data-stu-id="7be86-134">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be86-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be86-135">-ResourceGroupName</span></span>
<span data-ttu-id="7be86-136">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7be86-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7be86-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7be86-137">-ResourceId</span></span>
<span data-ttu-id="7be86-138">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="7be86-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="7be86-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7be86-139">-StartTime</span></span>
<span data-ttu-id="7be86-140">Start tiden för rapporten för Azure-tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="7be86-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="7be86-141">-State</span><span class="sxs-lookup"><span data-stu-id="7be86-141">-State</span></span>
<span data-ttu-id="7be86-142">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="7be86-142">The name of the state.</span></span>

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

### <span data-ttu-id="7be86-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be86-143">CommonParameters</span></span>
<span data-ttu-id="7be86-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7be86-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be86-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7be86-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be86-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7be86-146">INPUTS</span></span>

### <span data-ttu-id="7be86-147">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be86-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7be86-148">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7be86-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="7be86-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7be86-149">System.String</span></span>

## <span data-ttu-id="7be86-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7be86-150">OUTPUTS</span></span>

### <span data-ttu-id="7be86-151">Microsoft. Azure. commands. Networks. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7be86-151">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="7be86-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7be86-152">NOTES</span></span>
<span data-ttu-id="7be86-153">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, tillgänglighet, rapport</span><span class="sxs-lookup"><span data-stu-id="7be86-153">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="7be86-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7be86-154">RELATED LINKS</span></span>

[<span data-ttu-id="7be86-155">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be86-155">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7be86-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be86-156">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7be86-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7be86-157">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7be86-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7be86-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7be86-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7be86-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7be86-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7be86-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7be86-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7be86-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7be86-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7be86-162">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7be86-163">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7be86-163">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7be86-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7be86-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7be86-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7be86-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7be86-166">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7be86-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7be86-167">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7be86-167">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7be86-168">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7be86-168">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7be86-169">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7be86-169">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="7be86-170">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be86-170">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be86-171">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be86-171">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be86-172">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be86-172">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be86-173">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7be86-173">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7be86-174">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be86-174">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be86-175">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be86-175">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7be86-176">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7be86-176">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7be86-177">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7be86-177">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7be86-178">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7be86-178">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7be86-179">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7be86-179">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7be86-180">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7be86-180">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="7be86-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7be86-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
