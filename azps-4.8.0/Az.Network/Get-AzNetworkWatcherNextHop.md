---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: cf120e8e9ca9e0dad8f4d430c7f207d40fcfab3b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258802"
---
# <span data-ttu-id="0d7b6-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0d7b6-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="0d7b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7b6-103">Hämtar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="0d7b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d7b6-104">SYNTAX</span></span>

### <span data-ttu-id="0d7b6-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="0d7b6-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d7b6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0d7b6-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d7b6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0d7b6-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d7b6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d7b6-108">DESCRIPTION</span></span>
<span data-ttu-id="0d7b6-109">Get-AzNetworkWatcherNextHop cmdlet tar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="0d7b6-110">Med nästa hopp kan du Visa typen av Azure-resurs, den associerade IP-adressen för den resursen och regeln för routningstabellen som är ansvarig för vägen.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="0d7b6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d7b6-111">EXAMPLES</span></span>

### <span data-ttu-id="0d7b6-112">Exempel 1: få nästa hopp när du kommunicerar med en Internet-IP</span><span class="sxs-lookup"><span data-stu-id="0d7b6-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="0d7b6-113">Hämtar nästa hopp för utgående kommunikation från det primära nätverks gränssnittet på den angivna virtuella datorn till 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="0d7b6-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="0d7b6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d7b6-114">PARAMETERS</span></span>

### <span data-ttu-id="0d7b6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d7b6-115">-AsJob</span></span>
<span data-ttu-id="0d7b6-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0d7b6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d7b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7b6-117">-DefaultProfile</span></span>
<span data-ttu-id="0d7b6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d7b6-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="0d7b6-119">-DestinationIPAddress</span></span>
<span data-ttu-id="0d7b6-120">Mål-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-120">Destination IP address.</span></span>

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

### <span data-ttu-id="0d7b6-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="0d7b6-121">-Location</span></span>
<span data-ttu-id="0d7b6-122">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0d7b6-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7b6-123">-NetworkWatcher</span></span>
<span data-ttu-id="0d7b6-124">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="0d7b6-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0d7b6-125">-NetworkWatcherName</span></span>
<span data-ttu-id="0d7b6-126">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="0d7b6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d7b6-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d7b6-128">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0d7b6-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="0d7b6-129">-SourceIPAddress</span></span>
<span data-ttu-id="0d7b6-130">Käll-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-130">Source IP address.</span></span>

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

### <span data-ttu-id="0d7b6-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="0d7b6-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="0d7b6-132">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="0d7b6-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0d7b6-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0d7b6-134">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="0d7b6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7b6-135">CommonParameters</span></span>
<span data-ttu-id="0d7b6-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d7b6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7b6-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d7b6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7b6-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d7b6-138">INPUTS</span></span>

### <span data-ttu-id="0d7b6-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7b6-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0d7b6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0d7b6-140">System.String</span></span>

## <span data-ttu-id="0d7b6-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d7b6-141">OUTPUTS</span></span>

### <span data-ttu-id="0d7b6-142">Microsoft. Azure. commands. Networks. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="0d7b6-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="0d7b6-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d7b6-143">NOTES</span></span>
<span data-ttu-id="0d7b6-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="0d7b6-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="0d7b6-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d7b6-145">RELATED LINKS</span></span>

[<span data-ttu-id="0d7b6-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7b6-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0d7b6-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7b6-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0d7b6-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7b6-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0d7b6-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0d7b6-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0d7b6-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0d7b6-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0d7b6-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0d7b6-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0d7b6-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0d7b6-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0d7b6-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d7b6-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d7b6-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0d7b6-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0d7b6-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d7b6-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d7b6-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d7b6-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d7b6-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d7b6-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d7b6-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d7b6-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0d7b6-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0d7b6-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0d7b6-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0d7b6-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0d7b6-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d7b6-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d7b6-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d7b6-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d7b6-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d7b6-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d7b6-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0d7b6-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0d7b6-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d7b6-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d7b6-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d7b6-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d7b6-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0d7b6-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0d7b6-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0d7b6-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0d7b6-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0d7b6-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0d7b6-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0d7b6-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0d7b6-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0d7b6-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0d7b6-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d7b6-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)