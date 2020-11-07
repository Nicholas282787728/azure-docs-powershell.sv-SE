---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924373"
---
# <span data-ttu-id="677b6-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="677b6-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="677b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="677b6-102">SYNOPSIS</span></span>
<span data-ttu-id="677b6-103">Tar bort en paket registrerings resurs.</span><span class="sxs-lookup"><span data-stu-id="677b6-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="677b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="677b6-104">SYNTAX</span></span>

### <span data-ttu-id="677b6-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="677b6-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="677b6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="677b6-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="677b6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="677b6-107">DESCRIPTION</span></span>
<span data-ttu-id="677b6-108">Remove-AzNetworkWatcherPacketCapture tar bort en paket registrerings resurs.</span><span class="sxs-lookup"><span data-stu-id="677b6-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="677b6-109">Vi rekommenderar att du ringer Stop-AzNetworkWatcherPacketCapture innan du ringer Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="677b6-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="677b6-110">Om Packet Capture körs när Remove-AzNetworkWatcherPacketCapture kallas för paket inspelningen kanske den inte sparas.</span><span class="sxs-lookup"><span data-stu-id="677b6-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="677b6-111">Om sessionen stoppas innan du tar bort den. Cap-filen som innehåller insamlingsfiler tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="677b6-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="677b6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="677b6-112">EXAMPLES</span></span>

### <span data-ttu-id="677b6-113">---Exempel 1: ta bort en session med en paket--</span><span class="sxs-lookup"><span data-stu-id="677b6-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="677b6-114">I det här exemplet tar vi bort en befintlig paket infångnings session med namnet "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="677b6-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="677b6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="677b6-115">PARAMETERS</span></span>

### <span data-ttu-id="677b6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="677b6-116">-AsJob</span></span>
<span data-ttu-id="677b6-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="677b6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="677b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677b6-118">-DefaultProfile</span></span>
<span data-ttu-id="677b6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="677b6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="677b6-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="677b6-120">-NetworkWatcher</span></span>
<span data-ttu-id="677b6-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="677b6-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="677b6-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="677b6-122">-NetworkWatcherName</span></span>
<span data-ttu-id="677b6-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="677b6-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="677b6-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="677b6-124">-PacketCaptureName</span></span>
<span data-ttu-id="677b6-125">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="677b6-125">The packet capture name.</span></span>

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

### <span data-ttu-id="677b6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="677b6-126">-PassThru</span></span>
<span data-ttu-id="677b6-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="677b6-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="677b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="677b6-129">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="677b6-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="677b6-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="677b6-130">-Confirm</span></span>
<span data-ttu-id="677b6-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="677b6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="677b6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="677b6-132">-WhatIf</span></span>
<span data-ttu-id="677b6-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="677b6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="677b6-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="677b6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="677b6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677b6-135">CommonParameters</span></span>
<span data-ttu-id="677b6-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677b6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677b6-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="677b6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677b6-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="677b6-138">INPUTS</span></span>

### <span data-ttu-id="677b6-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="677b6-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="677b6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="677b6-140">System.String</span></span>

## <span data-ttu-id="677b6-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="677b6-141">OUTPUTS</span></span>

### <span data-ttu-id="677b6-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="677b6-142">System.Object</span></span>

## <span data-ttu-id="677b6-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="677b6-143">NOTES</span></span>
<span data-ttu-id="677b6-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik, ta bort</span><span class="sxs-lookup"><span data-stu-id="677b6-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="677b6-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="677b6-145">RELATED LINKS</span></span>

[<span data-ttu-id="677b6-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="677b6-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="677b6-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="677b6-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="677b6-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="677b6-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="677b6-149">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="677b6-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="677b6-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="677b6-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="677b6-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="677b6-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="677b6-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="677b6-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="677b6-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="677b6-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="677b6-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="677b6-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="677b6-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="677b6-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="677b6-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="677b6-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="677b6-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="677b6-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
