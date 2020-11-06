---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 0c84927ede94724da94351a219c9c0ec594c688d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586368"
---
# <span data-ttu-id="6e60d-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e60d-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="6e60d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e60d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e60d-103">Skapar en ny paket infångnings resurs och startar en session med paket-insamling på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6e60d-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e60d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e60d-104">SYNTAX</span></span>

### <span data-ttu-id="6e60d-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="6e60d-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e60d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6e60d-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e60d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e60d-107">DESCRIPTION</span></span>
<span data-ttu-id="6e60d-108">New-AzureRmNetworkWatcherPacketCapture cmdlet skapar en ny paket insamlings resurs och startar en session med paket-insamling på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6e60d-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="6e60d-109">Längden på Packet Capture-sessioner kan konfigureras via en tidsbegränsning eller ett storleks villkor.</span><span class="sxs-lookup"><span data-stu-id="6e60d-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="6e60d-110">Mängden data som sparas för varje paket kan också konfigureras.</span><span class="sxs-lookup"><span data-stu-id="6e60d-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="6e60d-111">Filter kan användas för en bestämd session för hämtning av paket, vilket gör det möjligt att anpassa vilken typ av paket som du har spelat in.</span><span class="sxs-lookup"><span data-stu-id="6e60d-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="6e60d-112">Filter kan begränsa paket på lokala och fjärr-IP-adresser & adress intervall, lokala portar och fjärrsamtal & port intervall och session Level Protocol som ska samlas in.</span><span class="sxs-lookup"><span data-stu-id="6e60d-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="6e60d-113">Filter är sammankopplade och flera filter kan användas för att ge dig detaljerad insamling.</span><span class="sxs-lookup"><span data-stu-id="6e60d-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="6e60d-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e60d-114">EXAMPLES</span></span>

### <span data-ttu-id="6e60d-115">---Exempel 1: skapa en paket avbildning med flera filter---</span><span class="sxs-lookup"><span data-stu-id="6e60d-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="6e60d-116">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="6e60d-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="6e60d-117">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="6e60d-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="6e60d-118">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="6e60d-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="6e60d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e60d-119">PARAMETERS</span></span>

### <span data-ttu-id="6e60d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e60d-120">-AsJob</span></span>
<span data-ttu-id="6e60d-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6e60d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e60d-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="6e60d-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="6e60d-123">Antal byte att fånga per paket.</span><span class="sxs-lookup"><span data-stu-id="6e60d-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e60d-124">-DefaultProfile</span></span>
<span data-ttu-id="6e60d-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e60d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e60d-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="6e60d-126">-Filter</span></span>
<span data-ttu-id="6e60d-127">Filter för sändning av paket.</span><span class="sxs-lookup"><span data-stu-id="6e60d-127">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="6e60d-128">-LocalFilePath</span></span>
<span data-ttu-id="6e60d-129">Lokal fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="6e60d-129">Local file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e60d-130">-NetworkWatcher</span></span>
<span data-ttu-id="6e60d-131">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="6e60d-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="6e60d-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6e60d-132">-NetworkWatcherName</span></span>
<span data-ttu-id="6e60d-133">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="6e60d-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="6e60d-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="6e60d-134">-PacketCaptureName</span></span>
<span data-ttu-id="6e60d-135">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="6e60d-135">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e60d-136">-ResourceGroupName</span></span>
<span data-ttu-id="6e60d-137">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6e60d-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6e60d-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6e60d-138">-StorageAccountId</span></span>
<span data-ttu-id="6e60d-139">ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6e60d-139">Storage account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="6e60d-140">-StoragePath</span></span>
<span data-ttu-id="6e60d-141">Lagrings Sök väg.</span><span class="sxs-lookup"><span data-stu-id="6e60d-141">Storage path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="6e60d-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="6e60d-143">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="6e60d-143">The target virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="6e60d-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="6e60d-145">Tids gräns på sekunder.</span><span class="sxs-lookup"><span data-stu-id="6e60d-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="6e60d-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="6e60d-147">Totalt antal byte per session.</span><span class="sxs-lookup"><span data-stu-id="6e60d-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6e60d-148">-Confirm</span></span>
<span data-ttu-id="6e60d-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6e60d-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e60d-150">-WhatIf</span></span>
<span data-ttu-id="6e60d-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6e60d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e60d-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6e60d-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e60d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e60d-153">CommonParameters</span></span>
<span data-ttu-id="6e60d-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e60d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e60d-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e60d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e60d-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e60d-156">INPUTS</span></span>

### <span data-ttu-id="6e60d-157">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e60d-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6e60d-158">System. String-system. Nullable \` 1 \[ \[ system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="6e60d-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="6e60d-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e60d-159">OUTPUTS</span></span>

### <span data-ttu-id="6e60d-160">Microsoft. Azure. commands. Networks. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e60d-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="6e60d-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e60d-161">NOTES</span></span>
<span data-ttu-id="6e60d-162">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="6e60d-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="6e60d-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e60d-163">RELATED LINKS</span></span>

[<span data-ttu-id="6e60d-164">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6e60d-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6e60d-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e60d-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6e60d-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e60d-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6e60d-167">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e60d-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6e60d-168">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e60d-168">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6e60d-169">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e60d-169">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6e60d-170">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e60d-170">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6e60d-171">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6e60d-171">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6e60d-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6e60d-172">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6e60d-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6e60d-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6e60d-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6e60d-174">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6e60d-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6e60d-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


