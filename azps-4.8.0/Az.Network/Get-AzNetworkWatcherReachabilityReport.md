---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258797"
---
# <span data-ttu-id="a4ec3-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a4ec3-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="a4ec3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ec3-103">Hämtar den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="a4ec3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4ec3-104">SYNTAX</span></span>

### <span data-ttu-id="a4ec3-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a4ec3-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ec3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a4ec3-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ec3-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a4ec3-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4ec3-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a4ec3-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4ec3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4ec3-109">DESCRIPTION</span></span>
<span data-ttu-id="a4ec3-110">Get-AzNetworkWatcherReachabilityReport får den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="a4ec3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4ec3-111">EXAMPLES</span></span>

### <span data-ttu-id="a4ec3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4ec3-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="a4ec3-113">Hämtar relativa fördröjningar till Azure Data Center i väster från 2017-10-10 till 2017-10-12 i USA.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="a4ec3-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a4ec3-114">Example 2</span></span>

<span data-ttu-id="a4ec3-115">Hämtar den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="a4ec3-116">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="a4ec3-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="a4ec3-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4ec3-117">PARAMETERS</span></span>

### <span data-ttu-id="a4ec3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4ec3-118">-AsJob</span></span>
<span data-ttu-id="a4ec3-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a4ec3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4ec3-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="a4ec3-120">-City</span></span>
<span data-ttu-id="a4ec3-121">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-121">The name of the city.</span></span>

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

### <span data-ttu-id="a4ec3-122">-Country</span><span class="sxs-lookup"><span data-stu-id="a4ec3-122">-Country</span></span>
<span data-ttu-id="a4ec3-123">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-123">The name of the country.</span></span>

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

### <span data-ttu-id="a4ec3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ec3-124">-DefaultProfile</span></span>
<span data-ttu-id="a4ec3-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4ec3-126">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="a4ec3-126">-EndTime</span></span>
<span data-ttu-id="a4ec3-127">Slut tiden för Azure REACH-rapporten.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="a4ec3-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="a4ec3-128">-Location</span></span>
<span data-ttu-id="a4ec3-129">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="a4ec3-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4ec3-130">-NetworkWatcher</span></span>
<span data-ttu-id="a4ec3-131">Nätverks Watcher-resursen</span><span class="sxs-lookup"><span data-stu-id="a4ec3-131">The network watcher resource</span></span>

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

### <span data-ttu-id="a4ec3-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="a4ec3-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="a4ec3-133">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a4ec3-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a4ec3-134">-NetworkWatcherName</span></span>
<span data-ttu-id="a4ec3-135">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="a4ec3-136">-Leverantör</span><span class="sxs-lookup"><span data-stu-id="a4ec3-136">-Provider</span></span>
<span data-ttu-id="a4ec3-137">Lista över Internet leverantörer.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="a4ec3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ec3-138">-ResourceGroupName</span></span>
<span data-ttu-id="a4ec3-139">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a4ec3-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4ec3-140">-ResourceId</span></span>
<span data-ttu-id="a4ec3-141">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="a4ec3-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a4ec3-142">-StartTime</span></span>
<span data-ttu-id="a4ec3-143">Start tiden för rapporten för Azure-tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="a4ec3-144">-State</span><span class="sxs-lookup"><span data-stu-id="a4ec3-144">-State</span></span>
<span data-ttu-id="a4ec3-145">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-145">The name of the state.</span></span>

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

### <span data-ttu-id="a4ec3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ec3-146">CommonParameters</span></span>
<span data-ttu-id="a4ec3-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ec3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ec3-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4ec3-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ec3-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4ec3-149">INPUTS</span></span>

### <span data-ttu-id="a4ec3-150">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4ec3-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a4ec3-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ec3-151">System.String</span></span>

## <span data-ttu-id="a4ec3-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4ec3-152">OUTPUTS</span></span>

### <span data-ttu-id="a4ec3-153">Microsoft. Azure. commands. Networks. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a4ec3-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="a4ec3-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4ec3-154">NOTES</span></span>
<span data-ttu-id="a4ec3-155">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, tillgänglighet, rapport</span><span class="sxs-lookup"><span data-stu-id="a4ec3-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="a4ec3-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4ec3-156">RELATED LINKS</span></span>

[<span data-ttu-id="a4ec3-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4ec3-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a4ec3-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4ec3-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a4ec3-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4ec3-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a4ec3-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a4ec3-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a4ec3-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a4ec3-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a4ec3-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a4ec3-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a4ec3-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a4ec3-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a4ec3-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a4ec3-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a4ec3-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a4ec3-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a4ec3-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a4ec3-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a4ec3-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a4ec3-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a4ec3-168">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a4ec3-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a4ec3-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4ec3-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a4ec3-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a4ec3-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a4ec3-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a4ec3-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a4ec3-172">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a4ec3-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a4ec3-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a4ec3-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a4ec3-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a4ec3-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a4ec3-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a4ec3-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a4ec3-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a4ec3-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a4ec3-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a4ec3-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a4ec3-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a4ec3-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a4ec3-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a4ec3-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a4ec3-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a4ec3-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a4ec3-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a4ec3-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a4ec3-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a4ec3-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a4ec3-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a4ec3-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)