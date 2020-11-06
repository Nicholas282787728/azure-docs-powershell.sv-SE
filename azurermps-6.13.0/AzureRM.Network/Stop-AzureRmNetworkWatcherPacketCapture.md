---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: fc78481ceeec796fe4a498bf76092955adb1639a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578851"
---
# <span data-ttu-id="c0460-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0460-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="c0460-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0460-102">SYNOPSIS</span></span>
<span data-ttu-id="c0460-103">Stoppar en session med pågående paket</span><span class="sxs-lookup"><span data-stu-id="c0460-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0460-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0460-104">SYNTAX</span></span>

### <span data-ttu-id="c0460-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="c0460-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0460-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c0460-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0460-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c0460-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0460-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0460-108">DESCRIPTION</span></span>
<span data-ttu-id="c0460-109">Stop-AzureRmNetworkWatcherPacketCapture stoppar sändningen av en pågående paket.</span><span class="sxs-lookup"><span data-stu-id="c0460-109">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="c0460-110">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0460-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="c0460-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0460-111">EXAMPLES</span></span>

### <span data-ttu-id="c0460-112">Exempel 1: stoppa en redigeringssession</span><span class="sxs-lookup"><span data-stu-id="c0460-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="c0460-113">I det här exemplet stoppar vi en session med namnet "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="c0460-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="c0460-114">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0460-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="c0460-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0460-115">PARAMETERS</span></span>

### <span data-ttu-id="c0460-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0460-116">-AsJob</span></span>
<span data-ttu-id="c0460-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c0460-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0460-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0460-118">-DefaultProfile</span></span>
<span data-ttu-id="c0460-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0460-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0460-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="c0460-120">-Location</span></span>
<span data-ttu-id="c0460-121">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="c0460-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c0460-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0460-122">-NetworkWatcher</span></span>
<span data-ttu-id="c0460-123">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="c0460-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="c0460-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c0460-124">-NetworkWatcherName</span></span>
<span data-ttu-id="c0460-125">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="c0460-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="c0460-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="c0460-126">-PacketCaptureName</span></span>
<span data-ttu-id="c0460-127">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="c0460-127">The packet capture name.</span></span>

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

### <span data-ttu-id="c0460-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0460-128">-PassThru</span></span>
<span data-ttu-id="c0460-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c0460-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c0460-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0460-130">-ResourceGroupName</span></span>
<span data-ttu-id="c0460-131">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c0460-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c0460-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0460-132">-Confirm</span></span>
<span data-ttu-id="c0460-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0460-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0460-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0460-134">-WhatIf</span></span>
<span data-ttu-id="c0460-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0460-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0460-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0460-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0460-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0460-137">CommonParameters</span></span>
<span data-ttu-id="c0460-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0460-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0460-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0460-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0460-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0460-140">INPUTS</span></span>

### <span data-ttu-id="c0460-141">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0460-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c0460-142">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c0460-142">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="c0460-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c0460-143">System.String</span></span>
<span data-ttu-id="c0460-144">Parametrar: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c0460-144">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="c0460-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0460-145">OUTPUTS</span></span>

### <span data-ttu-id="c0460-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0460-146">System.Boolean</span></span>

## <span data-ttu-id="c0460-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0460-147">NOTES</span></span>
<span data-ttu-id="c0460-148">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="c0460-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="c0460-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0460-149">RELATED LINKS</span></span>

[<span data-ttu-id="c0460-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0460-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0460-151">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c0460-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c0460-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0460-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0460-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0460-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0460-154">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0460-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0460-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0460-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0460-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0460-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0460-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c0460-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c0460-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c0460-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c0460-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c0460-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c0460-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c0460-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c0460-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c0460-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c0460-162">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c0460-162">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c0460-163">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0460-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0460-164">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0460-164">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c0460-165">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c0460-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="c0460-166">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0460-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0460-167">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0460-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0460-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0460-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0460-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c0460-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c0460-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0460-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0460-171">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0460-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0460-172">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c0460-172">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c0460-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c0460-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c0460-174">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c0460-174">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c0460-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c0460-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c0460-176">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0460-176">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
