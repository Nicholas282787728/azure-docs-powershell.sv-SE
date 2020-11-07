---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ec7f6f910a50f479a923451fb9b893a5cabb5301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918225"
---
# <span data-ttu-id="df566-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="df566-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="df566-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df566-102">SYNOPSIS</span></span>
<span data-ttu-id="df566-103">Skapar en anslutnings övervakare.</span><span class="sxs-lookup"><span data-stu-id="df566-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="df566-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df566-104">SYNTAX</span></span>

### <span data-ttu-id="df566-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="df566-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df566-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="df566-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df566-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="df566-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df566-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df566-108">DESCRIPTION</span></span>
<span data-ttu-id="df566-109">Med den New-AzNetworkWatcherConnectionMonitor cmdleten skapas en anslutnings Övervakare för en viss källa och mål.</span><span class="sxs-lookup"><span data-stu-id="df566-109">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="df566-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df566-110">EXAMPLES</span></span>

### <span data-ttu-id="df566-111">Exempel 1: skapa en anslutnings Övervakare för ett virtuellt dator-och Internet mål</span><span class="sxs-lookup"><span data-stu-id="df566-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="df566-112">Med den New-AzNetworkWatcherConnectionMonitor cmdleten skapas en anslutnings Övervakare för en viss källa och mål.</span><span class="sxs-lookup"><span data-stu-id="df566-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="df566-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df566-113">PARAMETERS</span></span>

### <span data-ttu-id="df566-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df566-114">-AsJob</span></span>
<span data-ttu-id="df566-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="df566-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df566-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="df566-116">-ConfigureOnly</span></span>
<span data-ttu-id="df566-117">Konfigurera anslutnings övervakaren men starta den inte</span><span class="sxs-lookup"><span data-stu-id="df566-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="df566-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df566-118">-DefaultProfile</span></span>
<span data-ttu-id="df566-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df566-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df566-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="df566-120">-DestinationAddress</span></span>
<span data-ttu-id="df566-121">IP-adressen för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="df566-121">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df566-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="df566-122">-DestinationPort</span></span>
<span data-ttu-id="df566-123">Målport.</span><span class="sxs-lookup"><span data-stu-id="df566-123">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df566-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="df566-124">-DestinationResourceId</span></span>
<span data-ttu-id="df566-125">ID för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="df566-125">The ID of the connection monitor destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df566-126">-Force</span><span class="sxs-lookup"><span data-stu-id="df566-126">-Force</span></span>
<span data-ttu-id="df566-127">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="df566-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="df566-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="df566-128">-Location</span></span>
<span data-ttu-id="df566-129">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="df566-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="df566-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="df566-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="df566-131">Övervaknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="df566-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df566-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="df566-132">-Name</span></span>
<span data-ttu-id="df566-133">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="df566-133">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df566-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="df566-134">-NetworkWatcher</span></span>
<span data-ttu-id="df566-135">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="df566-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="df566-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="df566-136">-NetworkWatcherName</span></span>
<span data-ttu-id="df566-137">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="df566-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="df566-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df566-138">-ResourceGroupName</span></span>
<span data-ttu-id="df566-139">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="df566-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="df566-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="df566-140">-SourcePort</span></span>
<span data-ttu-id="df566-141">Källport.</span><span class="sxs-lookup"><span data-stu-id="df566-141">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df566-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="df566-142">-SourceResourceId</span></span>
<span data-ttu-id="df566-143">ID för källa för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="df566-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="df566-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="df566-144">-Tag</span></span>
<span data-ttu-id="df566-145">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="df566-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df566-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df566-146">-Confirm</span></span>
<span data-ttu-id="df566-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df566-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df566-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df566-148">-WhatIf</span></span>
<span data-ttu-id="df566-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df566-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df566-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df566-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df566-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df566-151">CommonParameters</span></span>
<span data-ttu-id="df566-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df566-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df566-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df566-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df566-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df566-154">INPUTS</span></span>

### <span data-ttu-id="df566-155">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="df566-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="df566-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df566-156">OUTPUTS</span></span>

### <span data-ttu-id="df566-157">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="df566-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="df566-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df566-158">NOTES</span></span>
<span data-ttu-id="df566-159">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="df566-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="df566-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df566-160">RELATED LINKS</span></span>

[<span data-ttu-id="df566-161">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="df566-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="df566-162">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="df566-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="df566-163">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="df566-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="df566-164">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="df566-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="df566-165">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="df566-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="df566-166">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="df566-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="df566-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="df566-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="df566-168">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="df566-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="df566-169">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="df566-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="df566-170">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="df566-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="df566-171">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="df566-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="df566-172">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="df566-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="df566-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="df566-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="df566-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="df566-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="df566-175">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="df566-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="df566-176">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="df566-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="df566-177">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="df566-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="df566-178">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="df566-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="df566-179">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="df566-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="df566-180">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="df566-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="df566-181">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="df566-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="df566-182">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="df566-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="df566-183">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="df566-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="df566-184">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="df566-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="df566-185">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="df566-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="df566-186">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="df566-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="df566-187">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="df566-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
