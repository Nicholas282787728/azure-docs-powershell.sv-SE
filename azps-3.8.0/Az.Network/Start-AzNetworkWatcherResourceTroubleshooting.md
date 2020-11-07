---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: e8e8b9dfd217f9407af8db18a5f468d7d971c97d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925986"
---
# <span data-ttu-id="db4a2-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="db4a2-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="db4a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="db4a2-103">Startar fel sökning på en nätverks resurs i Azure.</span><span class="sxs-lookup"><span data-stu-id="db4a2-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="db4a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db4a2-104">SYNTAX</span></span>

### <span data-ttu-id="db4a2-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="db4a2-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db4a2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="db4a2-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db4a2-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="db4a2-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db4a2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db4a2-108">DESCRIPTION</span></span>
<span data-ttu-id="db4a2-109">Start-AzNetworkWatcherResourceTroubleshooting-cmdleten startar fel sökning för en nätverks resurs i Azure och returnerar information om potentiella problem och begränsningar.</span><span class="sxs-lookup"><span data-stu-id="db4a2-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="db4a2-110">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="db4a2-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="db4a2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db4a2-111">EXAMPLES</span></span>

### <span data-ttu-id="db4a2-112">Exempel 1: starta fel sökning på en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="db4a2-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="db4a2-113">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="db4a2-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="db4a2-114">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="db4a2-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="db4a2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db4a2-115">PARAMETERS</span></span>

### <span data-ttu-id="db4a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4a2-116">-DefaultProfile</span></span>
<span data-ttu-id="db4a2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db4a2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db4a2-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="db4a2-118">-Location</span></span>
<span data-ttu-id="db4a2-119">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="db4a2-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="db4a2-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="db4a2-120">-NetworkWatcher</span></span>
<span data-ttu-id="db4a2-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="db4a2-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="db4a2-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="db4a2-122">-NetworkWatcherName</span></span>
<span data-ttu-id="db4a2-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="db4a2-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="db4a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db4a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="db4a2-125">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="db4a2-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="db4a2-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="db4a2-126">-StorageId</span></span>
<span data-ttu-id="db4a2-127">Lagrings-ID.</span><span class="sxs-lookup"><span data-stu-id="db4a2-127">The storage ID.</span></span>

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

### <span data-ttu-id="db4a2-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="db4a2-128">-StoragePath</span></span>
<span data-ttu-id="db4a2-129">Lagrings Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="db4a2-129">The storage path.</span></span>

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

### <span data-ttu-id="db4a2-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="db4a2-130">-TargetResourceId</span></span>
<span data-ttu-id="db4a2-131">Anger resurs-ID för den resurs som ska felsökas.</span><span class="sxs-lookup"><span data-stu-id="db4a2-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="db4a2-132">Exempel format: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="db4a2-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="db4a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4a2-133">CommonParameters</span></span>
<span data-ttu-id="db4a2-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db4a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4a2-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db4a2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4a2-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db4a2-136">INPUTS</span></span>

### <span data-ttu-id="db4a2-137">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="db4a2-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="db4a2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="db4a2-138">System.String</span></span>

## <span data-ttu-id="db4a2-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db4a2-139">OUTPUTS</span></span>

### <span data-ttu-id="db4a2-140">Microsoft. Azure. commands. Networks. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="db4a2-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="db4a2-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db4a2-141">NOTES</span></span>
<span data-ttu-id="db4a2-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="db4a2-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="db4a2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db4a2-143">RELATED LINKS</span></span>

[<span data-ttu-id="db4a2-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="db4a2-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="db4a2-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="db4a2-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="db4a2-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="db4a2-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="db4a2-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="db4a2-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="db4a2-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="db4a2-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="db4a2-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="db4a2-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="db4a2-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="db4a2-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="db4a2-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="db4a2-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="db4a2-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="db4a2-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="db4a2-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="db4a2-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="db4a2-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="db4a2-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="db4a2-155">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="db4a2-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="db4a2-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="db4a2-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="db4a2-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="db4a2-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="db4a2-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="db4a2-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="db4a2-159">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="db4a2-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="db4a2-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="db4a2-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="db4a2-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="db4a2-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="db4a2-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="db4a2-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="db4a2-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="db4a2-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="db4a2-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="db4a2-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="db4a2-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="db4a2-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="db4a2-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="db4a2-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="db4a2-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="db4a2-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="db4a2-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="db4a2-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="db4a2-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="db4a2-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="db4a2-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="db4a2-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)