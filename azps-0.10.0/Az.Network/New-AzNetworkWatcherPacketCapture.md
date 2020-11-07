---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 6844db506ee8a55c7d0c16f54946e35349059ae4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922101"
---
# <span data-ttu-id="bd9f0-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bd9f0-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="bd9f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd9f0-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9f0-103">Skapar en ny paket infångnings resurs och startar en session med paket-insamling på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="bd9f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd9f0-104">SYNTAX</span></span>

### <span data-ttu-id="bd9f0-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="bd9f0-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9f0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bd9f0-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd9f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd9f0-107">DESCRIPTION</span></span>
<span data-ttu-id="bd9f0-108">New-AzNetworkWatcherPacketCapture cmdlet skapar en ny paket insamlings resurs och startar en session med paket-insamling på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-108">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="bd9f0-109">Längden på Packet Capture-sessioner kan konfigureras via en tidsbegränsning eller ett storleks villkor.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="bd9f0-110">Mängden data som sparas för varje paket kan också konfigureras.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="bd9f0-111">Filter kan användas för en bestämd session för hämtning av paket, vilket gör det möjligt att anpassa vilken typ av paket som du har spelat in.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="bd9f0-112">Filter kan begränsa paket på lokala och fjärr-IP-adresser & adress intervall, lokala portar och fjärrsamtal & port intervall och session Level Protocol som ska samlas in.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="bd9f0-113">Filter är sammankopplade och flera filter kan användas för att ge dig detaljerad insamling.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="bd9f0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd9f0-114">EXAMPLES</span></span>

### <span data-ttu-id="bd9f0-115">---Exempel 1: skapa en paket avbildning med flera filter---</span><span class="sxs-lookup"><span data-stu-id="bd9f0-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="bd9f0-116">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="bd9f0-117">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="bd9f0-118">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="bd9f0-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd9f0-119">PARAMETERS</span></span>

### <span data-ttu-id="bd9f0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd9f0-120">-AsJob</span></span>
<span data-ttu-id="bd9f0-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bd9f0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd9f0-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="bd9f0-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="bd9f0-123">Antal byte att fånga per paket.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-123">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="bd9f0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9f0-124">-DefaultProfile</span></span>
<span data-ttu-id="bd9f0-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd9f0-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="bd9f0-126">-Filter</span></span>
<span data-ttu-id="bd9f0-127">Filter för sändning av paket.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-127">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="bd9f0-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="bd9f0-128">-LocalFilePath</span></span>
<span data-ttu-id="bd9f0-129">Lokal fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-129">Local file path.</span></span>

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

### <span data-ttu-id="bd9f0-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd9f0-130">-NetworkWatcher</span></span>
<span data-ttu-id="bd9f0-131">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="bd9f0-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bd9f0-132">-NetworkWatcherName</span></span>
<span data-ttu-id="bd9f0-133">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="bd9f0-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="bd9f0-134">-PacketCaptureName</span></span>
<span data-ttu-id="bd9f0-135">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-135">The packet capture name.</span></span>

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

### <span data-ttu-id="bd9f0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd9f0-136">-ResourceGroupName</span></span>
<span data-ttu-id="bd9f0-137">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bd9f0-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bd9f0-138">-StorageAccountId</span></span>
<span data-ttu-id="bd9f0-139">ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-139">Storage account Id.</span></span>

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

### <span data-ttu-id="bd9f0-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="bd9f0-140">-StoragePath</span></span>
<span data-ttu-id="bd9f0-141">Lagrings Sök väg.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-141">Storage path.</span></span>

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

### <span data-ttu-id="bd9f0-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="bd9f0-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="bd9f0-143">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="bd9f0-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="bd9f0-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="bd9f0-145">Tids gräns på sekunder.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-145">Time limit in seconds.</span></span>

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

### <span data-ttu-id="bd9f0-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="bd9f0-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="bd9f0-147">Totalt antal byte per session.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-147">Total bytes per session.</span></span>

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

### <span data-ttu-id="bd9f0-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd9f0-148">-Confirm</span></span>
<span data-ttu-id="bd9f0-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd9f0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd9f0-150">-WhatIf</span></span>
<span data-ttu-id="bd9f0-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd9f0-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd9f0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9f0-153">CommonParameters</span></span>
<span data-ttu-id="bd9f0-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd9f0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9f0-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd9f0-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9f0-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd9f0-156">INPUTS</span></span>

### <span data-ttu-id="bd9f0-157">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd9f0-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bd9f0-158">System. String-system. Nullable \` 1 \[ \[ system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="bd9f0-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="bd9f0-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd9f0-159">OUTPUTS</span></span>

### <span data-ttu-id="bd9f0-160">Microsoft. Azure. commands. Networks. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bd9f0-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="bd9f0-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd9f0-161">NOTES</span></span>
<span data-ttu-id="bd9f0-162">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="bd9f0-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="bd9f0-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd9f0-163">RELATED LINKS</span></span>

[<span data-ttu-id="bd9f0-164">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bd9f0-164">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bd9f0-165">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bd9f0-165">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bd9f0-166">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bd9f0-166">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bd9f0-167">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bd9f0-167">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bd9f0-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd9f0-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bd9f0-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd9f0-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bd9f0-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd9f0-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bd9f0-171">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bd9f0-171">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bd9f0-172">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bd9f0-172">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bd9f0-173">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bd9f0-173">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bd9f0-174">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bd9f0-174">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bd9f0-175">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bd9f0-175">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)


