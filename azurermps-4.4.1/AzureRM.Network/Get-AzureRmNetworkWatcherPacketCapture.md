---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 4cf1cb9149c0f821ad0e6164cd7c817b12ccc147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575992"
---
# <span data-ttu-id="333b0-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="333b0-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="333b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="333b0-102">SYNOPSIS</span></span>
<span data-ttu-id="333b0-103">Hämtar information och egenskaper och status för en paket infångnings resurs.</span><span class="sxs-lookup"><span data-stu-id="333b0-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="333b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="333b0-104">SYNTAX</span></span>

### <span data-ttu-id="333b0-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="333b0-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="333b0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="333b0-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="333b0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="333b0-107">DESCRIPTION</span></span>
<span data-ttu-id="333b0-108">Get-AzureRmNetworkWatcherPacketCapture hämtar egenskaper och status för en paket infångnings resurs.</span><span class="sxs-lookup"><span data-stu-id="333b0-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="333b0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="333b0-109">EXAMPLES</span></span>

### <span data-ttu-id="333b0-110">---Exempel 1: skapa en paket avbildning med flera filter och hämta dess status---</span><span class="sxs-lookup"><span data-stu-id="333b0-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="333b0-111">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="333b0-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="333b0-112">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="333b0-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="333b0-113">Vi ringer sedan Get-AzureRmNetworkWatcherPacketCapture för att hämta statusen för insamlingsbufferten.</span><span class="sxs-lookup"><span data-stu-id="333b0-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="333b0-114">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="333b0-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="333b0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="333b0-115">PARAMETERS</span></span>

### <span data-ttu-id="333b0-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="333b0-116">-NetworkWatcher</span></span>
<span data-ttu-id="333b0-117">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="333b0-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="333b0-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="333b0-118">-NetworkWatcherName</span></span>
<span data-ttu-id="333b0-119">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="333b0-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="333b0-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="333b0-120">-PacketCaptureName</span></span>
<span data-ttu-id="333b0-121">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="333b0-121">The packet capture name.</span></span>

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

### <span data-ttu-id="333b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="333b0-123">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="333b0-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="333b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333b0-124">-DefaultProfile</span></span>
<span data-ttu-id="333b0-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="333b0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="333b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333b0-126">CommonParameters</span></span>
<span data-ttu-id="333b0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333b0-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="333b0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333b0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="333b0-129">INPUTS</span></span>

### <span data-ttu-id="333b0-130">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="333b0-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="333b0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="333b0-131">System.String</span></span>

## <span data-ttu-id="333b0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="333b0-132">OUTPUTS</span></span>

### <span data-ttu-id="333b0-133">Microsoft. Azure. commands. Networks. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="333b0-133">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="333b0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="333b0-134">NOTES</span></span>
<span data-ttu-id="333b0-135">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="333b0-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="333b0-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="333b0-136">RELATED LINKS</span></span>

[<span data-ttu-id="333b0-137">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="333b0-137">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="333b0-138">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="333b0-138">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="333b0-139">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="333b0-139">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="333b0-140">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="333b0-140">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="333b0-141">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="333b0-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="333b0-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="333b0-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="333b0-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="333b0-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="333b0-144">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="333b0-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="333b0-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="333b0-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="333b0-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="333b0-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="333b0-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="333b0-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="333b0-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="333b0-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

