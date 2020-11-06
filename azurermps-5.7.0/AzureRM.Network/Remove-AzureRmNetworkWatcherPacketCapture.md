---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 034cca094bf6dd7d3911e3e705e03888f0ea10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583644"
---
# <span data-ttu-id="f195f-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f195f-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="f195f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f195f-102">SYNOPSIS</span></span>
<span data-ttu-id="f195f-103">Tar bort en paket registrerings resurs.</span><span class="sxs-lookup"><span data-stu-id="f195f-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f195f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f195f-104">SYNTAX</span></span>

### <span data-ttu-id="f195f-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="f195f-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f195f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f195f-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f195f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f195f-107">DESCRIPTION</span></span>
<span data-ttu-id="f195f-108">Remove-AzureRmNetworkWatcherPacketCapture tar bort en paket registrerings resurs.</span><span class="sxs-lookup"><span data-stu-id="f195f-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="f195f-109">Vi rekommenderar att du ringer Stop-AzureRmNetworkWatcherPacketCapture innan du ringer Remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="f195f-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="f195f-110">Om Packet Capture körs när Remove-AzureRmNetworkWatcherPacketCapture kallas för paket inspelningen kanske den inte sparas.</span><span class="sxs-lookup"><span data-stu-id="f195f-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="f195f-111">Om sessionen stoppas innan du tar bort den. Cap-filen som innehåller insamlingsfiler tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="f195f-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="f195f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f195f-112">EXAMPLES</span></span>

### <span data-ttu-id="f195f-113">---Exempel 1: ta bort en session med en paket--</span><span class="sxs-lookup"><span data-stu-id="f195f-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="f195f-114">I det här exemplet tar vi bort en befintlig paket infångnings session med namnet "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="f195f-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="f195f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f195f-115">PARAMETERS</span></span>

### <span data-ttu-id="f195f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f195f-116">-AsJob</span></span>
<span data-ttu-id="f195f-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f195f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f195f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f195f-118">-DefaultProfile</span></span>
<span data-ttu-id="f195f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f195f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f195f-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f195f-120">-NetworkWatcher</span></span>
<span data-ttu-id="f195f-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="f195f-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="f195f-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f195f-122">-NetworkWatcherName</span></span>
<span data-ttu-id="f195f-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="f195f-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="f195f-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="f195f-124">-PacketCaptureName</span></span>
<span data-ttu-id="f195f-125">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="f195f-125">The packet capture name.</span></span>

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

### <span data-ttu-id="f195f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f195f-126">-PassThru</span></span>
<span data-ttu-id="f195f-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f195f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f195f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f195f-128">-ResourceGroupName</span></span>
<span data-ttu-id="f195f-129">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f195f-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f195f-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f195f-130">-Confirm</span></span>
<span data-ttu-id="f195f-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f195f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f195f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f195f-132">-WhatIf</span></span>
<span data-ttu-id="f195f-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f195f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f195f-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f195f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f195f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f195f-135">CommonParameters</span></span>
<span data-ttu-id="f195f-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f195f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f195f-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f195f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f195f-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f195f-138">INPUTS</span></span>

### <span data-ttu-id="f195f-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f195f-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f195f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f195f-140">System.String</span></span>

## <span data-ttu-id="f195f-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f195f-141">OUTPUTS</span></span>

### <span data-ttu-id="f195f-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="f195f-142">System.Object</span></span>

## <span data-ttu-id="f195f-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f195f-143">NOTES</span></span>
<span data-ttu-id="f195f-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik, ta bort</span><span class="sxs-lookup"><span data-stu-id="f195f-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="f195f-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f195f-145">RELATED LINKS</span></span>

[<span data-ttu-id="f195f-146">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f195f-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f195f-147">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f195f-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f195f-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f195f-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f195f-149">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f195f-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f195f-150">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f195f-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f195f-151">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f195f-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f195f-152">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f195f-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f195f-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f195f-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f195f-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f195f-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f195f-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f195f-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f195f-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f195f-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f195f-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f195f-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
