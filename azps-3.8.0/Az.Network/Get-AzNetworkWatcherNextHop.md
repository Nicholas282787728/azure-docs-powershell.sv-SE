---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 7fe316bda1cc6385babad2b5a7cb03d44a6fc128
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926510"
---
# <span data-ttu-id="e2946-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e2946-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="e2946-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2946-102">SYNOPSIS</span></span>
<span data-ttu-id="e2946-103">Hämtar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e2946-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="e2946-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2946-104">SYNTAX</span></span>

### <span data-ttu-id="e2946-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="e2946-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2946-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e2946-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2946-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e2946-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2946-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2946-108">DESCRIPTION</span></span>
<span data-ttu-id="e2946-109">Get-AzNetworkWatcherNextHop cmdlet tar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e2946-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="e2946-110">Med nästa hopp kan du Visa typen av Azure-resurs, den associerade IP-adressen för den resursen och regeln för routningstabellen som är ansvarig för vägen.</span><span class="sxs-lookup"><span data-stu-id="e2946-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="e2946-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2946-111">EXAMPLES</span></span>

### <span data-ttu-id="e2946-112">Exempel 1: få nästa hopp när du kommunicerar med en Internet-IP</span><span class="sxs-lookup"><span data-stu-id="e2946-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="e2946-113">Hämtar nästa hopp för utgående kommunikation från det primära nätverks gränssnittet på den angivna virtuella datorn till 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="e2946-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="e2946-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2946-114">PARAMETERS</span></span>

### <span data-ttu-id="e2946-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2946-115">-AsJob</span></span>
<span data-ttu-id="e2946-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e2946-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2946-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2946-117">-DefaultProfile</span></span>
<span data-ttu-id="e2946-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2946-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2946-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="e2946-119">-DestinationIPAddress</span></span>
<span data-ttu-id="e2946-120">Mål-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="e2946-120">Destination IP address.</span></span>

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

### <span data-ttu-id="e2946-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="e2946-121">-Location</span></span>
<span data-ttu-id="e2946-122">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="e2946-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e2946-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2946-123">-NetworkWatcher</span></span>
<span data-ttu-id="e2946-124">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="e2946-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="e2946-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e2946-125">-NetworkWatcherName</span></span>
<span data-ttu-id="e2946-126">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="e2946-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="e2946-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2946-127">-ResourceGroupName</span></span>
<span data-ttu-id="e2946-128">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e2946-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e2946-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="e2946-129">-SourceIPAddress</span></span>
<span data-ttu-id="e2946-130">Käll-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="e2946-130">Source IP address.</span></span>

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

### <span data-ttu-id="e2946-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="e2946-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="e2946-132">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="e2946-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="e2946-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e2946-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="e2946-134">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="e2946-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="e2946-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2946-135">CommonParameters</span></span>
<span data-ttu-id="e2946-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2946-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2946-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2946-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2946-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2946-138">INPUTS</span></span>

### <span data-ttu-id="e2946-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2946-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e2946-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e2946-140">System.String</span></span>

## <span data-ttu-id="e2946-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2946-141">OUTPUTS</span></span>

### <span data-ttu-id="e2946-142">Microsoft. Azure. commands. Networks. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="e2946-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="e2946-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2946-143">NOTES</span></span>
<span data-ttu-id="e2946-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="e2946-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="e2946-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2946-145">RELATED LINKS</span></span>

[<span data-ttu-id="e2946-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2946-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e2946-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2946-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e2946-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2946-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e2946-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e2946-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e2946-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e2946-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e2946-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e2946-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e2946-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e2946-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e2946-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2946-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2946-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e2946-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e2946-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2946-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2946-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2946-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2946-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2946-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2946-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2946-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e2946-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e2946-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e2946-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e2946-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e2946-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2946-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2946-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2946-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2946-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2946-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2946-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e2946-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e2946-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2946-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2946-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2946-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2946-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e2946-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e2946-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e2946-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e2946-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e2946-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e2946-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e2946-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e2946-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e2946-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="e2946-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2946-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)