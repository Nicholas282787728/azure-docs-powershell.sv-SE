---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: db3e3e529fd5c056acf793cd14280ef688c58a81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258791"
---
# <span data-ttu-id="98fe1-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="98fe1-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="98fe1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="98fe1-103">Hämtar fel söknings resultatet från den tidigare körningen eller fel söknings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="98fe1-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="98fe1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98fe1-104">SYNTAX</span></span>

### <span data-ttu-id="98fe1-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="98fe1-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fe1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="98fe1-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fe1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="98fe1-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98fe1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98fe1-108">DESCRIPTION</span></span>
<span data-ttu-id="98fe1-109">Get-AzNetworkWatcherTroubleshootingResult cmdlet får fel söknings resultatet från den tidigare körningen eller Start-AzNetworkWatcherResourceTroubleshooting åtgärden.</span><span class="sxs-lookup"><span data-stu-id="98fe1-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="98fe1-110">Om det pågår en fel söknings åtgärd kan det ta några minuter att slutföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="98fe1-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="98fe1-111">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="98fe1-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="98fe1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98fe1-112">EXAMPLES</span></span>

### <span data-ttu-id="98fe1-113">Exempel 1: starta fel sökning på en virtuell nätverksgateway och hämta resultat</span><span class="sxs-lookup"><span data-stu-id="98fe1-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="98fe1-114">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="98fe1-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="98fe1-115">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="98fe1-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="98fe1-116">När fel sökningen har startat görs ett Get-AzNetworkWatcherTroubleshootingResult-samtal till resursen för att hämta resultatet av samtalet.</span><span class="sxs-lookup"><span data-stu-id="98fe1-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="98fe1-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98fe1-117">PARAMETERS</span></span>

### <span data-ttu-id="98fe1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fe1-118">-DefaultProfile</span></span>
<span data-ttu-id="98fe1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98fe1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98fe1-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="98fe1-120">-Location</span></span>
<span data-ttu-id="98fe1-121">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="98fe1-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="98fe1-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98fe1-122">-NetworkWatcher</span></span>
<span data-ttu-id="98fe1-123">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="98fe1-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="98fe1-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="98fe1-124">-NetworkWatcherName</span></span>
<span data-ttu-id="98fe1-125">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="98fe1-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="98fe1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98fe1-126">-ResourceGroupName</span></span>
<span data-ttu-id="98fe1-127">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="98fe1-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="98fe1-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="98fe1-128">-TargetResourceId</span></span>
<span data-ttu-id="98fe1-129">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="98fe1-129">The target resource ID.</span></span>

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

### <span data-ttu-id="98fe1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fe1-130">CommonParameters</span></span>
<span data-ttu-id="98fe1-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98fe1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fe1-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98fe1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fe1-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98fe1-133">INPUTS</span></span>

### <span data-ttu-id="98fe1-134">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98fe1-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="98fe1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="98fe1-135">System.String</span></span>

## <span data-ttu-id="98fe1-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98fe1-136">OUTPUTS</span></span>

### <span data-ttu-id="98fe1-137">Microsoft. Azure. commands. Networks. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="98fe1-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="98fe1-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98fe1-138">NOTES</span></span>
<span data-ttu-id="98fe1-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="98fe1-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="98fe1-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98fe1-140">RELATED LINKS</span></span>

[<span data-ttu-id="98fe1-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98fe1-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="98fe1-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98fe1-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="98fe1-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98fe1-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="98fe1-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="98fe1-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="98fe1-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="98fe1-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="98fe1-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="98fe1-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="98fe1-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="98fe1-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="98fe1-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98fe1-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98fe1-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="98fe1-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="98fe1-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98fe1-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98fe1-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98fe1-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98fe1-152">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98fe1-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98fe1-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="98fe1-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="98fe1-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="98fe1-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="98fe1-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="98fe1-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="98fe1-156">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98fe1-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98fe1-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98fe1-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98fe1-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98fe1-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98fe1-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="98fe1-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="98fe1-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98fe1-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98fe1-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98fe1-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98fe1-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="98fe1-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="98fe1-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="98fe1-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="98fe1-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="98fe1-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="98fe1-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="98fe1-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="98fe1-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="98fe1-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="98fe1-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98fe1-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)