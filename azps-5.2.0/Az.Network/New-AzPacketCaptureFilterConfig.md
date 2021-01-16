---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 194e3c71cc763aeb74091f912b37dd15e4dfe4aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395056"
---
# <span data-ttu-id="2452d-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2452d-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="2452d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2452d-102">SYNOPSIS</span></span>
<span data-ttu-id="2452d-103">Skapar ett nytt paket för infångstfilter.</span><span class="sxs-lookup"><span data-stu-id="2452d-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="2452d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2452d-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2452d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2452d-105">DESCRIPTION</span></span>
<span data-ttu-id="2452d-106">New-AzPacketCaptureFilterConfig-cmdleten skapar ett nytt paket för Packet Capture-objekt.</span><span class="sxs-lookup"><span data-stu-id="2452d-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="2452d-107">Det här objektet används för att begränsa vilken typ av paket som fångas under en paket upptagning med de angivna villkoren.</span><span class="sxs-lookup"><span data-stu-id="2452d-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="2452d-108">New-AzNetworkWatcherPacketCapture cmdlet kan acceptera flera filter objekt för att aktivera sammanställnings bara infångnings-sessioner.</span><span class="sxs-lookup"><span data-stu-id="2452d-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="2452d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2452d-109">EXAMPLES</span></span>

### <span data-ttu-id="2452d-110">Exempel 1: skapa en paket avbildning med flera filter</span><span class="sxs-lookup"><span data-stu-id="2452d-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="2452d-111">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="2452d-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="2452d-112">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="2452d-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="2452d-113">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="2452d-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="2452d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2452d-114">PARAMETERS</span></span>

### <span data-ttu-id="2452d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2452d-115">-DefaultProfile</span></span>
<span data-ttu-id="2452d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2452d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2452d-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="2452d-117">-LocalIPAddress</span></span>
<span data-ttu-id="2452d-118">Anger den lokala IP-adressen som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="2452d-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="2452d-119">Exempel på indata: "127.0.0.1" för post med en enda adress.</span><span class="sxs-lookup"><span data-stu-id="2452d-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="2452d-120">"127.0.0.1-127.0.0.255" för området.</span><span class="sxs-lookup"><span data-stu-id="2452d-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="2452d-121">"127.0.0.1; 127.0.0.5;" för flera poster.</span><span class="sxs-lookup"><span data-stu-id="2452d-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="2452d-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="2452d-122">-LocalPort</span></span>
<span data-ttu-id="2452d-123">Anger den lokala IP-adressen som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="2452d-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="2452d-124">Exempel på indata: "127.0.0.1" för post med en enda adress.</span><span class="sxs-lookup"><span data-stu-id="2452d-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="2452d-125">"127.0.0.1-127.0.0.255" för området.</span><span class="sxs-lookup"><span data-stu-id="2452d-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="2452d-126">"127.0.0.1; 127.0.0.5;" för flera poster.</span><span class="sxs-lookup"><span data-stu-id="2452d-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="2452d-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2452d-127">-Protocol</span></span>
<span data-ttu-id="2452d-128">Anger protokollet som ska filtreras på.</span><span class="sxs-lookup"><span data-stu-id="2452d-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="2452d-129">Acceptabla värden "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="2452d-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2452d-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="2452d-130">-RemoteIPAddress</span></span>
<span data-ttu-id="2452d-131">Anger vilken fjärr-IP-adress som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="2452d-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="2452d-132">Exempel på indata: "127.0.0.1" för post med en enda adress.</span><span class="sxs-lookup"><span data-stu-id="2452d-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="2452d-133">"127.0.0.1-127.0.0.255" för området.</span><span class="sxs-lookup"><span data-stu-id="2452d-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="2452d-134">"127.0.0.1; 127.0.0.5;" för flera poster.</span><span class="sxs-lookup"><span data-stu-id="2452d-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="2452d-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="2452d-135">-RemotePort</span></span>
<span data-ttu-id="2452d-136">Anger vilken fjärr porten som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="2452d-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="2452d-137">Exempel på Fjärrport: "80" för en enskild port.</span><span class="sxs-lookup"><span data-stu-id="2452d-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="2452d-138">"80-85" för området.</span><span class="sxs-lookup"><span data-stu-id="2452d-138">"80-85" for range.</span></span>
<span data-ttu-id="2452d-139">"80; 443;" för flera poster.</span><span class="sxs-lookup"><span data-stu-id="2452d-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="2452d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2452d-140">CommonParameters</span></span>
<span data-ttu-id="2452d-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2452d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2452d-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2452d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2452d-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2452d-143">INPUTS</span></span>

### <span data-ttu-id="2452d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2452d-144">System.String</span></span>

## <span data-ttu-id="2452d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2452d-145">OUTPUTS</span></span>

### <span data-ttu-id="2452d-146">Microsoft. Azure. commands. Networks. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="2452d-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="2452d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2452d-147">NOTES</span></span>
<span data-ttu-id="2452d-148">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, paket, Capture, trafik, filter</span><span class="sxs-lookup"><span data-stu-id="2452d-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="2452d-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2452d-149">RELATED LINKS</span></span>

[<span data-ttu-id="2452d-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2452d-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2452d-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2452d-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2452d-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2452d-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2452d-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2452d-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2452d-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2452d-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2452d-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2452d-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2452d-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2452d-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2452d-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2452d-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2452d-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2452d-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2452d-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2452d-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2452d-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2452d-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2452d-161">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2452d-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2452d-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2452d-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2452d-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2452d-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2452d-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2452d-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2452d-165">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2452d-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2452d-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2452d-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2452d-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2452d-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2452d-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2452d-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2452d-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2452d-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2452d-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2452d-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2452d-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2452d-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2452d-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2452d-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2452d-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2452d-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2452d-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2452d-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2452d-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2452d-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2452d-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2452d-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
