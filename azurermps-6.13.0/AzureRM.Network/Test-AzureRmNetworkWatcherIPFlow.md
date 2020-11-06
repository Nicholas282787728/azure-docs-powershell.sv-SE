---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6fc406d0af3ed451fbbf2f14c9ca8943256df744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585868"
---
# <span data-ttu-id="69907-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="69907-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="69907-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69907-102">SYNOPSIS</span></span>
<span data-ttu-id="69907-103">Returnerar om paketet är tillåtet eller nekat till eller från ett visst mål.</span><span class="sxs-lookup"><span data-stu-id="69907-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69907-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69907-104">SYNTAX</span></span>

### <span data-ttu-id="69907-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="69907-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69907-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="69907-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69907-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="69907-107">SetByLocation</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69907-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69907-108">DESCRIPTION</span></span>
<span data-ttu-id="69907-109">Test-AzureRmNetworkWatcherIPFlow cmdlet för en viss VM-resurs och ett paket med angiven riktning med lokala och fjärr-IP-adresser och portar, returnerar eller nekar paketet.</span><span class="sxs-lookup"><span data-stu-id="69907-109">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="69907-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69907-110">EXAMPLES</span></span>

### <span data-ttu-id="69907-111">Exempel 1: kör Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="69907-111">Example 1: Run Test-AzureRmNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="69907-112">Får nätverks tittaren i västra central för det här abonnemanget och hämtar sedan den virtuella datorn och dess associerade nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="69907-112">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="69907-113">För det första nätverks gränssnittet körs Test-AzureRmNetworkWatcherIPFlow med den första IP-adressen från det första nätverks gränssnittet för en utgående anslutning till en IP-adress på Internet.</span><span class="sxs-lookup"><span data-stu-id="69907-113">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="69907-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69907-114">PARAMETERS</span></span>

### <span data-ttu-id="69907-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69907-115">-AsJob</span></span>
<span data-ttu-id="69907-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="69907-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69907-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69907-117">-DefaultProfile</span></span>
<span data-ttu-id="69907-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69907-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69907-119">-Riktning</span><span class="sxs-lookup"><span data-stu-id="69907-119">-Direction</span></span>
<span data-ttu-id="69907-120">Piltangent.</span><span class="sxs-lookup"><span data-stu-id="69907-120">Direction.</span></span>

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

### <span data-ttu-id="69907-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="69907-121">-LocalIPAddress</span></span>
<span data-ttu-id="69907-122">Lokal IP-adress.</span><span class="sxs-lookup"><span data-stu-id="69907-122">Local IP Address.</span></span>

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

### <span data-ttu-id="69907-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="69907-123">-LocalPort</span></span>
<span data-ttu-id="69907-124">Lokal port.</span><span class="sxs-lookup"><span data-stu-id="69907-124">Local Port.</span></span>

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

### <span data-ttu-id="69907-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="69907-125">-Location</span></span>
<span data-ttu-id="69907-126">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="69907-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="69907-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69907-127">-NetworkWatcher</span></span>
<span data-ttu-id="69907-128">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="69907-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="69907-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="69907-129">-NetworkWatcherName</span></span>
<span data-ttu-id="69907-130">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="69907-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="69907-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="69907-131">-Protocol</span></span>
<span data-ttu-id="69907-132">Http.</span><span class="sxs-lookup"><span data-stu-id="69907-132">Protocol.</span></span>

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

### <span data-ttu-id="69907-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="69907-133">-RemoteIPAddress</span></span>
<span data-ttu-id="69907-134">Fjärr-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="69907-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="69907-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="69907-135">-RemotePort</span></span>
<span data-ttu-id="69907-136">Fjärrport.</span><span class="sxs-lookup"><span data-stu-id="69907-136">Remote port.</span></span>

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

### <span data-ttu-id="69907-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69907-137">-ResourceGroupName</span></span>
<span data-ttu-id="69907-138">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="69907-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="69907-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="69907-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="69907-140">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="69907-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="69907-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="69907-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="69907-142">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="69907-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="69907-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69907-143">CommonParameters</span></span>
<span data-ttu-id="69907-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69907-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69907-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69907-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69907-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69907-146">INPUTS</span></span>

### <span data-ttu-id="69907-147">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69907-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="69907-148">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="69907-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="69907-149">System. String</span><span class="sxs-lookup"><span data-stu-id="69907-149">System.String</span></span>
<span data-ttu-id="69907-150">Parametrar: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="69907-150">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="69907-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69907-151">OUTPUTS</span></span>

### <span data-ttu-id="69907-152">Microsoft. Azure. commands. Networks. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="69907-152">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="69907-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69907-153">NOTES</span></span>
<span data-ttu-id="69907-154">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="69907-154">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="69907-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69907-155">RELATED LINKS</span></span>

[<span data-ttu-id="69907-156">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69907-156">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="69907-157">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69907-157">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="69907-158">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69907-158">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="69907-159">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="69907-159">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="69907-160">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="69907-160">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="69907-161">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="69907-161">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="69907-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="69907-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="69907-163">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69907-163">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69907-164">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="69907-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="69907-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69907-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69907-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69907-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69907-167">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69907-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69907-168">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="69907-168">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="69907-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="69907-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="69907-170">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="69907-170">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="69907-171">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69907-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69907-172">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69907-172">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69907-173">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69907-173">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69907-174">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="69907-174">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="69907-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69907-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69907-176">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69907-176">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69907-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="69907-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="69907-178">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="69907-178">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="69907-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="69907-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="69907-180">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="69907-180">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="69907-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="69907-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="69907-182">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69907-182">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
