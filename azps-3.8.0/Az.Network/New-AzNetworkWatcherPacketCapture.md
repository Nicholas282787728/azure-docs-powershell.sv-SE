---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 348767f145c2dd407fc277549f89c44386c8a564
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089506"
---
# <span data-ttu-id="bdf97-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdf97-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="bdf97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdf97-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf97-103">Skapar en ny paket infångnings resurs och startar en session med paket-insamling på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bdf97-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="bdf97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdf97-104">SYNTAX</span></span>

### <span data-ttu-id="bdf97-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="bdf97-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdf97-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bdf97-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdf97-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bdf97-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdf97-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdf97-108">DESCRIPTION</span></span>
<span data-ttu-id="bdf97-109">New-AzNetworkWatcherPacketCapture cmdlet skapar en ny paket insamlings resurs och startar en session med paket-insamling på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bdf97-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="bdf97-110">Längden på Packet Capture-sessioner kan konfigureras via en tidsbegränsning eller ett storleks villkor.</span><span class="sxs-lookup"><span data-stu-id="bdf97-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="bdf97-111">Mängden data som sparas för varje paket kan också konfigureras.</span><span class="sxs-lookup"><span data-stu-id="bdf97-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="bdf97-112">Filter kan användas för en bestämd session för hämtning av paket, vilket gör det möjligt att anpassa vilken typ av paket som du har spelat in.</span><span class="sxs-lookup"><span data-stu-id="bdf97-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="bdf97-113">Filter kan begränsa paket på lokala och fjärr-IP-adresser & adress intervall, lokala portar och fjärrsamtal & port intervall och session Level Protocol som ska samlas in.</span><span class="sxs-lookup"><span data-stu-id="bdf97-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="bdf97-114">Filter är sammankopplade och flera filter kan användas för att ge dig detaljerad insamling.</span><span class="sxs-lookup"><span data-stu-id="bdf97-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="bdf97-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdf97-115">EXAMPLES</span></span>

### <span data-ttu-id="bdf97-116">Exempel 1: skapa en paket avbildning med flera filter</span><span class="sxs-lookup"><span data-stu-id="bdf97-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="bdf97-117">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="bdf97-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="bdf97-118">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="bdf97-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="bdf97-119">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="bdf97-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="bdf97-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdf97-120">PARAMETERS</span></span>

### <span data-ttu-id="bdf97-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdf97-121">-AsJob</span></span>
<span data-ttu-id="bdf97-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bdf97-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdf97-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="bdf97-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="bdf97-124">Antal byte att fånga per paket.</span><span class="sxs-lookup"><span data-stu-id="bdf97-124">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf97-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf97-125">-DefaultProfile</span></span>
<span data-ttu-id="bdf97-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf97-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdf97-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="bdf97-127">-Filter</span></span>
<span data-ttu-id="bdf97-128">Filter för sändning av paket.</span><span class="sxs-lookup"><span data-stu-id="bdf97-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf97-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="bdf97-129">-LocalFilePath</span></span>
<span data-ttu-id="bdf97-130">Lokal fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="bdf97-130">Local file path.</span></span>

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

### <span data-ttu-id="bdf97-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="bdf97-131">-Location</span></span>
<span data-ttu-id="bdf97-132">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="bdf97-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bdf97-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdf97-133">-NetworkWatcher</span></span>
<span data-ttu-id="bdf97-134">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="bdf97-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="bdf97-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bdf97-135">-NetworkWatcherName</span></span>
<span data-ttu-id="bdf97-136">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="bdf97-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="bdf97-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="bdf97-137">-PacketCaptureName</span></span>
<span data-ttu-id="bdf97-138">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="bdf97-138">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf97-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf97-139">-ResourceGroupName</span></span>
<span data-ttu-id="bdf97-140">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bdf97-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bdf97-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bdf97-141">-StorageAccountId</span></span>
<span data-ttu-id="bdf97-142">ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="bdf97-142">Storage account Id.</span></span>

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

### <span data-ttu-id="bdf97-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="bdf97-143">-StoragePath</span></span>
<span data-ttu-id="bdf97-144">Lagrings Sök väg.</span><span class="sxs-lookup"><span data-stu-id="bdf97-144">Storage path.</span></span>

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

### <span data-ttu-id="bdf97-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="bdf97-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="bdf97-146">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="bdf97-146">The target virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf97-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="bdf97-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="bdf97-148">Tids gräns på sekunder.</span><span class="sxs-lookup"><span data-stu-id="bdf97-148">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf97-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="bdf97-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="bdf97-150">Totalt antal byte per session.</span><span class="sxs-lookup"><span data-stu-id="bdf97-150">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf97-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bdf97-151">-Confirm</span></span>
<span data-ttu-id="bdf97-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bdf97-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf97-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdf97-153">-WhatIf</span></span>
<span data-ttu-id="bdf97-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bdf97-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdf97-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bdf97-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf97-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf97-156">CommonParameters</span></span>
<span data-ttu-id="bdf97-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf97-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf97-158">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdf97-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf97-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdf97-159">INPUTS</span></span>

### <span data-ttu-id="bdf97-160">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdf97-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="bdf97-161">System. String</span><span class="sxs-lookup"><span data-stu-id="bdf97-161">System.String</span></span>

### <span data-ttu-id="bdf97-162">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bdf97-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bdf97-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdf97-163">OUTPUTS</span></span>

### <span data-ttu-id="bdf97-164">Microsoft. Azure. commands. Networks. Models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="bdf97-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="bdf97-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdf97-165">NOTES</span></span>
<span data-ttu-id="bdf97-166">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="bdf97-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="bdf97-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdf97-167">RELATED LINKS</span></span>

[<span data-ttu-id="bdf97-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdf97-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bdf97-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdf97-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bdf97-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdf97-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bdf97-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bdf97-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bdf97-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bdf97-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bdf97-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bdf97-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bdf97-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bdf97-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="bdf97-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdf97-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bdf97-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bdf97-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bdf97-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdf97-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bdf97-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdf97-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bdf97-179">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdf97-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bdf97-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdf97-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="bdf97-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bdf97-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bdf97-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="bdf97-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="bdf97-183">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bdf97-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bdf97-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bdf97-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bdf97-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bdf97-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bdf97-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bdf97-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="bdf97-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bdf97-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bdf97-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bdf97-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bdf97-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bdf97-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="bdf97-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="bdf97-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="bdf97-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bdf97-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="bdf97-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bdf97-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="bdf97-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bdf97-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="bdf97-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bdf97-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

