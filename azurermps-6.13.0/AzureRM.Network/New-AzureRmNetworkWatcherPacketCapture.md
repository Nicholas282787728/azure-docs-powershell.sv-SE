---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: ab7b6176f8453d1a3e5e0001e6b6c1e47c4de1cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585908"
---
# <span data-ttu-id="ae60c-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae60c-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="ae60c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae60c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae60c-103">Skapar en ny paket infångnings resurs och startar en session med paket-insamling på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ae60c-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae60c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae60c-104">SYNTAX</span></span>

### <span data-ttu-id="ae60c-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="ae60c-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae60c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ae60c-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae60c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ae60c-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae60c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae60c-108">DESCRIPTION</span></span>
<span data-ttu-id="ae60c-109">New-AzureRmNetworkWatcherPacketCapture cmdlet skapar en ny paket insamlings resurs och startar en session med paket-insamling på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ae60c-109">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="ae60c-110">Längden på Packet Capture-sessioner kan konfigureras via en tidsbegränsning eller ett storleks villkor.</span><span class="sxs-lookup"><span data-stu-id="ae60c-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="ae60c-111">Mängden data som sparas för varje paket kan också konfigureras.</span><span class="sxs-lookup"><span data-stu-id="ae60c-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="ae60c-112">Filter kan användas för en bestämd session för hämtning av paket, vilket gör det möjligt att anpassa vilken typ av paket som du har spelat in.</span><span class="sxs-lookup"><span data-stu-id="ae60c-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="ae60c-113">Filter kan begränsa paket på lokala och fjärr-IP-adresser & adress intervall, lokala portar och fjärrsamtal & port intervall och session Level Protocol som ska samlas in.</span><span class="sxs-lookup"><span data-stu-id="ae60c-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="ae60c-114">Filter är sammankopplade och flera filter kan användas för att ge dig detaljerad insamling.</span><span class="sxs-lookup"><span data-stu-id="ae60c-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="ae60c-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae60c-115">EXAMPLES</span></span>

### <span data-ttu-id="ae60c-116">Exempel 1: skapa en paket avbildning med flera filter</span><span class="sxs-lookup"><span data-stu-id="ae60c-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="ae60c-117">I det här exemplet skapar vi en paket avbildning med namnet "PacketCaptureTest" med flera filter och en tids gräns.</span><span class="sxs-lookup"><span data-stu-id="ae60c-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="ae60c-118">När sessionen är klar sparas den till det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ae60c-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="ae60c-119">Obs! Azure Network Watcher-tillägget måste vara installerat på den virtuella mål datorn för att du ska kunna skapa paket avbildningar.</span><span class="sxs-lookup"><span data-stu-id="ae60c-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="ae60c-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae60c-120">PARAMETERS</span></span>

### <span data-ttu-id="ae60c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae60c-121">-AsJob</span></span>
<span data-ttu-id="ae60c-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ae60c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae60c-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="ae60c-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="ae60c-124">Antal byte att fånga per paket.</span><span class="sxs-lookup"><span data-stu-id="ae60c-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="ae60c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae60c-125">-DefaultProfile</span></span>
<span data-ttu-id="ae60c-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae60c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae60c-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="ae60c-127">-Filter</span></span>
<span data-ttu-id="ae60c-128">Filter för sändning av paket.</span><span class="sxs-lookup"><span data-stu-id="ae60c-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="ae60c-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="ae60c-129">-LocalFilePath</span></span>
<span data-ttu-id="ae60c-130">Lokal fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="ae60c-130">Local file path.</span></span>

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

### <span data-ttu-id="ae60c-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="ae60c-131">-Location</span></span>
<span data-ttu-id="ae60c-132">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="ae60c-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ae60c-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae60c-133">-NetworkWatcher</span></span>
<span data-ttu-id="ae60c-134">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="ae60c-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="ae60c-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ae60c-135">-NetworkWatcherName</span></span>
<span data-ttu-id="ae60c-136">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="ae60c-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="ae60c-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="ae60c-137">-PacketCaptureName</span></span>
<span data-ttu-id="ae60c-138">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="ae60c-138">The packet capture name.</span></span>

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

### <span data-ttu-id="ae60c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae60c-139">-ResourceGroupName</span></span>
<span data-ttu-id="ae60c-140">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ae60c-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ae60c-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ae60c-141">-StorageAccountId</span></span>
<span data-ttu-id="ae60c-142">ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ae60c-142">Storage account Id.</span></span>

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

### <span data-ttu-id="ae60c-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="ae60c-143">-StoragePath</span></span>
<span data-ttu-id="ae60c-144">Lagrings Sök väg.</span><span class="sxs-lookup"><span data-stu-id="ae60c-144">Storage path.</span></span>

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

### <span data-ttu-id="ae60c-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ae60c-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="ae60c-146">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="ae60c-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="ae60c-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="ae60c-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="ae60c-148">Tids gräns på sekunder.</span><span class="sxs-lookup"><span data-stu-id="ae60c-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="ae60c-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="ae60c-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="ae60c-150">Totalt antal byte per session.</span><span class="sxs-lookup"><span data-stu-id="ae60c-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="ae60c-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae60c-151">-Confirm</span></span>
<span data-ttu-id="ae60c-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae60c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae60c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae60c-153">-WhatIf</span></span>
<span data-ttu-id="ae60c-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae60c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae60c-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae60c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae60c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae60c-156">CommonParameters</span></span>
<span data-ttu-id="ae60c-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae60c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae60c-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae60c-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae60c-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae60c-159">INPUTS</span></span>

### <span data-ttu-id="ae60c-160">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae60c-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ae60c-161">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae60c-161">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="ae60c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="ae60c-162">System.String</span></span>
<span data-ttu-id="ae60c-163">Parametrar: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae60c-163">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="ae60c-164">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ae60c-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ae60c-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae60c-165">OUTPUTS</span></span>

### <span data-ttu-id="ae60c-166">Microsoft. Azure. commands. Networks. Models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="ae60c-166">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="ae60c-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae60c-167">NOTES</span></span>
<span data-ttu-id="ae60c-168">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="ae60c-168">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="ae60c-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae60c-169">RELATED LINKS</span></span>

[<span data-ttu-id="ae60c-170">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae60c-170">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ae60c-171">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae60c-171">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ae60c-172">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae60c-172">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ae60c-173">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ae60c-173">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ae60c-174">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ae60c-174">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ae60c-175">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ae60c-175">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ae60c-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ae60c-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ae60c-177">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae60c-177">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae60c-178">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ae60c-178">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ae60c-179">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae60c-179">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae60c-180">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae60c-180">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae60c-181">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae60c-181">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae60c-182">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae60c-182">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ae60c-183">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ae60c-183">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ae60c-184">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ae60c-184">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="ae60c-185">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae60c-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae60c-186">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae60c-186">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae60c-187">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae60c-187">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae60c-188">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ae60c-188">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ae60c-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae60c-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae60c-190">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae60c-190">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae60c-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ae60c-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ae60c-192">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ae60c-192">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ae60c-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ae60c-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ae60c-194">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ae60c-194">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ae60c-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ae60c-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="ae60c-196">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae60c-196">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)


