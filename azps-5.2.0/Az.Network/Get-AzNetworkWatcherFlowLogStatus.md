---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: dd88c40876bf3ceb5f90a7088f5943fcf5f18ce8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409931"
---
# <span data-ttu-id="6c478-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6c478-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="6c478-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c478-102">SYNOPSIS</span></span>
<span data-ttu-id="6c478-103">Hämtar status för flödes loggning för en resurs.</span><span class="sxs-lookup"><span data-stu-id="6c478-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="6c478-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c478-104">SYNTAX</span></span>

### <span data-ttu-id="6c478-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="6c478-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c478-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6c478-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c478-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6c478-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c478-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c478-108">DESCRIPTION</span></span>
<span data-ttu-id="6c478-109">Get-AzNetworkWatcherFlowLogStatus cmdlet får statusen för flödes loggning för en resurs.</span><span class="sxs-lookup"><span data-stu-id="6c478-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="6c478-110">Statusen inkluderar om flödes loggning är aktiverat för den angivna resursen, det konfigurerade lagrings kontot för att skicka loggar och bevarande princip för loggarna.</span><span class="sxs-lookup"><span data-stu-id="6c478-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="6c478-111">För närvarande stöds nätverks säkerhets grupper för flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="6c478-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="6c478-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c478-112">EXAMPLES</span></span>

### <span data-ttu-id="6c478-113">Exempel 1: få loggnings status för flödet för ett angivet NSG</span><span class="sxs-lookup"><span data-stu-id="6c478-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="6c478-114">I det här exemplet får du status för flödes loggning för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="6c478-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="6c478-115">Den angivna NSG har flödes loggning aktive rad, standard format och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="6c478-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="6c478-116">Exempel 2: Hämta flödes loggning och trafik analys för en viss NSG</span><span class="sxs-lookup"><span data-stu-id="6c478-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="6c478-117">I det här exemplet får du en säkerhets grupp för flödes loggning och trafik analys.</span><span class="sxs-lookup"><span data-stu-id="6c478-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="6c478-118">Den angivna NSG har flödes loggning och Traffic Analytics aktive rad, standard format och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="6c478-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="6c478-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c478-119">PARAMETERS</span></span>

### <span data-ttu-id="6c478-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c478-120">-AsJob</span></span>
<span data-ttu-id="6c478-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6c478-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c478-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c478-122">-DefaultProfile</span></span>
<span data-ttu-id="6c478-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c478-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c478-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="6c478-124">-Location</span></span>
<span data-ttu-id="6c478-125">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="6c478-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6c478-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c478-126">-NetworkWatcher</span></span>
<span data-ttu-id="6c478-127">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="6c478-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="6c478-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6c478-128">-NetworkWatcherName</span></span>
<span data-ttu-id="6c478-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="6c478-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="6c478-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c478-130">-ResourceGroupName</span></span>
<span data-ttu-id="6c478-131">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6c478-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6c478-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6c478-132">-TargetResourceId</span></span>
<span data-ttu-id="6c478-133">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6c478-133">The target resource ID.</span></span>

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

### <span data-ttu-id="6c478-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c478-134">CommonParameters</span></span>
<span data-ttu-id="6c478-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c478-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c478-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c478-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c478-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c478-137">INPUTS</span></span>

### <span data-ttu-id="6c478-138">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c478-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="6c478-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6c478-139">System.String</span></span>

## <span data-ttu-id="6c478-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c478-140">OUTPUTS</span></span>

### <span data-ttu-id="6c478-141">Microsoft. Azure. commands. Networks. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="6c478-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="6c478-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c478-142">NOTES</span></span>
<span data-ttu-id="6c478-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, flöde, loggar, flowlog, loggning</span><span class="sxs-lookup"><span data-stu-id="6c478-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="6c478-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c478-144">RELATED LINKS</span></span>

[<span data-ttu-id="6c478-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c478-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6c478-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c478-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6c478-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c478-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6c478-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6c478-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6c478-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6c478-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6c478-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6c478-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6c478-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6c478-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6c478-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c478-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c478-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6c478-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6c478-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c478-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c478-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c478-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c478-156">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c478-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c478-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c478-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6c478-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6c478-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6c478-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6c478-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6c478-160">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c478-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c478-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c478-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c478-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c478-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c478-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6c478-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6c478-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c478-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c478-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c478-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c478-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6c478-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6c478-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6c478-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6c478-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6c478-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6c478-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6c478-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6c478-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6c478-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="6c478-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c478-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
