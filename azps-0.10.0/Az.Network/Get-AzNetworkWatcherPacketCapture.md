---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922240"
---
# <span data-ttu-id="06c0c-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06c0c-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="06c0c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="06c0c-103">Hämtar information och egenskaper och status för en paket infångnings resurs.</span><span class="sxs-lookup"><span data-stu-id="06c0c-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="06c0c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06c0c-104">SYNTAX</span></span>

### <span data-ttu-id="06c0c-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="06c0c-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06c0c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="06c0c-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06c0c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06c0c-107">DESCRIPTION</span></span>
<span data-ttu-id="06c0c-108">Get-AzNetworkWatcherPacketCapture hämtar egenskaper och status för en paket infångnings resurs.</span><span class="sxs-lookup"><span data-stu-id="06c0c-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="06c0c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06c0c-109">EXAMPLES</span></span>

### <span data-ttu-id="06c0c-110">---Exempel 1: skapa en paket avbildning med flera filter och hämta dess status---</span><span class="sxs-lookup"><span data-stu-id="06c0c-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="06c0c-111">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="06c0c-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="06c0c-112">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="06c0c-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="06c0c-113">Vi ringer sedan Get-AzNetworkWatcherPacketCapture för att hämta statusen för insamlingsbufferten.</span><span class="sxs-lookup"><span data-stu-id="06c0c-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="06c0c-114">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="06c0c-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="06c0c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06c0c-115">PARAMETERS</span></span>

### <span data-ttu-id="06c0c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06c0c-116">-AsJob</span></span>
<span data-ttu-id="06c0c-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="06c0c-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06c0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c0c-118">-DefaultProfile</span></span>
<span data-ttu-id="06c0c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06c0c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06c0c-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06c0c-120">-NetworkWatcher</span></span>
<span data-ttu-id="06c0c-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="06c0c-121">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06c0c-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="06c0c-122">-NetworkWatcherName</span></span>
<span data-ttu-id="06c0c-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="06c0c-123">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06c0c-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="06c0c-124">-PacketCaptureName</span></span>
<span data-ttu-id="06c0c-125">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="06c0c-125">The packet capture name.</span></span>

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

### <span data-ttu-id="06c0c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06c0c-126">-ResourceGroupName</span></span>
<span data-ttu-id="06c0c-127">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="06c0c-127">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06c0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c0c-128">CommonParameters</span></span>
<span data-ttu-id="06c0c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06c0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c0c-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c0c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c0c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06c0c-131">INPUTS</span></span>

### <span data-ttu-id="06c0c-132">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06c0c-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="06c0c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="06c0c-133">System.String</span></span>

## <span data-ttu-id="06c0c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06c0c-134">OUTPUTS</span></span>

### <span data-ttu-id="06c0c-135">Microsoft. Azure. commands. Networks. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="06c0c-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="06c0c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06c0c-136">NOTES</span></span>
<span data-ttu-id="06c0c-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="06c0c-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="06c0c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06c0c-138">RELATED LINKS</span></span>

[<span data-ttu-id="06c0c-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06c0c-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06c0c-140">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="06c0c-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="06c0c-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06c0c-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06c0c-142">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06c0c-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06c0c-143">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06c0c-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="06c0c-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06c0c-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="06c0c-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06c0c-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="06c0c-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="06c0c-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="06c0c-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="06c0c-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="06c0c-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="06c0c-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="06c0c-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="06c0c-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="06c0c-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="06c0c-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

