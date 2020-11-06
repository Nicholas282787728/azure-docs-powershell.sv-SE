---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 4929612cd2bb3788bd171f4bb6386c622c4fbbee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585900"
---
# <span data-ttu-id="e9347-101">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9347-101">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="e9347-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9347-102">SYNOPSIS</span></span>
<span data-ttu-id="e9347-103">Skapar ett nytt protokoll konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="e9347-103">Creates a new protocol configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9347-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9347-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9347-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9347-105">DESCRIPTION</span></span>
<span data-ttu-id="e9347-106">New-AzureRmNetworkWatcherProtocolConfiguration cmdlet skapar ett nytt protokoll konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="e9347-106">The New-AzureRmNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="e9347-107">Det här objektet används för att begränsa protokollets confiuration under en connecitivity-incheckning med de angivna villkoren.</span><span class="sxs-lookup"><span data-stu-id="e9347-107">This object is used to restrict the protocol confiuration during a connecitivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="e9347-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9347-108">EXAMPLES</span></span>

### <span data-ttu-id="e9347-109">Exempel 1: testa nätverks övervakaren anslutning från en virtuell dator till en webbplats med protokoll konfiguration</span><span class="sxs-lookup"><span data-stu-id="e9347-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzureRmNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


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

<span data-ttu-id="e9347-110">I det här exemplet testar vi anslutningen från en VM i Azure till www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="e9347-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="e9347-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9347-111">PARAMETERS</span></span>

### <span data-ttu-id="e9347-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9347-112">-DefaultProfile</span></span>
<span data-ttu-id="e9347-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9347-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9347-114">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="e9347-114">-Header</span></span>
<span data-ttu-id="e9347-115">lista över HTTP-rubriker</span><span class="sxs-lookup"><span data-stu-id="e9347-115">list of HTTP headers</span></span>

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

### <span data-ttu-id="e9347-116">-Metod</span><span class="sxs-lookup"><span data-stu-id="e9347-116">-Method</span></span>
<span data-ttu-id="e9347-117">HTTP-metod</span><span class="sxs-lookup"><span data-stu-id="e9347-117">HTTP method</span></span>

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

### <span data-ttu-id="e9347-118">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e9347-118">-Protocol</span></span>
<span data-ttu-id="e9347-119">Procotol typ</span><span class="sxs-lookup"><span data-stu-id="e9347-119">Procotol type</span></span>

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

### <span data-ttu-id="e9347-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="e9347-120">-ValidStatusCode</span></span>
<span data-ttu-id="e9347-121">giltiga status koder</span><span class="sxs-lookup"><span data-stu-id="e9347-121">valid status codes</span></span>

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

### <span data-ttu-id="e9347-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9347-122">CommonParameters</span></span>
<span data-ttu-id="e9347-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9347-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9347-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9347-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9347-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9347-125">INPUTS</span></span>

### <span data-ttu-id="e9347-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="e9347-126">None</span></span>

## <span data-ttu-id="e9347-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9347-127">OUTPUTS</span></span>

### <span data-ttu-id="e9347-128">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9347-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="e9347-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9347-129">NOTES</span></span>
<span data-ttu-id="e9347-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, paket, Capture, trafik, filter</span><span class="sxs-lookup"><span data-stu-id="e9347-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="e9347-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9347-131">RELATED LINKS</span></span>

[<span data-ttu-id="e9347-132">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e9347-132">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e9347-133">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e9347-133">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e9347-134">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e9347-134">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e9347-135">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e9347-135">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="e9347-136">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e9347-136">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e9347-137">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e9347-137">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e9347-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e9347-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e9347-139">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e9347-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e9347-140">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e9347-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="e9347-141">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e9347-141">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e9347-142">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e9347-142">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e9347-143">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e9347-143">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e9347-144">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9347-144">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e9347-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e9347-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e9347-146">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e9347-146">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="e9347-147">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e9347-147">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e9347-148">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e9347-148">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e9347-149">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e9347-149">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e9347-150">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e9347-150">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e9347-151">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e9347-151">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e9347-152">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e9347-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e9347-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e9347-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e9347-154">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e9347-154">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e9347-155">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e9347-155">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e9347-156">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e9347-156">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e9347-157">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e9347-157">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="e9347-158">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e9347-158">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
