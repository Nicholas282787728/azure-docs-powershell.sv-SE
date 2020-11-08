---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: e20c0087c44ee7dbf29d65733712eb28022da1b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090383"
---
# <span data-ttu-id="756ff-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="756ff-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="756ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="756ff-102">SYNOPSIS</span></span>
<span data-ttu-id="756ff-103">Returnerar om paketet är tillåtet eller nekat till eller från ett visst mål.</span><span class="sxs-lookup"><span data-stu-id="756ff-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="756ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="756ff-104">SYNTAX</span></span>

### <span data-ttu-id="756ff-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="756ff-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="756ff-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="756ff-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="756ff-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="756ff-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="756ff-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="756ff-108">DESCRIPTION</span></span>
<span data-ttu-id="756ff-109">Test-AzNetworkWatcherIPFlow cmdlet för en viss VM-resurs och ett paket med angiven riktning med lokala och fjärr-IP-adresser och portar, returnerar eller nekar paketet.</span><span class="sxs-lookup"><span data-stu-id="756ff-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="756ff-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="756ff-110">EXAMPLES</span></span>

### <span data-ttu-id="756ff-111">Exempel 1: kör Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="756ff-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="756ff-112">Hämtar nätverks bevakningen i västra centrala USA för det här abonnemanget och hämtar sedan den virtuella datorn och dess associerade nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="756ff-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="756ff-113">För det första nätverks gränssnittet körs Test-AzNetworkWatcherIPFlow med den första IP-adressen från det första nätverks gränssnittet för en utgående anslutning till en IP-adress på Internet.</span><span class="sxs-lookup"><span data-stu-id="756ff-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="756ff-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="756ff-114">PARAMETERS</span></span>

### <span data-ttu-id="756ff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="756ff-115">-AsJob</span></span>
<span data-ttu-id="756ff-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="756ff-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="756ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756ff-117">-DefaultProfile</span></span>
<span data-ttu-id="756ff-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="756ff-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="756ff-119">-Riktning</span><span class="sxs-lookup"><span data-stu-id="756ff-119">-Direction</span></span>
<span data-ttu-id="756ff-120">Piltangent.</span><span class="sxs-lookup"><span data-stu-id="756ff-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756ff-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="756ff-121">-LocalIPAddress</span></span>
<span data-ttu-id="756ff-122">Lokal IP-adress.</span><span class="sxs-lookup"><span data-stu-id="756ff-122">Local IP Address.</span></span>

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

### <span data-ttu-id="756ff-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="756ff-123">-LocalPort</span></span>
<span data-ttu-id="756ff-124">Lokal port.</span><span class="sxs-lookup"><span data-stu-id="756ff-124">Local Port.</span></span>

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

### <span data-ttu-id="756ff-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="756ff-125">-Location</span></span>
<span data-ttu-id="756ff-126">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="756ff-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="756ff-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="756ff-127">-NetworkWatcher</span></span>
<span data-ttu-id="756ff-128">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="756ff-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="756ff-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="756ff-129">-NetworkWatcherName</span></span>
<span data-ttu-id="756ff-130">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="756ff-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="756ff-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="756ff-131">-Protocol</span></span>
<span data-ttu-id="756ff-132">Http.</span><span class="sxs-lookup"><span data-stu-id="756ff-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756ff-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="756ff-133">-RemoteIPAddress</span></span>
<span data-ttu-id="756ff-134">Fjärr-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="756ff-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="756ff-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="756ff-135">-RemotePort</span></span>
<span data-ttu-id="756ff-136">Fjärrport.</span><span class="sxs-lookup"><span data-stu-id="756ff-136">Remote port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="756ff-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="756ff-137">-ResourceGroupName</span></span>
<span data-ttu-id="756ff-138">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="756ff-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="756ff-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="756ff-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="756ff-140">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="756ff-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="756ff-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="756ff-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="756ff-142">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="756ff-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="756ff-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756ff-143">CommonParameters</span></span>
<span data-ttu-id="756ff-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="756ff-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756ff-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="756ff-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756ff-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="756ff-146">INPUTS</span></span>

### <span data-ttu-id="756ff-147">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="756ff-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="756ff-148">System. String</span><span class="sxs-lookup"><span data-stu-id="756ff-148">System.String</span></span>

## <span data-ttu-id="756ff-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="756ff-149">OUTPUTS</span></span>

### <span data-ttu-id="756ff-150">Microsoft. Azure. commands. Networks. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="756ff-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="756ff-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="756ff-151">NOTES</span></span>
<span data-ttu-id="756ff-152">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="756ff-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="756ff-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="756ff-153">RELATED LINKS</span></span>

[<span data-ttu-id="756ff-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="756ff-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="756ff-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="756ff-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="756ff-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="756ff-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="756ff-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="756ff-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="756ff-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="756ff-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="756ff-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="756ff-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="756ff-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="756ff-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="756ff-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="756ff-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="756ff-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="756ff-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="756ff-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="756ff-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="756ff-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="756ff-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="756ff-165">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="756ff-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="756ff-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="756ff-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="756ff-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="756ff-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="756ff-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="756ff-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="756ff-169">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="756ff-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="756ff-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="756ff-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="756ff-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="756ff-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="756ff-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="756ff-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="756ff-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="756ff-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="756ff-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="756ff-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="756ff-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="756ff-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="756ff-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="756ff-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="756ff-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="756ff-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="756ff-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="756ff-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="756ff-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="756ff-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="756ff-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="756ff-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
