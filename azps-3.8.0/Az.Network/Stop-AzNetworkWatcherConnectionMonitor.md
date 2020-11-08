---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 8840fc454601880fd2d4ed8bf7b816f7f3d83e5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090513"
---
# <span data-ttu-id="f22ba-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f22ba-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="f22ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f22ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f22ba-103">Stoppa en anslutnings övervakare</span><span class="sxs-lookup"><span data-stu-id="f22ba-103">Stop a connection monitor</span></span>

## <span data-ttu-id="f22ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f22ba-104">SYNTAX</span></span>

### <span data-ttu-id="f22ba-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="f22ba-105">SetByName (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f22ba-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f22ba-106">SetByResource</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f22ba-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f22ba-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f22ba-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f22ba-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f22ba-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f22ba-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f22ba-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f22ba-110">DESCRIPTION</span></span>
<span data-ttu-id="f22ba-111">Stop-AzNetworkWatcherConnectionMonitor cmdlet stoppar den angivna anslutnings skärmen.</span><span class="sxs-lookup"><span data-stu-id="f22ba-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="f22ba-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f22ba-112">EXAMPLES</span></span>

### <span data-ttu-id="f22ba-113">Exempel 1: stoppa en anslutnings bildskärm</span><span class="sxs-lookup"><span data-stu-id="f22ba-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="f22ba-114">I det här exemplet stoppar vi anslutnings övervakaren som anges med namn och nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="f22ba-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="f22ba-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f22ba-115">PARAMETERS</span></span>

### <span data-ttu-id="f22ba-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f22ba-116">-AsJob</span></span>
<span data-ttu-id="f22ba-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f22ba-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f22ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22ba-118">-DefaultProfile</span></span>
<span data-ttu-id="f22ba-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f22ba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f22ba-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f22ba-120">-InputObject</span></span>
<span data-ttu-id="f22ba-121">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="f22ba-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f22ba-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="f22ba-122">-Location</span></span>
<span data-ttu-id="f22ba-123">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="f22ba-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f22ba-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="f22ba-124">-Name</span></span>
<span data-ttu-id="f22ba-125">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="f22ba-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22ba-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f22ba-126">-NetworkWatcher</span></span>
<span data-ttu-id="f22ba-127">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="f22ba-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="f22ba-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f22ba-128">-NetworkWatcherName</span></span>
<span data-ttu-id="f22ba-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="f22ba-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22ba-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f22ba-130">-PassThru</span></span>
<span data-ttu-id="f22ba-131">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f22ba-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="f22ba-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22ba-132">-ResourceGroupName</span></span>
<span data-ttu-id="f22ba-133">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f22ba-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22ba-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22ba-134">-ResourceId</span></span>
<span data-ttu-id="f22ba-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f22ba-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f22ba-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f22ba-136">-Confirm</span></span>
<span data-ttu-id="f22ba-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f22ba-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f22ba-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f22ba-138">-WhatIf</span></span>
<span data-ttu-id="f22ba-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f22ba-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f22ba-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f22ba-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f22ba-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22ba-141">CommonParameters</span></span>
<span data-ttu-id="f22ba-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f22ba-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22ba-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f22ba-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22ba-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f22ba-144">INPUTS</span></span>

### <span data-ttu-id="f22ba-145">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f22ba-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f22ba-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f22ba-146">System.String</span></span>

### <span data-ttu-id="f22ba-147">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="f22ba-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="f22ba-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f22ba-148">OUTPUTS</span></span>

### <span data-ttu-id="f22ba-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f22ba-149">System.Boolean</span></span>

## <span data-ttu-id="f22ba-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f22ba-150">NOTES</span></span>
<span data-ttu-id="f22ba-151">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="f22ba-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="f22ba-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f22ba-152">RELATED LINKS</span></span>

[<span data-ttu-id="f22ba-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f22ba-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f22ba-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f22ba-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f22ba-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f22ba-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f22ba-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f22ba-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f22ba-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f22ba-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f22ba-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f22ba-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f22ba-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f22ba-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f22ba-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f22ba-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f22ba-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f22ba-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f22ba-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f22ba-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f22ba-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f22ba-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f22ba-164">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f22ba-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f22ba-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f22ba-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f22ba-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f22ba-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f22ba-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f22ba-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f22ba-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f22ba-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f22ba-169">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f22ba-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f22ba-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f22ba-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f22ba-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22ba-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f22ba-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f22ba-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f22ba-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f22ba-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f22ba-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f22ba-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f22ba-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f22ba-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f22ba-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f22ba-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f22ba-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f22ba-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f22ba-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f22ba-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f22ba-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f22ba-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
