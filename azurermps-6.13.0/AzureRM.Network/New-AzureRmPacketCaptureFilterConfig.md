---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: 3c69884e988b10f41da4d41d98318ee96c019112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585899"
---
# <span data-ttu-id="4612e-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4612e-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="4612e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4612e-102">SYNOPSIS</span></span>
<span data-ttu-id="4612e-103">Skapar ett nytt paket för infångstfilter.</span><span class="sxs-lookup"><span data-stu-id="4612e-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4612e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4612e-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4612e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4612e-105">DESCRIPTION</span></span>
<span data-ttu-id="4612e-106">New-AzureRmPacketCaptureFilterConfig-cmdleten skapar ett nytt paket för Packet Capture-objekt.</span><span class="sxs-lookup"><span data-stu-id="4612e-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="4612e-107">Det här objektet används för att begränsa vilken typ av paket som fångas under en paket upptagning med de angivna villkoren.</span><span class="sxs-lookup"><span data-stu-id="4612e-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="4612e-108">New-AzureRmNetworkWatcherPacketCapture cmdlet kan acceptera flera filter objekt för att aktivera sammanställnings bara infångnings-sessioner.</span><span class="sxs-lookup"><span data-stu-id="4612e-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="4612e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4612e-109">EXAMPLES</span></span>

### <span data-ttu-id="4612e-110">Exempel 1: skapa en paket avbildning med flera filter</span><span class="sxs-lookup"><span data-stu-id="4612e-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="4612e-111">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="4612e-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="4612e-112">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4612e-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="4612e-113">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="4612e-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="4612e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4612e-114">PARAMETERS</span></span>

### <span data-ttu-id="4612e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4612e-115">-DefaultProfile</span></span>
<span data-ttu-id="4612e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4612e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4612e-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="4612e-117">-LocalIPAddress</span></span>
<span data-ttu-id="4612e-118">Anger den lokala IP-adressen som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="4612e-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="4612e-119">Exempel på indata: "127.0.0.1" för post med en enda adress.</span><span class="sxs-lookup"><span data-stu-id="4612e-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="4612e-120">"127.0.0.1-127.0.0.255" för området.</span><span class="sxs-lookup"><span data-stu-id="4612e-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="4612e-121">"127.0.0.1; 127.0.0.5;" för flera poster.</span><span class="sxs-lookup"><span data-stu-id="4612e-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="4612e-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="4612e-122">-LocalPort</span></span>
<span data-ttu-id="4612e-123">Anger den lokala IP-adressen som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="4612e-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="4612e-124">Exempel på indata: "127.0.0.1" för post med en enda adress.</span><span class="sxs-lookup"><span data-stu-id="4612e-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="4612e-125">"127.0.0.1-127.0.0.255" för området.</span><span class="sxs-lookup"><span data-stu-id="4612e-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="4612e-126">"127.0.0.1; 127.0.0.5;" för flera poster.</span><span class="sxs-lookup"><span data-stu-id="4612e-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="4612e-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4612e-127">-Protocol</span></span>
<span data-ttu-id="4612e-128">Anger vilken Procotol som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="4612e-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="4612e-129">Acceptabla värden "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="4612e-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="4612e-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="4612e-130">-RemoteIPAddress</span></span>
<span data-ttu-id="4612e-131">Anger vilken fjärr-IP-adress som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="4612e-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="4612e-132">Exempel på indata: "127.0.0.1" för post med en enda adress.</span><span class="sxs-lookup"><span data-stu-id="4612e-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="4612e-133">"127.0.0.1-127.0.0.255" för området.</span><span class="sxs-lookup"><span data-stu-id="4612e-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="4612e-134">"127.0.0.1; 127.0.0.5;" för flera poster.</span><span class="sxs-lookup"><span data-stu-id="4612e-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="4612e-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="4612e-135">-RemotePort</span></span>
<span data-ttu-id="4612e-136">Anger vilken fjärr porten som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="4612e-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="4612e-137">Exempel på Fjärrport: "80" för en enskild port.</span><span class="sxs-lookup"><span data-stu-id="4612e-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="4612e-138">"80-85" för området.</span><span class="sxs-lookup"><span data-stu-id="4612e-138">"80-85" for range.</span></span>
<span data-ttu-id="4612e-139">"80; 443;" för flera poster.</span><span class="sxs-lookup"><span data-stu-id="4612e-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="4612e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4612e-140">CommonParameters</span></span>
<span data-ttu-id="4612e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4612e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4612e-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4612e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4612e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4612e-143">INPUTS</span></span>

### <span data-ttu-id="4612e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4612e-144">System.String</span></span>
<span data-ttu-id="4612e-145">Parametrar: Protocol (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4612e-145">Parameters: Protocol (ByValue)</span></span>

## <span data-ttu-id="4612e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4612e-146">OUTPUTS</span></span>

### <span data-ttu-id="4612e-147">Microsoft. Azure. commands. Networks. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="4612e-147">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="4612e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4612e-148">NOTES</span></span>
<span data-ttu-id="4612e-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, paket, Capture, trafik, filter</span><span class="sxs-lookup"><span data-stu-id="4612e-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="4612e-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4612e-150">RELATED LINKS</span></span>

[<span data-ttu-id="4612e-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4612e-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4612e-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4612e-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4612e-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4612e-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4612e-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4612e-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4612e-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4612e-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4612e-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4612e-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4612e-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4612e-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4612e-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4612e-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4612e-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4612e-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4612e-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4612e-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4612e-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4612e-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4612e-162">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4612e-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4612e-163">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4612e-163">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4612e-164">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4612e-164">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4612e-165">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4612e-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="4612e-166">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4612e-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4612e-167">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4612e-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4612e-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4612e-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4612e-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4612e-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4612e-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4612e-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4612e-171">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4612e-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4612e-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4612e-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4612e-173">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4612e-173">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4612e-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4612e-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4612e-175">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4612e-175">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4612e-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4612e-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4612e-177">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4612e-177">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
