---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 922026b14531cc1c65f60901914383b402d06889
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525740"
---
# <span data-ttu-id="c0349-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0349-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="c0349-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0349-102">SYNOPSIS</span></span>
<span data-ttu-id="c0349-103">Stoppar en session med pågående paket</span><span class="sxs-lookup"><span data-stu-id="c0349-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="c0349-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0349-104">SYNTAX</span></span>

### <span data-ttu-id="c0349-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="c0349-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0349-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c0349-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0349-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c0349-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0349-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0349-108">DESCRIPTION</span></span>
<span data-ttu-id="c0349-109">Stop-AzNetworkWatcherPacketCapture stoppar sändningen av en pågående paket.</span><span class="sxs-lookup"><span data-stu-id="c0349-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="c0349-110">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0349-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="c0349-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0349-111">EXAMPLES</span></span>

### <span data-ttu-id="c0349-112">Exempel 1: stoppa en redigeringssession</span><span class="sxs-lookup"><span data-stu-id="c0349-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="c0349-113">I det här exemplet stoppar vi en session med namnet "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="c0349-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="c0349-114">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0349-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="c0349-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0349-115">PARAMETERS</span></span>

### <span data-ttu-id="c0349-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0349-116">-AsJob</span></span>
<span data-ttu-id="c0349-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c0349-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0349-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0349-118">-DefaultProfile</span></span>
<span data-ttu-id="c0349-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0349-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0349-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="c0349-120">-Location</span></span>
<span data-ttu-id="c0349-121">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="c0349-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c0349-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0349-122">-NetworkWatcher</span></span>
<span data-ttu-id="c0349-123">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="c0349-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="c0349-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c0349-124">-NetworkWatcherName</span></span>
<span data-ttu-id="c0349-125">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="c0349-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="c0349-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="c0349-126">-PacketCaptureName</span></span>
<span data-ttu-id="c0349-127">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="c0349-127">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0349-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0349-128">-PassThru</span></span>
<span data-ttu-id="c0349-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c0349-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="c0349-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0349-130">-ResourceGroupName</span></span>
<span data-ttu-id="c0349-131">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c0349-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c0349-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0349-132">-Confirm</span></span>
<span data-ttu-id="c0349-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0349-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0349-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0349-134">-WhatIf</span></span>
<span data-ttu-id="c0349-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0349-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0349-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0349-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0349-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0349-137">CommonParameters</span></span>
<span data-ttu-id="c0349-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0349-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0349-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0349-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0349-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0349-140">INPUTS</span></span>

### <span data-ttu-id="c0349-141">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0349-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c0349-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c0349-142">System.String</span></span>

## <span data-ttu-id="c0349-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0349-143">OUTPUTS</span></span>

### <span data-ttu-id="c0349-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0349-144">System.Boolean</span></span>

## <span data-ttu-id="c0349-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0349-145">NOTES</span></span>
<span data-ttu-id="c0349-146">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="c0349-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="c0349-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0349-147">RELATED LINKS</span></span>

[<span data-ttu-id="c0349-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0349-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0349-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c0349-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c0349-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0349-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0349-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0349-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0349-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0349-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c0349-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0349-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c0349-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0349-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c0349-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c0349-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c0349-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c0349-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c0349-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c0349-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c0349-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c0349-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c0349-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c0349-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c0349-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c0349-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c0349-161">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0349-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0349-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0349-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c0349-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c0349-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c0349-164">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0349-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0349-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0349-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0349-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0349-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0349-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c0349-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c0349-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0349-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0349-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0349-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0349-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c0349-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c0349-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c0349-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c0349-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c0349-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c0349-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c0349-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c0349-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0349-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
