---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: d0f4661a2b4814fc1c4b5692de6c56865cfa6be9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756019"
---
# <span data-ttu-id="905ba-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="905ba-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="905ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="905ba-102">SYNOPSIS</span></span>
<span data-ttu-id="905ba-103">Startar fel sökning på en nätverks resurs i Azure.</span><span class="sxs-lookup"><span data-stu-id="905ba-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="905ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="905ba-104">SYNTAX</span></span>

### <span data-ttu-id="905ba-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="905ba-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="905ba-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="905ba-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="905ba-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="905ba-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="905ba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="905ba-108">DESCRIPTION</span></span>
<span data-ttu-id="905ba-109">Start-AzureRmNetworkWatcherResourceTroubleshooting-cmdleten startar fel sökning för en nätverks resurs i Azure och returnerar information om potentiella problem och begränsningar.</span><span class="sxs-lookup"><span data-stu-id="905ba-109">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="905ba-110">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="905ba-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="905ba-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="905ba-111">EXAMPLES</span></span>

### <span data-ttu-id="905ba-112">Exempel 1: starta fel sökning på en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="905ba-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="905ba-113">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="905ba-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="905ba-114">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="905ba-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="905ba-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="905ba-115">PARAMETERS</span></span>

### <span data-ttu-id="905ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905ba-116">-DefaultProfile</span></span>
<span data-ttu-id="905ba-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="905ba-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="905ba-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="905ba-118">-Location</span></span>
<span data-ttu-id="905ba-119">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="905ba-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="905ba-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="905ba-120">-NetworkWatcher</span></span>
<span data-ttu-id="905ba-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="905ba-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="905ba-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="905ba-122">-NetworkWatcherName</span></span>
<span data-ttu-id="905ba-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="905ba-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="905ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="905ba-125">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="905ba-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="905ba-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="905ba-126">-StorageId</span></span>
<span data-ttu-id="905ba-127">Lagrings-ID.</span><span class="sxs-lookup"><span data-stu-id="905ba-127">The storage ID.</span></span>

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

### <span data-ttu-id="905ba-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="905ba-128">-StoragePath</span></span>
<span data-ttu-id="905ba-129">Lagrings Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="905ba-129">The storage path.</span></span>

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

### <span data-ttu-id="905ba-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="905ba-130">-TargetResourceId</span></span>
<span data-ttu-id="905ba-131">Anger resurs-ID för den resurs som ska felsökas.</span><span class="sxs-lookup"><span data-stu-id="905ba-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="905ba-132">Exempel format: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="905ba-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="905ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905ba-133">CommonParameters</span></span>
<span data-ttu-id="905ba-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905ba-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="905ba-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905ba-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="905ba-136">INPUTS</span></span>

### <span data-ttu-id="905ba-137">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="905ba-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="905ba-138">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="905ba-138">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="905ba-139">System. String</span><span class="sxs-lookup"><span data-stu-id="905ba-139">System.String</span></span>
<span data-ttu-id="905ba-140">Parametrar: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="905ba-140">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="905ba-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="905ba-141">OUTPUTS</span></span>

### <span data-ttu-id="905ba-142">Microsoft. Azure. commands. Networks. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="905ba-142">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="905ba-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="905ba-143">NOTES</span></span>
<span data-ttu-id="905ba-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="905ba-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="905ba-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="905ba-145">RELATED LINKS</span></span>

[<span data-ttu-id="905ba-146">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="905ba-146">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="905ba-147">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="905ba-147">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="905ba-148">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="905ba-148">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="905ba-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="905ba-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="905ba-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="905ba-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="905ba-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="905ba-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="905ba-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="905ba-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="905ba-153">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="905ba-153">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="905ba-154">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="905ba-154">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="905ba-155">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="905ba-155">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="905ba-156">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="905ba-156">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="905ba-157">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="905ba-157">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="905ba-158">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="905ba-158">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="905ba-159">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="905ba-159">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="905ba-160">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="905ba-160">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="905ba-161">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="905ba-161">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="905ba-162">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="905ba-162">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="905ba-163">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="905ba-163">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="905ba-164">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="905ba-164">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="905ba-165">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="905ba-165">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="905ba-166">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="905ba-166">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="905ba-167">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="905ba-167">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="905ba-168">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="905ba-168">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="905ba-169">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="905ba-169">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="905ba-170">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="905ba-170">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="905ba-171">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="905ba-171">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="905ba-172">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="905ba-172">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
