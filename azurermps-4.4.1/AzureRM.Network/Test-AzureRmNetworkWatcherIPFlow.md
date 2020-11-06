---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6e9700f91a9d6f8db5983604a0146f9d864dafd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585487"
---
# <span data-ttu-id="7daac-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7daac-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="7daac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7daac-102">SYNOPSIS</span></span>
<span data-ttu-id="7daac-103">Returnerar om paketet är tillåtet eller nekat till eller från ett visst mål.</span><span class="sxs-lookup"><span data-stu-id="7daac-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7daac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7daac-104">SYNTAX</span></span>

### <span data-ttu-id="7daac-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="7daac-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7daac-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7daac-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7daac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7daac-107">DESCRIPTION</span></span>
<span data-ttu-id="7daac-108">Test-AzureRmNetworkWatcherIPFlow cmdlet för en viss VM-resurs och ett paket med angiven riktning med lokala och fjärr-IP-adresser och portar, returnerar eller nekar paketet.</span><span class="sxs-lookup"><span data-stu-id="7daac-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="7daac-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7daac-109">EXAMPLES</span></span>

### <span data-ttu-id="7daac-110">---Exempel 1: kör Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="7daac-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="7daac-111">Får nätverks tittaren i västra central för det här abonnemanget och hämtar sedan den virtuella datorn och dess associerade nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="7daac-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="7daac-112">För det första nätverks gränssnittet körs Test-AzureRmNetworkWatcherIPFlow med den första IP-adressen från det första nätverks gränssnittet för en utgående anslutning till en IP-adress på Internet.</span><span class="sxs-lookup"><span data-stu-id="7daac-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="7daac-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7daac-113">PARAMETERS</span></span>

### <span data-ttu-id="7daac-114">-Riktning</span><span class="sxs-lookup"><span data-stu-id="7daac-114">-Direction</span></span>
<span data-ttu-id="7daac-115">Piltangent.</span><span class="sxs-lookup"><span data-stu-id="7daac-115">Direction.</span></span>

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

### <span data-ttu-id="7daac-116">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="7daac-116">-LocalIPAddress</span></span>
<span data-ttu-id="7daac-117">Lokal IP-adress.</span><span class="sxs-lookup"><span data-stu-id="7daac-117">Local IP Address.</span></span>

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

### <span data-ttu-id="7daac-118">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="7daac-118">-LocalPort</span></span>
<span data-ttu-id="7daac-119">Lokal port.</span><span class="sxs-lookup"><span data-stu-id="7daac-119">Local Port.</span></span>

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

### <span data-ttu-id="7daac-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7daac-120">-NetworkWatcher</span></span>
<span data-ttu-id="7daac-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="7daac-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="7daac-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7daac-122">-NetworkWatcherName</span></span>
<span data-ttu-id="7daac-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="7daac-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="7daac-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7daac-124">-Protocol</span></span>
<span data-ttu-id="7daac-125">Http.</span><span class="sxs-lookup"><span data-stu-id="7daac-125">Protocol.</span></span>

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

### <span data-ttu-id="7daac-126">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="7daac-126">-RemoteIPAddress</span></span>
<span data-ttu-id="7daac-127">Fjärr-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="7daac-127">Remote IP Address.</span></span>

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

### <span data-ttu-id="7daac-128">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="7daac-128">-RemotePort</span></span>
<span data-ttu-id="7daac-129">Fjärrport.</span><span class="sxs-lookup"><span data-stu-id="7daac-129">Remote port.</span></span>

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

### <span data-ttu-id="7daac-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7daac-130">-ResourceGroupName</span></span>
<span data-ttu-id="7daac-131">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7daac-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7daac-132">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="7daac-132">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="7daac-133">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="7daac-133">Target network interface Id.</span></span>

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

### <span data-ttu-id="7daac-134">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="7daac-134">-TargetVirtualMachineId</span></span>
<span data-ttu-id="7daac-135">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="7daac-135">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="7daac-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7daac-136">-DefaultProfile</span></span>
<span data-ttu-id="7daac-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7daac-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7daac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7daac-138">CommonParameters</span></span>
<span data-ttu-id="7daac-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7daac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7daac-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7daac-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7daac-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7daac-141">INPUTS</span></span>

### <span data-ttu-id="7daac-142">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7daac-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7daac-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7daac-143">System.String</span></span>

## <span data-ttu-id="7daac-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7daac-144">OUTPUTS</span></span>

### <span data-ttu-id="7daac-145">Microsoft. Azure. commands. Networks. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="7daac-145">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="7daac-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7daac-146">NOTES</span></span>
<span data-ttu-id="7daac-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="7daac-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="7daac-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7daac-148">RELATED LINKS</span></span>

[<span data-ttu-id="7daac-149">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7daac-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7daac-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7daac-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7daac-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7daac-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7daac-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7daac-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7daac-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7daac-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7daac-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7daac-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7daac-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7daac-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7daac-156">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7daac-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7daac-157">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7daac-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7daac-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7daac-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7daac-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7daac-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7daac-160">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7daac-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
