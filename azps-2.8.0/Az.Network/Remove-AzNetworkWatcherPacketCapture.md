---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d99b085f5137c9f18d4dda50fce0654954266f37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919001"
---
# <span data-ttu-id="48e01-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="48e01-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="48e01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48e01-102">SYNOPSIS</span></span>
<span data-ttu-id="48e01-103">Tar bort en paket registrerings resurs.</span><span class="sxs-lookup"><span data-stu-id="48e01-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="48e01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48e01-104">SYNTAX</span></span>

### <span data-ttu-id="48e01-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="48e01-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48e01-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="48e01-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48e01-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="48e01-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48e01-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48e01-108">DESCRIPTION</span></span>
<span data-ttu-id="48e01-109">Remove-AzNetworkWatcherPacketCapture tar bort en paket registrerings resurs.</span><span class="sxs-lookup"><span data-stu-id="48e01-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="48e01-110">Vi rekommenderar att du ringer Stop-AzNetworkWatcherPacketCapture innan du ringer Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="48e01-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="48e01-111">Om Packet Capture körs när Remove-AzNetworkWatcherPacketCapture kallas för paket inspelningen kanske den inte sparas.</span><span class="sxs-lookup"><span data-stu-id="48e01-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="48e01-112">Om sessionen stoppas innan du tar bort den. Cap-filen som innehåller insamlingsfiler tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="48e01-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="48e01-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48e01-113">EXAMPLES</span></span>

### <span data-ttu-id="48e01-114">Exempel 1: ta bort en session med ett paket</span><span class="sxs-lookup"><span data-stu-id="48e01-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="48e01-115">I det här exemplet tar vi bort en befintlig paket infångnings session med namnet "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="48e01-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="48e01-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48e01-116">PARAMETERS</span></span>

### <span data-ttu-id="48e01-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48e01-117">-AsJob</span></span>
<span data-ttu-id="48e01-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="48e01-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48e01-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e01-119">-DefaultProfile</span></span>
<span data-ttu-id="48e01-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48e01-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48e01-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="48e01-121">-Location</span></span>
<span data-ttu-id="48e01-122">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="48e01-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="48e01-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="48e01-123">-NetworkWatcher</span></span>
<span data-ttu-id="48e01-124">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="48e01-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="48e01-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="48e01-125">-NetworkWatcherName</span></span>
<span data-ttu-id="48e01-126">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="48e01-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="48e01-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="48e01-127">-PacketCaptureName</span></span>
<span data-ttu-id="48e01-128">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="48e01-128">The packet capture name.</span></span>

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

### <span data-ttu-id="48e01-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48e01-129">-PassThru</span></span>
<span data-ttu-id="48e01-130">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="48e01-130">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e01-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e01-131">-ResourceGroupName</span></span>
<span data-ttu-id="48e01-132">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="48e01-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="48e01-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48e01-133">-Confirm</span></span>
<span data-ttu-id="48e01-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48e01-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48e01-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48e01-135">-WhatIf</span></span>
<span data-ttu-id="48e01-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48e01-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48e01-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48e01-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48e01-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e01-138">CommonParameters</span></span>
<span data-ttu-id="48e01-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48e01-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e01-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48e01-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e01-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48e01-141">INPUTS</span></span>

### <span data-ttu-id="48e01-142">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="48e01-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="48e01-143">System. String</span><span class="sxs-lookup"><span data-stu-id="48e01-143">System.String</span></span>

## <span data-ttu-id="48e01-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48e01-144">OUTPUTS</span></span>

### <span data-ttu-id="48e01-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48e01-145">System.Boolean</span></span>

## <span data-ttu-id="48e01-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48e01-146">NOTES</span></span>
<span data-ttu-id="48e01-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik, ta bort</span><span class="sxs-lookup"><span data-stu-id="48e01-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="48e01-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48e01-148">RELATED LINKS</span></span>

[<span data-ttu-id="48e01-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="48e01-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="48e01-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="48e01-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="48e01-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="48e01-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="48e01-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="48e01-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="48e01-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="48e01-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="48e01-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="48e01-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="48e01-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="48e01-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="48e01-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="48e01-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="48e01-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="48e01-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="48e01-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="48e01-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="48e01-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="48e01-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="48e01-160">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="48e01-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="48e01-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="48e01-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="48e01-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="48e01-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="48e01-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="48e01-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="48e01-164">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="48e01-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="48e01-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="48e01-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="48e01-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="48e01-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="48e01-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="48e01-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="48e01-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="48e01-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="48e01-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="48e01-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="48e01-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="48e01-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="48e01-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="48e01-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="48e01-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="48e01-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="48e01-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="48e01-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="48e01-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="48e01-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="48e01-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="48e01-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)