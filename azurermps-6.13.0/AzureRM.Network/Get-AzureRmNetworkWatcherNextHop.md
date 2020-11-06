---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 4c6a1e179cf0c6086035488d092232e85c570637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576244"
---
# <span data-ttu-id="41e3e-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="41e3e-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="41e3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="41e3e-103">Hämtar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="41e3e-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41e3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41e3e-104">SYNTAX</span></span>

### <span data-ttu-id="41e3e-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="41e3e-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41e3e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="41e3e-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41e3e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="41e3e-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41e3e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41e3e-108">DESCRIPTION</span></span>
<span data-ttu-id="41e3e-109">Get-AzureRmNetworkWatcherNextHop cmdlet tar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="41e3e-109">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="41e3e-110">Med nästa hopp kan du Visa typen av Azure-resurs, den associerade IP-adressen för den resursen och regeln för routningstabellen som är ansvarig för vägen.</span><span class="sxs-lookup"><span data-stu-id="41e3e-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="41e3e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41e3e-111">EXAMPLES</span></span>

### <span data-ttu-id="41e3e-112">Exempel 1: få nästa hopp när du kommunicerar med en Internet-IP</span><span class="sxs-lookup"><span data-stu-id="41e3e-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="41e3e-113">Får nästa hopp för utgående kommunikation från det primära nätverks gränssnittet på den angivna virtuella Vachine till 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="41e3e-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="41e3e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41e3e-114">PARAMETERS</span></span>

### <span data-ttu-id="41e3e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41e3e-115">-AsJob</span></span>
<span data-ttu-id="41e3e-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="41e3e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41e3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e3e-117">-DefaultProfile</span></span>
<span data-ttu-id="41e3e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41e3e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41e3e-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="41e3e-119">-DestinationIPAddress</span></span>
<span data-ttu-id="41e3e-120">Mål-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="41e3e-120">Destination IP address.</span></span>

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

### <span data-ttu-id="41e3e-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="41e3e-121">-Location</span></span>
<span data-ttu-id="41e3e-122">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="41e3e-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="41e3e-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e3e-123">-NetworkWatcher</span></span>
<span data-ttu-id="41e3e-124">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="41e3e-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="41e3e-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="41e3e-125">-NetworkWatcherName</span></span>
<span data-ttu-id="41e3e-126">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="41e3e-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="41e3e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e3e-127">-ResourceGroupName</span></span>
<span data-ttu-id="41e3e-128">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="41e3e-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="41e3e-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="41e3e-129">-SourceIPAddress</span></span>
<span data-ttu-id="41e3e-130">Käll-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="41e3e-130">Source IP address.</span></span>

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

### <span data-ttu-id="41e3e-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="41e3e-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="41e3e-132">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="41e3e-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="41e3e-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="41e3e-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="41e3e-134">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="41e3e-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="41e3e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e3e-135">CommonParameters</span></span>
<span data-ttu-id="41e3e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e3e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e3e-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41e3e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e3e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41e3e-138">INPUTS</span></span>

### <span data-ttu-id="41e3e-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e3e-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="41e3e-140">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41e3e-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="41e3e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="41e3e-141">System.String</span></span>
<span data-ttu-id="41e3e-142">Parametrar: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41e3e-142">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="41e3e-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41e3e-143">OUTPUTS</span></span>

### <span data-ttu-id="41e3e-144">Microsoft. Azure. commands. Networks. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="41e3e-144">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="41e3e-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41e3e-145">NOTES</span></span>
<span data-ttu-id="41e3e-146">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="41e3e-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="41e3e-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41e3e-147">RELATED LINKS</span></span>

[<span data-ttu-id="41e3e-148">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e3e-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41e3e-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e3e-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41e3e-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="41e3e-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="41e3e-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="41e3e-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="41e3e-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="41e3e-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="41e3e-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="41e3e-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="41e3e-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="41e3e-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="41e3e-155">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41e3e-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41e3e-156">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="41e3e-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="41e3e-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41e3e-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41e3e-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41e3e-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41e3e-159">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="41e3e-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="41e3e-160">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="41e3e-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="41e3e-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="41e3e-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="41e3e-162">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="41e3e-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="41e3e-163">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="41e3e-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="41e3e-164">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="41e3e-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="41e3e-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="41e3e-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="41e3e-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="41e3e-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="41e3e-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="41e3e-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="41e3e-168">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="41e3e-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="41e3e-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="41e3e-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="41e3e-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="41e3e-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="41e3e-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="41e3e-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="41e3e-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="41e3e-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="41e3e-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="41e3e-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="41e3e-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="41e3e-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
