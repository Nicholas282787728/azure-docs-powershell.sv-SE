---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: aeadada7c6e2e2d7cb94a484e7ca3223e03b4426
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929038"
---
# <span data-ttu-id="27c65-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="27c65-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="27c65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27c65-102">SYNOPSIS</span></span>
<span data-ttu-id="27c65-103">Hämtar information och egenskaper och status för en paket infångnings resurs.</span><span class="sxs-lookup"><span data-stu-id="27c65-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27c65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27c65-104">SYNTAX</span></span>

### <span data-ttu-id="27c65-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="27c65-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27c65-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="27c65-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27c65-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27c65-107">DESCRIPTION</span></span>
<span data-ttu-id="27c65-108">Get-AzureRmNetworkWatcherPacketCapture hämtar egenskaper och status för en paket infångnings resurs.</span><span class="sxs-lookup"><span data-stu-id="27c65-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="27c65-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27c65-109">EXAMPLES</span></span>

### <span data-ttu-id="27c65-110">---Exempel 1: skapa en paket avbildning med flera filter och hämta dess status---</span><span class="sxs-lookup"><span data-stu-id="27c65-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="27c65-111">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="27c65-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="27c65-112">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="27c65-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="27c65-113">Vi ringer sedan Get-AzureRmNetworkWatcherPacketCapture för att hämta statusen för insamlingsbufferten.</span><span class="sxs-lookup"><span data-stu-id="27c65-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="27c65-114">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="27c65-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="27c65-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27c65-115">PARAMETERS</span></span>

### <span data-ttu-id="27c65-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27c65-116">-AsJob</span></span>
<span data-ttu-id="27c65-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="27c65-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27c65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c65-118">-DefaultProfile</span></span>
<span data-ttu-id="27c65-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27c65-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27c65-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27c65-120">-NetworkWatcher</span></span>
<span data-ttu-id="27c65-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="27c65-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="27c65-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="27c65-122">-NetworkWatcherName</span></span>
<span data-ttu-id="27c65-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="27c65-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="27c65-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="27c65-124">-PacketCaptureName</span></span>
<span data-ttu-id="27c65-125">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="27c65-125">The packet capture name.</span></span>

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

### <span data-ttu-id="27c65-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27c65-126">-ResourceGroupName</span></span>
<span data-ttu-id="27c65-127">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="27c65-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="27c65-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c65-128">CommonParameters</span></span>
<span data-ttu-id="27c65-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c65-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c65-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27c65-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c65-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27c65-131">INPUTS</span></span>

### <span data-ttu-id="27c65-132">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27c65-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="27c65-133">System. String</span><span class="sxs-lookup"><span data-stu-id="27c65-133">System.String</span></span>

## <span data-ttu-id="27c65-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27c65-134">OUTPUTS</span></span>

### <span data-ttu-id="27c65-135">Microsoft. Azure. commands. Networks. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="27c65-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="27c65-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27c65-136">NOTES</span></span>
<span data-ttu-id="27c65-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="27c65-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="27c65-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27c65-138">RELATED LINKS</span></span>

[<span data-ttu-id="27c65-139">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="27c65-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="27c65-140">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="27c65-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="27c65-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="27c65-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="27c65-142">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="27c65-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="27c65-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27c65-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="27c65-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27c65-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="27c65-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="27c65-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="27c65-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="27c65-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="27c65-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="27c65-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="27c65-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="27c65-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="27c65-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="27c65-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="27c65-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="27c65-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

