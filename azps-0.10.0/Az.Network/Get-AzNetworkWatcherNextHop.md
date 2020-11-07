---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922242"
---
# <span data-ttu-id="a2ae4-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a2ae4-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="a2ae4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ae4-103">Hämtar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="a2ae4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2ae4-104">SYNTAX</span></span>

### <span data-ttu-id="a2ae4-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="a2ae4-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2ae4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a2ae4-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2ae4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2ae4-107">DESCRIPTION</span></span>
<span data-ttu-id="a2ae4-108">Get-AzNetworkWatcherNextHop cmdlet tar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="a2ae4-109">Med nästa hopp kan du Visa typen av Azure-resurs, den associerade IP-adressen för den resursen och regeln för routningstabellen som är ansvarig för vägen.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="a2ae4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2ae4-110">EXAMPLES</span></span>

### <span data-ttu-id="a2ae4-111">--Exempel 1: få nästa hopp när du kommunicerar med en Internet-IP--</span><span class="sxs-lookup"><span data-stu-id="a2ae4-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="a2ae4-112">Får nästa hopp för utgående kommunikation från det primära nätverks gränssnittet på den angivna virtuella Vachine till 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="a2ae4-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="a2ae4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2ae4-113">PARAMETERS</span></span>

### <span data-ttu-id="a2ae4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2ae4-114">-AsJob</span></span>
<span data-ttu-id="a2ae4-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a2ae4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2ae4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ae4-116">-DefaultProfile</span></span>
<span data-ttu-id="a2ae4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2ae4-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="a2ae4-118">-DestinationIPAddress</span></span>
<span data-ttu-id="a2ae4-119">Mål-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-119">Destination IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ae4-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2ae4-120">-NetworkWatcher</span></span>
<span data-ttu-id="a2ae4-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="a2ae4-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a2ae4-122">-NetworkWatcherName</span></span>
<span data-ttu-id="a2ae4-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="a2ae4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ae4-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2ae4-125">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a2ae4-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="a2ae4-126">-SourceIPAddress</span></span>
<span data-ttu-id="a2ae4-127">Käll-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-127">Source IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ae4-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="a2ae4-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="a2ae4-129">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="a2ae4-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a2ae4-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="a2ae4-131">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="a2ae4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ae4-132">CommonParameters</span></span>
<span data-ttu-id="a2ae4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ae4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ae4-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ae4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ae4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2ae4-135">INPUTS</span></span>

### <span data-ttu-id="a2ae4-136">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2ae4-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a2ae4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a2ae4-137">System.String</span></span>

## <span data-ttu-id="a2ae4-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2ae4-138">OUTPUTS</span></span>

### <span data-ttu-id="a2ae4-139">Microsoft. Azure. commands. Networks. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="a2ae4-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="a2ae4-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2ae4-140">NOTES</span></span>
<span data-ttu-id="a2ae4-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="a2ae4-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="a2ae4-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2ae4-142">RELATED LINKS</span></span>

[<span data-ttu-id="a2ae4-143">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2ae4-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a2ae4-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2ae4-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a2ae4-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2ae4-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a2ae4-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a2ae4-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a2ae4-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a2ae4-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a2ae4-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a2ae4-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a2ae4-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a2ae4-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a2ae4-150">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2ae4-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2ae4-151">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a2ae4-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a2ae4-152">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2ae4-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2ae4-153">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2ae4-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2ae4-154">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2ae4-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

