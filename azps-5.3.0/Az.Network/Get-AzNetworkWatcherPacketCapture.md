---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1276a3c63ec4b9c4ec1c2c4c91ea792013cbacc9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523403"
---
# <span data-ttu-id="a20b1-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a20b1-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a20b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a20b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a20b1-103">Hämtar information och egenskaper och status för en paket infångnings resurs.</span><span class="sxs-lookup"><span data-stu-id="a20b1-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a20b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a20b1-104">SYNTAX</span></span>

### <span data-ttu-id="a20b1-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="a20b1-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a20b1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a20b1-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a20b1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a20b1-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a20b1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a20b1-108">DESCRIPTION</span></span>
<span data-ttu-id="a20b1-109">Get-AzNetworkWatcherPacketCapture hämtar egenskaper och status för en paket infångnings resurs.</span><span class="sxs-lookup"><span data-stu-id="a20b1-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a20b1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a20b1-110">EXAMPLES</span></span>

### <span data-ttu-id="a20b1-111">Exempel 1: skapa en paket avbildning med flera filter och hämta dess status</span><span class="sxs-lookup"><span data-stu-id="a20b1-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a20b1-112">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="a20b1-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="a20b1-113">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a20b1-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="a20b1-114">Vi ringer sedan Get-AzNetworkWatcherPacketCapture för att hämta statusen för insamlingsbufferten.</span><span class="sxs-lookup"><span data-stu-id="a20b1-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="a20b1-115">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="a20b1-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="a20b1-116">Om du skapar en referens till Packet Capture direkt från kommandot New-AzNetworkWatcherPacketCapture har den inga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a20b1-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="a20b1-117">Du kan hämta alla egenskaper för paket fångsten genom att ringa ett samtal till kommandot Get-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="a20b1-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="a20b1-118">Exempel 2: skapa en paket avbildning med flera filter och hämta dess status</span><span class="sxs-lookup"><span data-stu-id="a20b1-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="a20b1-119">Denna cmdlet returnerar alla PacketCaptures som börjar med "PacketCapture" i NW1-klockan.</span><span class="sxs-lookup"><span data-stu-id="a20b1-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="a20b1-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a20b1-120">PARAMETERS</span></span>

### <span data-ttu-id="a20b1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a20b1-121">-AsJob</span></span>
<span data-ttu-id="a20b1-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a20b1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a20b1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20b1-123">-DefaultProfile</span></span>
<span data-ttu-id="a20b1-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a20b1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a20b1-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="a20b1-125">-Location</span></span>
<span data-ttu-id="a20b1-126">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="a20b1-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a20b1-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a20b1-127">-NetworkWatcher</span></span>
<span data-ttu-id="a20b1-128">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="a20b1-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="a20b1-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a20b1-129">-NetworkWatcherName</span></span>
<span data-ttu-id="a20b1-130">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="a20b1-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a20b1-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a20b1-131">-PacketCaptureName</span></span>
<span data-ttu-id="a20b1-132">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="a20b1-132">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a20b1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a20b1-133">-ResourceGroupName</span></span>
<span data-ttu-id="a20b1-134">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a20b1-134">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a20b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20b1-135">CommonParameters</span></span>
<span data-ttu-id="a20b1-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20b1-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a20b1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20b1-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a20b1-138">INPUTS</span></span>

### <span data-ttu-id="a20b1-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a20b1-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a20b1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a20b1-140">System.String</span></span>

## <span data-ttu-id="a20b1-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a20b1-141">OUTPUTS</span></span>

### <span data-ttu-id="a20b1-142">Microsoft. Azure. commands. Networks. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a20b1-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="a20b1-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a20b1-143">NOTES</span></span>
<span data-ttu-id="a20b1-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="a20b1-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="a20b1-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a20b1-145">RELATED LINKS</span></span>

[<span data-ttu-id="a20b1-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a20b1-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a20b1-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a20b1-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a20b1-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a20b1-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a20b1-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a20b1-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a20b1-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a20b1-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a20b1-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a20b1-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a20b1-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a20b1-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a20b1-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a20b1-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a20b1-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a20b1-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a20b1-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a20b1-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a20b1-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a20b1-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a20b1-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a20b1-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a20b1-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a20b1-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a20b1-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a20b1-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a20b1-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a20b1-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a20b1-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a20b1-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a20b1-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a20b1-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a20b1-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a20b1-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a20b1-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a20b1-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a20b1-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a20b1-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a20b1-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a20b1-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a20b1-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a20b1-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a20b1-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a20b1-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a20b1-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a20b1-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a20b1-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a20b1-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a20b1-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a20b1-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a20b1-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a20b1-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

