---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 7f974d9be1faaaf4d78a2527250cdec1775ae49f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262545"
---
# <span data-ttu-id="fde44-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fde44-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="fde44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fde44-102">SYNOPSIS</span></span>
<span data-ttu-id="fde44-103">Skapar ett nytt protokoll konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="fde44-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="fde44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fde44-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fde44-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fde44-105">DESCRIPTION</span></span>
<span data-ttu-id="fde44-106">New-AzNetworkWatcherProtocolConfiguration cmdlet skapar ett nytt protokoll konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="fde44-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="fde44-107">Det här objektet används för att begränsa protokoll konfigurationen under en anslutnings kontroll med de angivna villkoren.</span><span class="sxs-lookup"><span data-stu-id="fde44-107">This object is used to restrict the protocol configuration during a connectivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="fde44-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fde44-108">EXAMPLES</span></span>

### <span data-ttu-id="fde44-109">Exempel 1: testa nätverks övervakaren anslutning från en virtuell dator till en webbplats med protokoll konfiguration</span><span class="sxs-lookup"><span data-stu-id="fde44-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="fde44-110">I det här exemplet testar vi anslutningen från en VM i Azure till www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="fde44-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="fde44-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fde44-111">PARAMETERS</span></span>

### <span data-ttu-id="fde44-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde44-112">-DefaultProfile</span></span>
<span data-ttu-id="fde44-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fde44-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fde44-114">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="fde44-114">-Header</span></span>
<span data-ttu-id="fde44-115">lista över HTTP-rubriker</span><span class="sxs-lookup"><span data-stu-id="fde44-115">list of HTTP headers</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde44-116">-Metod</span><span class="sxs-lookup"><span data-stu-id="fde44-116">-Method</span></span>
<span data-ttu-id="fde44-117">HTTP-metod</span><span class="sxs-lookup"><span data-stu-id="fde44-117">HTTP method</span></span>

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

### <span data-ttu-id="fde44-118">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="fde44-118">-Protocol</span></span>
<span data-ttu-id="fde44-119">Protokoll typ</span><span class="sxs-lookup"><span data-stu-id="fde44-119">Protocol type</span></span>

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

### <span data-ttu-id="fde44-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="fde44-120">-ValidStatusCode</span></span>
<span data-ttu-id="fde44-121">giltiga status koder</span><span class="sxs-lookup"><span data-stu-id="fde44-121">valid status codes</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde44-122">CommonParameters</span></span>
<span data-ttu-id="fde44-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde44-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde44-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde44-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fde44-125">INPUTS</span></span>

### <span data-ttu-id="fde44-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="fde44-126">None</span></span>

## <span data-ttu-id="fde44-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fde44-127">OUTPUTS</span></span>

### <span data-ttu-id="fde44-128">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fde44-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="fde44-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fde44-129">NOTES</span></span>
<span data-ttu-id="fde44-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, paket, Capture, trafik, filter</span><span class="sxs-lookup"><span data-stu-id="fde44-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="fde44-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fde44-131">RELATED LINKS</span></span>

[<span data-ttu-id="fde44-132">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fde44-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="fde44-133">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fde44-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="fde44-134">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fde44-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="fde44-135">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fde44-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="fde44-136">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fde44-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fde44-137">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fde44-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="fde44-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fde44-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fde44-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fde44-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fde44-140">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fde44-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="fde44-141">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fde44-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fde44-142">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fde44-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fde44-143">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fde44-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fde44-144">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fde44-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="fde44-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fde44-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="fde44-146">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fde44-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="fde44-147">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fde44-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fde44-148">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fde44-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fde44-149">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fde44-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fde44-150">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fde44-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="fde44-151">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fde44-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fde44-152">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fde44-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fde44-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fde44-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="fde44-154">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fde44-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="fde44-155">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fde44-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="fde44-156">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fde44-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fde44-157">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fde44-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="fde44-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fde44-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)