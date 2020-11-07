---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 577f883affc772c01343a57a533c5ae06eccf31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757645"
---
# <span data-ttu-id="caa80-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="caa80-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="caa80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="caa80-102">SYNOPSIS</span></span>
<span data-ttu-id="caa80-103">Returnerar om paketet är tillåtet eller nekat till eller från ett visst mål.</span><span class="sxs-lookup"><span data-stu-id="caa80-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caa80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="caa80-104">SYNTAX</span></span>

### <span data-ttu-id="caa80-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="caa80-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caa80-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="caa80-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caa80-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="caa80-107">DESCRIPTION</span></span>
<span data-ttu-id="caa80-108">Test-AzureRmNetworkWatcherIPFlow cmdlet för en viss VM-resurs och ett paket med angiven riktning med lokala och fjärr-IP-adresser och portar, returnerar eller nekar paketet.</span><span class="sxs-lookup"><span data-stu-id="caa80-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="caa80-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="caa80-109">EXAMPLES</span></span>

### <span data-ttu-id="caa80-110">---Exempel 1: kör Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="caa80-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="caa80-111">Får nätverks tittaren i västra central för det här abonnemanget och hämtar sedan den virtuella datorn och dess associerade nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="caa80-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="caa80-112">För det första nätverks gränssnittet körs Test-AzureRmNetworkWatcherIPFlow med den första IP-adressen från det första nätverks gränssnittet för en utgående anslutning till en IP-adress på Internet.</span><span class="sxs-lookup"><span data-stu-id="caa80-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="caa80-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="caa80-113">PARAMETERS</span></span>

### <span data-ttu-id="caa80-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="caa80-114">-AsJob</span></span>
<span data-ttu-id="caa80-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="caa80-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="caa80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa80-116">-DefaultProfile</span></span>
<span data-ttu-id="caa80-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="caa80-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caa80-118">-Riktning</span><span class="sxs-lookup"><span data-stu-id="caa80-118">-Direction</span></span>
<span data-ttu-id="caa80-119">Piltangent.</span><span class="sxs-lookup"><span data-stu-id="caa80-119">Direction.</span></span>

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

### <span data-ttu-id="caa80-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="caa80-120">-LocalIPAddress</span></span>
<span data-ttu-id="caa80-121">Lokal IP-adress.</span><span class="sxs-lookup"><span data-stu-id="caa80-121">Local IP Address.</span></span>

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

### <span data-ttu-id="caa80-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="caa80-122">-LocalPort</span></span>
<span data-ttu-id="caa80-123">Lokal port.</span><span class="sxs-lookup"><span data-stu-id="caa80-123">Local Port.</span></span>

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

### <span data-ttu-id="caa80-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="caa80-124">-NetworkWatcher</span></span>
<span data-ttu-id="caa80-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="caa80-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="caa80-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="caa80-126">-NetworkWatcherName</span></span>
<span data-ttu-id="caa80-127">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="caa80-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="caa80-128">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="caa80-128">-Protocol</span></span>
<span data-ttu-id="caa80-129">Http.</span><span class="sxs-lookup"><span data-stu-id="caa80-129">Protocol.</span></span>

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

### <span data-ttu-id="caa80-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="caa80-130">-RemoteIPAddress</span></span>
<span data-ttu-id="caa80-131">Fjärr-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="caa80-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="caa80-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="caa80-132">-RemotePort</span></span>
<span data-ttu-id="caa80-133">Fjärrport.</span><span class="sxs-lookup"><span data-stu-id="caa80-133">Remote port.</span></span>

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

### <span data-ttu-id="caa80-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caa80-134">-ResourceGroupName</span></span>
<span data-ttu-id="caa80-135">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="caa80-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="caa80-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="caa80-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="caa80-137">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="caa80-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="caa80-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="caa80-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="caa80-139">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="caa80-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="caa80-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa80-140">CommonParameters</span></span>
<span data-ttu-id="caa80-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caa80-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa80-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa80-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa80-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="caa80-143">INPUTS</span></span>

### <span data-ttu-id="caa80-144">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="caa80-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="caa80-145">System. String</span><span class="sxs-lookup"><span data-stu-id="caa80-145">System.String</span></span>

## <span data-ttu-id="caa80-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="caa80-146">OUTPUTS</span></span>

### <span data-ttu-id="caa80-147">Microsoft. Azure. commands. Networks. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="caa80-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="caa80-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="caa80-148">NOTES</span></span>
<span data-ttu-id="caa80-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="caa80-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="caa80-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="caa80-150">RELATED LINKS</span></span>

[<span data-ttu-id="caa80-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="caa80-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="caa80-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="caa80-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="caa80-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="caa80-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="caa80-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="caa80-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="caa80-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="caa80-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="caa80-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="caa80-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="caa80-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="caa80-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="caa80-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="caa80-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="caa80-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="caa80-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="caa80-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="caa80-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="caa80-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="caa80-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="caa80-162">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="caa80-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
