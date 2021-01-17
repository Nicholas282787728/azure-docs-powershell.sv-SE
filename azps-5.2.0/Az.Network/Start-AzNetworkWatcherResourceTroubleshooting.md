---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 0776b10a14236ac4806ccc166f24b1dd5a3ee3de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395496"
---
# <span data-ttu-id="752f6-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="752f6-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="752f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="752f6-102">SYNOPSIS</span></span>
<span data-ttu-id="752f6-103">Startar fel sökning på en nätverks resurs i Azure.</span><span class="sxs-lookup"><span data-stu-id="752f6-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="752f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="752f6-104">SYNTAX</span></span>

### <span data-ttu-id="752f6-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="752f6-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="752f6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="752f6-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="752f6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="752f6-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="752f6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="752f6-108">DESCRIPTION</span></span>
<span data-ttu-id="752f6-109">Start-AzNetworkWatcherResourceTroubleshooting-cmdleten startar fel sökning för en nätverks resurs i Azure och returnerar information om potentiella problem och begränsningar.</span><span class="sxs-lookup"><span data-stu-id="752f6-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="752f6-110">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="752f6-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="752f6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="752f6-111">EXAMPLES</span></span>

### <span data-ttu-id="752f6-112">Exempel 1: starta fel sökning på en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="752f6-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="752f6-113">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="752f6-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="752f6-114">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="752f6-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="752f6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="752f6-115">PARAMETERS</span></span>

### <span data-ttu-id="752f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752f6-116">-DefaultProfile</span></span>
<span data-ttu-id="752f6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="752f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="752f6-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="752f6-118">-Location</span></span>
<span data-ttu-id="752f6-119">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="752f6-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="752f6-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="752f6-120">-NetworkWatcher</span></span>
<span data-ttu-id="752f6-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="752f6-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="752f6-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="752f6-122">-NetworkWatcherName</span></span>
<span data-ttu-id="752f6-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="752f6-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="752f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="752f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="752f6-125">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="752f6-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="752f6-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="752f6-126">-StorageId</span></span>
<span data-ttu-id="752f6-127">Lagrings-ID.</span><span class="sxs-lookup"><span data-stu-id="752f6-127">The storage ID.</span></span>

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

### <span data-ttu-id="752f6-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="752f6-128">-StoragePath</span></span>
<span data-ttu-id="752f6-129">Lagrings Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="752f6-129">The storage path.</span></span>

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

### <span data-ttu-id="752f6-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="752f6-130">-TargetResourceId</span></span>
<span data-ttu-id="752f6-131">Anger resurs-ID för den resurs som ska felsökas.</span><span class="sxs-lookup"><span data-stu-id="752f6-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="752f6-132">Exempel format: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="752f6-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="752f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752f6-133">CommonParameters</span></span>
<span data-ttu-id="752f6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752f6-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="752f6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752f6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="752f6-136">INPUTS</span></span>

### <span data-ttu-id="752f6-137">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="752f6-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="752f6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="752f6-138">System.String</span></span>

## <span data-ttu-id="752f6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="752f6-139">OUTPUTS</span></span>

### <span data-ttu-id="752f6-140">Microsoft. Azure. commands. Networks. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="752f6-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="752f6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="752f6-141">NOTES</span></span>
<span data-ttu-id="752f6-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="752f6-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="752f6-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="752f6-143">RELATED LINKS</span></span>

[<span data-ttu-id="752f6-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="752f6-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="752f6-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="752f6-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="752f6-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="752f6-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="752f6-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="752f6-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="752f6-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="752f6-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="752f6-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="752f6-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="752f6-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="752f6-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="752f6-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="752f6-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="752f6-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="752f6-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="752f6-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="752f6-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="752f6-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="752f6-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="752f6-155">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="752f6-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="752f6-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="752f6-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="752f6-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="752f6-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="752f6-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="752f6-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="752f6-159">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="752f6-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="752f6-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="752f6-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="752f6-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="752f6-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="752f6-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="752f6-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="752f6-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="752f6-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="752f6-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="752f6-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="752f6-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="752f6-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="752f6-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="752f6-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="752f6-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="752f6-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="752f6-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="752f6-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="752f6-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="752f6-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="752f6-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="752f6-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
