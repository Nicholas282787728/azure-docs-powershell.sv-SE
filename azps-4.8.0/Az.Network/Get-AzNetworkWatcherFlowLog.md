---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5f4322ba81cdae5bdb0b33c2658a6d7934ed638d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258806"
---
# <span data-ttu-id="49c21-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="49c21-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="49c21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49c21-102">SYNOPSIS</span></span>
<span data-ttu-id="49c21-103">Hämtar en flödes logg resurs eller en lista över resurser för flödes loggar i angivet abonnemang och region.</span><span class="sxs-lookup"><span data-stu-id="49c21-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="49c21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49c21-104">SYNTAX</span></span>

### <span data-ttu-id="49c21-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="49c21-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49c21-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="49c21-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49c21-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="49c21-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49c21-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="49c21-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49c21-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49c21-109">DESCRIPTION</span></span>
<span data-ttu-id="49c21-110">Hämtar en flödes logg resurs eller en lista över resurser för flödes loggar i angivet abonnemang och region.</span><span class="sxs-lookup"><span data-stu-id="49c21-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="49c21-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49c21-111">EXAMPLES</span></span>

### <span data-ttu-id="49c21-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="49c21-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="49c21-113">Namn: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid inspirerar/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest etag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: lyckades plats: öster TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/nonstorage Enabled: true RetentionPolicy: {"Days": 5, "Enabled": true} format: {"typ": "JSON", "version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "öster", "workspaceResourceId": "/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr Oups/FlowLogsV2Demo/providers/Microsoft. OperationalInsights/arbets ytan", "trafficAnalyticsInterval": 60}</span><span class="sxs-lookup"><span data-stu-id="49c21-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="49c21-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49c21-114">PARAMETERS</span></span>

### <span data-ttu-id="49c21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c21-115">-DefaultProfile</span></span>
<span data-ttu-id="49c21-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49c21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c21-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="49c21-117">-Location</span></span>
<span data-ttu-id="49c21-118">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="49c21-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c21-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="49c21-119">-Name</span></span>
<span data-ttu-id="49c21-120">Flödets logg namn.</span><span class="sxs-lookup"><span data-stu-id="49c21-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c21-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49c21-121">-NetworkWatcher</span></span>
<span data-ttu-id="49c21-122">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="49c21-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="49c21-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="49c21-123">-NetworkWatcherName</span></span>
<span data-ttu-id="49c21-124">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="49c21-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c21-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c21-125">-ResourceGroupName</span></span>
<span data-ttu-id="49c21-126">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="49c21-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c21-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49c21-127">-ResourceId</span></span>
<span data-ttu-id="49c21-128">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="49c21-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c21-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c21-129">CommonParameters</span></span>
<span data-ttu-id="49c21-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c21-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c21-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49c21-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c21-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49c21-132">INPUTS</span></span>

### <span data-ttu-id="49c21-133">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49c21-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="49c21-134">System. String</span><span class="sxs-lookup"><span data-stu-id="49c21-134">System.String</span></span>

## <span data-ttu-id="49c21-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49c21-135">OUTPUTS</span></span>

### <span data-ttu-id="49c21-136">Microsoft. Azure. commands. Networks. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="49c21-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="49c21-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49c21-137">NOTES</span></span>

## <span data-ttu-id="49c21-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49c21-138">RELATED LINKS</span></span>

[<span data-ttu-id="49c21-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49c21-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="49c21-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49c21-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="49c21-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49c21-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="49c21-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="49c21-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="49c21-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="49c21-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="49c21-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="49c21-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="49c21-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="49c21-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="49c21-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49c21-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49c21-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="49c21-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="49c21-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49c21-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49c21-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49c21-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49c21-150">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49c21-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49c21-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="49c21-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="49c21-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="49c21-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="49c21-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="49c21-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="49c21-154">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49c21-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49c21-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49c21-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49c21-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49c21-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49c21-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="49c21-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="49c21-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49c21-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49c21-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49c21-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49c21-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="49c21-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="49c21-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="49c21-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="49c21-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="49c21-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="49c21-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="49c21-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="49c21-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="49c21-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="49c21-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49c21-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="49c21-166">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="49c21-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="49c21-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="49c21-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="49c21-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="49c21-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
