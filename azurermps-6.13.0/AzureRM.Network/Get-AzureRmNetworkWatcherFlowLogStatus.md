---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: a045acd86141b57d02fef9931cfb01ff8b783e8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755703"
---
# <span data-ttu-id="aad0a-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="aad0a-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="aad0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aad0a-102">SYNOPSIS</span></span>
<span data-ttu-id="aad0a-103">Hämtar status för flödes loggning för en resurs.</span><span class="sxs-lookup"><span data-stu-id="aad0a-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aad0a-104">SYNTAX</span></span>

### <span data-ttu-id="aad0a-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="aad0a-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aad0a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="aad0a-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aad0a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="aad0a-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aad0a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aad0a-108">DESCRIPTION</span></span>
<span data-ttu-id="aad0a-109">Get-AzureRmNetworkWatcherFlowLogStatus cmdlet får statusen för flödes loggning för en resurs.</span><span class="sxs-lookup"><span data-stu-id="aad0a-109">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="aad0a-110">Statusen inkluderar om flödes loggning är aktiverat för den angivna resursen, det konfigurerade lagrings kontot för att skicka loggar och bevarande princip för loggarna.</span><span class="sxs-lookup"><span data-stu-id="aad0a-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="aad0a-111">För närvarande stöds nätverks säkerhets grupper för flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="aad0a-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="aad0a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aad0a-112">EXAMPLES</span></span>

### <span data-ttu-id="aad0a-113">Exempel 1: få loggnings status för flödet för ett angivet NSG</span><span class="sxs-lookup"><span data-stu-id="aad0a-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="aad0a-114">I det här exemplet får du status för flödes loggning för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="aad0a-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="aad0a-115">Den angivna NSG har flödes loggning aktive rad och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="aad0a-115">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

### <span data-ttu-id="aad0a-116">Exempel 2: Hämta flödes loggning och trafik analys för en viss NSG</span><span class="sxs-lookup"><span data-stu-id="aad0a-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName"
            }
          }
```

<span data-ttu-id="aad0a-117">I det här exemplet får du en säkerhets grupp för flödes loggning och trafik analys.</span><span class="sxs-lookup"><span data-stu-id="aad0a-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="aad0a-118">Den angivna NSG har flödes loggning och Traffic Analytics aktiverat och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="aad0a-118">The specified NSG has flow logging and Traffic Analytics enabled, and no retention policy set.</span></span>

## <span data-ttu-id="aad0a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aad0a-119">PARAMETERS</span></span>

### <span data-ttu-id="aad0a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aad0a-120">-AsJob</span></span>
<span data-ttu-id="aad0a-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="aad0a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aad0a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad0a-122">-DefaultProfile</span></span>
<span data-ttu-id="aad0a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aad0a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aad0a-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="aad0a-124">-Location</span></span>
<span data-ttu-id="aad0a-125">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="aad0a-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="aad0a-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aad0a-126">-NetworkWatcher</span></span>
<span data-ttu-id="aad0a-127">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="aad0a-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="aad0a-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="aad0a-128">-NetworkWatcherName</span></span>
<span data-ttu-id="aad0a-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="aad0a-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="aad0a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad0a-130">-ResourceGroupName</span></span>
<span data-ttu-id="aad0a-131">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="aad0a-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="aad0a-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="aad0a-132">-TargetResourceId</span></span>
<span data-ttu-id="aad0a-133">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="aad0a-133">The target resource ID.</span></span>

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

### <span data-ttu-id="aad0a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad0a-134">CommonParameters</span></span>
<span data-ttu-id="aad0a-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad0a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad0a-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad0a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad0a-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aad0a-137">INPUTS</span></span>

### <span data-ttu-id="aad0a-138">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aad0a-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="aad0a-139">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aad0a-139">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="aad0a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aad0a-140">System.String</span></span>
<span data-ttu-id="aad0a-141">Parametrar: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aad0a-141">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="aad0a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aad0a-142">OUTPUTS</span></span>

### <span data-ttu-id="aad0a-143">Microsoft. Azure. commands. Networks. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="aad0a-143">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="aad0a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aad0a-144">NOTES</span></span>
<span data-ttu-id="aad0a-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, flöde, loggar, flowlog, loggning</span><span class="sxs-lookup"><span data-stu-id="aad0a-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="aad0a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aad0a-146">RELATED LINKS</span></span>

[<span data-ttu-id="aad0a-147">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aad0a-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="aad0a-148">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aad0a-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="aad0a-149">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aad0a-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="aad0a-150">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="aad0a-150">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="aad0a-151">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="aad0a-151">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="aad0a-152">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="aad0a-152">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="aad0a-153">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="aad0a-153">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="aad0a-154">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aad0a-154">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aad0a-155">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="aad0a-155">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="aad0a-156">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aad0a-156">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aad0a-157">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aad0a-157">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aad0a-158">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aad0a-158">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aad0a-159">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad0a-159">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="aad0a-160">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="aad0a-160">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="aad0a-161">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="aad0a-161">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="aad0a-162">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aad0a-162">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aad0a-163">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aad0a-163">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aad0a-164">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aad0a-164">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aad0a-165">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="aad0a-165">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="aad0a-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aad0a-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aad0a-167">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aad0a-167">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aad0a-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="aad0a-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="aad0a-169">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="aad0a-169">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="aad0a-170">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="aad0a-170">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="aad0a-171">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="aad0a-171">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="aad0a-172">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="aad0a-172">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="aad0a-173">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aad0a-173">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
