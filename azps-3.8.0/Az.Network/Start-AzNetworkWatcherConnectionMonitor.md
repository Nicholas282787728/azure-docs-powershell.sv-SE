---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 83d7da65ad8c525d4c37ab1b5f78eb72bf1d9f49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925993"
---
# <span data-ttu-id="1a883-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a883-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="1a883-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a883-102">SYNOPSIS</span></span>
<span data-ttu-id="1a883-103">Starta en anslutnings övervakare</span><span class="sxs-lookup"><span data-stu-id="1a883-103">Start a connection monitor</span></span>

## <span data-ttu-id="1a883-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a883-104">SYNTAX</span></span>

### <span data-ttu-id="1a883-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="1a883-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a883-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1a883-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a883-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1a883-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a883-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a883-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a883-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1a883-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a883-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a883-110">DESCRIPTION</span></span>
<span data-ttu-id="1a883-111">Den angivna anslutnings övervakaren startas med Start-AzNetworkWatcherConnectionMonitor cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a883-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="1a883-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a883-112">EXAMPLES</span></span>

### <span data-ttu-id="1a883-113">Exempel 1: starta en anslutnings bildskärm</span><span class="sxs-lookup"><span data-stu-id="1a883-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="1a883-114">I det här exemplet startas anslutnings övervakaren som anges med namn och nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="1a883-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="1a883-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a883-115">PARAMETERS</span></span>

### <span data-ttu-id="1a883-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a883-116">-AsJob</span></span>
<span data-ttu-id="1a883-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1a883-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a883-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a883-118">-DefaultProfile</span></span>
<span data-ttu-id="1a883-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a883-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a883-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a883-120">-InputObject</span></span>
<span data-ttu-id="1a883-121">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="1a883-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="1a883-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="1a883-122">-Location</span></span>
<span data-ttu-id="1a883-123">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="1a883-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1a883-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a883-124">-Name</span></span>
<span data-ttu-id="1a883-125">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="1a883-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="1a883-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a883-126">-NetworkWatcher</span></span>
<span data-ttu-id="1a883-127">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="1a883-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="1a883-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1a883-128">-NetworkWatcherName</span></span>
<span data-ttu-id="1a883-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="1a883-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="1a883-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a883-130">-PassThru</span></span>
<span data-ttu-id="1a883-131">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="1a883-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="1a883-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a883-132">-ResourceGroupName</span></span>
<span data-ttu-id="1a883-133">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1a883-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1a883-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a883-134">-ResourceId</span></span>
<span data-ttu-id="1a883-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1a883-135">Resource ID.</span></span>

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

### <span data-ttu-id="1a883-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1a883-136">-Confirm</span></span>
<span data-ttu-id="1a883-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1a883-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a883-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a883-138">-WhatIf</span></span>
<span data-ttu-id="1a883-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1a883-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a883-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1a883-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a883-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a883-141">CommonParameters</span></span>
<span data-ttu-id="1a883-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a883-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a883-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a883-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a883-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a883-144">INPUTS</span></span>

### <span data-ttu-id="1a883-145">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a883-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1a883-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1a883-146">System.String</span></span>

### <span data-ttu-id="1a883-147">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="1a883-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="1a883-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a883-148">OUTPUTS</span></span>

### <span data-ttu-id="1a883-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a883-149">System.Boolean</span></span>

## <span data-ttu-id="1a883-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a883-150">NOTES</span></span>
<span data-ttu-id="1a883-151">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="1a883-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="1a883-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a883-152">RELATED LINKS</span></span>

[<span data-ttu-id="1a883-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a883-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1a883-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a883-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1a883-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a883-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1a883-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1a883-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1a883-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1a883-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1a883-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1a883-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1a883-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1a883-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1a883-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a883-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a883-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1a883-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1a883-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a883-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a883-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a883-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a883-164">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a883-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a883-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a883-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a883-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1a883-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1a883-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a883-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a883-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a883-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a883-169">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a883-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a883-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a883-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a883-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a883-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1a883-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1a883-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1a883-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1a883-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1a883-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1a883-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1a883-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a883-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a883-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1a883-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1a883-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1a883-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1a883-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1a883-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1a883-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1a883-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)