---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924089"
---
# <span data-ttu-id="0eb8e-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0eb8e-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="0eb8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0eb8e-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb8e-103">Returnerar om paketet är tillåtet eller nekat till eller från ett visst mål.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="0eb8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0eb8e-104">SYNTAX</span></span>

### <span data-ttu-id="0eb8e-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="0eb8e-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eb8e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0eb8e-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eb8e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0eb8e-107">DESCRIPTION</span></span>
<span data-ttu-id="0eb8e-108">Test-AzNetworkWatcherIPFlow cmdlet för en viss VM-resurs och ett paket med angiven riktning med lokala och fjärr-IP-adresser och portar, returnerar eller nekar paketet.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="0eb8e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0eb8e-109">EXAMPLES</span></span>

### <span data-ttu-id="0eb8e-110">---Exempel 1: kör Test-AzNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="0eb8e-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="0eb8e-111">Får nätverks tittaren i västra central för det här abonnemanget och hämtar sedan den virtuella datorn och dess associerade nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="0eb8e-112">För det första nätverks gränssnittet körs Test-AzNetworkWatcherIPFlow med den första IP-adressen från det första nätverks gränssnittet för en utgående anslutning till en IP-adress på Internet.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="0eb8e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0eb8e-113">PARAMETERS</span></span>

### <span data-ttu-id="0eb8e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0eb8e-114">-AsJob</span></span>
<span data-ttu-id="0eb8e-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0eb8e-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb8e-116">-DefaultProfile</span></span>
<span data-ttu-id="0eb8e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-118">-Riktning</span><span class="sxs-lookup"><span data-stu-id="0eb8e-118">-Direction</span></span>
<span data-ttu-id="0eb8e-119">Piltangent.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="0eb8e-120">-LocalIPAddress</span></span>
<span data-ttu-id="0eb8e-121">Lokal IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-121">Local IP Address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="0eb8e-122">-LocalPort</span></span>
<span data-ttu-id="0eb8e-123">Lokal port.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-123">Local Port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0eb8e-124">-NetworkWatcher</span></span>
<span data-ttu-id="0eb8e-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0eb8e-126">-NetworkWatcherName</span></span>
<span data-ttu-id="0eb8e-127">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-128">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0eb8e-128">-Protocol</span></span>
<span data-ttu-id="0eb8e-129">Http.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="0eb8e-130">-RemoteIPAddress</span></span>
<span data-ttu-id="0eb8e-131">Fjärr-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-131">Remote IP Address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="0eb8e-132">-RemotePort</span></span>
<span data-ttu-id="0eb8e-133">Fjärrport.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-133">Remote port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb8e-134">-ResourceGroupName</span></span>
<span data-ttu-id="0eb8e-135">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="0eb8e-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="0eb8e-137">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-137">Target network interface Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0eb8e-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0eb8e-139">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-139">The target virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb8e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb8e-140">CommonParameters</span></span>
<span data-ttu-id="0eb8e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb8e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb8e-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eb8e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb8e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0eb8e-143">INPUTS</span></span>

### <span data-ttu-id="0eb8e-144">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0eb8e-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0eb8e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0eb8e-145">System.String</span></span>

## <span data-ttu-id="0eb8e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0eb8e-146">OUTPUTS</span></span>

### <span data-ttu-id="0eb8e-147">Microsoft. Azure. commands. Networks. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="0eb8e-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="0eb8e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0eb8e-148">NOTES</span></span>
<span data-ttu-id="0eb8e-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="0eb8e-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="0eb8e-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0eb8e-150">RELATED LINKS</span></span>

[<span data-ttu-id="0eb8e-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0eb8e-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0eb8e-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0eb8e-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0eb8e-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0eb8e-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0eb8e-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0eb8e-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0eb8e-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0eb8e-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0eb8e-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0eb8e-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0eb8e-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0eb8e-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0eb8e-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0eb8e-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0eb8e-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0eb8e-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0eb8e-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0eb8e-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0eb8e-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0eb8e-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0eb8e-162">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0eb8e-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
