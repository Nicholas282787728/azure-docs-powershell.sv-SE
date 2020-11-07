---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
ms.openlocfilehash: 41c76d78ad27ff889f2dc3e7be254bcc88668023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930986"
---
# <span data-ttu-id="44f16-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="44f16-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="44f16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44f16-102">SYNOPSIS</span></span>
<span data-ttu-id="44f16-103">Hämtar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="44f16-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44f16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44f16-104">SYNTAX</span></span>

### <span data-ttu-id="44f16-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="44f16-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44f16-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="44f16-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44f16-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44f16-107">DESCRIPTION</span></span>
<span data-ttu-id="44f16-108">Get-AzureRmNetworkWatcherNextHop cmdlet tar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="44f16-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="44f16-109">Med nästa hopp kan du Visa typen av Azure-resurs, den associerade IP-adressen för den resursen och regeln för routningstabellen som är ansvarig för vägen.</span><span class="sxs-lookup"><span data-stu-id="44f16-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="44f16-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44f16-110">EXAMPLES</span></span>

### <span data-ttu-id="44f16-111">--Exempel 1: få nästa hopp när du kommunicerar med en Internet-IP--</span><span class="sxs-lookup"><span data-stu-id="44f16-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="44f16-112">Får nästa hopp för utgående kommunikation från det primära nätverks gränssnittet på den angivna virtuella Vachine till 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="44f16-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="44f16-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44f16-113">PARAMETERS</span></span>

### <span data-ttu-id="44f16-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44f16-114">-AsJob</span></span>
<span data-ttu-id="44f16-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="44f16-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44f16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f16-116">-DefaultProfile</span></span>
<span data-ttu-id="44f16-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44f16-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44f16-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="44f16-118">-DestinationIPAddress</span></span>
<span data-ttu-id="44f16-119">Mål-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="44f16-119">Destination IP address.</span></span>

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

### <span data-ttu-id="44f16-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44f16-120">-NetworkWatcher</span></span>
<span data-ttu-id="44f16-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="44f16-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="44f16-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="44f16-122">-NetworkWatcherName</span></span>
<span data-ttu-id="44f16-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="44f16-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="44f16-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f16-124">-ResourceGroupName</span></span>
<span data-ttu-id="44f16-125">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="44f16-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="44f16-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="44f16-126">-SourceIPAddress</span></span>
<span data-ttu-id="44f16-127">Käll-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="44f16-127">Source IP address.</span></span>

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

### <span data-ttu-id="44f16-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="44f16-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="44f16-129">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="44f16-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="44f16-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="44f16-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="44f16-131">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="44f16-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="44f16-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f16-132">CommonParameters</span></span>
<span data-ttu-id="44f16-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f16-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f16-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44f16-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f16-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44f16-135">INPUTS</span></span>

### <span data-ttu-id="44f16-136">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44f16-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="44f16-137">System. String</span><span class="sxs-lookup"><span data-stu-id="44f16-137">System.String</span></span>

## <span data-ttu-id="44f16-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44f16-138">OUTPUTS</span></span>

### <span data-ttu-id="44f16-139">Microsoft. Azure. commands. Networks. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="44f16-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="44f16-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44f16-140">NOTES</span></span>
<span data-ttu-id="44f16-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="44f16-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="44f16-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44f16-142">RELATED LINKS</span></span>

[<span data-ttu-id="44f16-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44f16-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="44f16-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44f16-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="44f16-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44f16-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="44f16-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="44f16-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="44f16-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="44f16-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="44f16-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="44f16-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="44f16-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="44f16-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="44f16-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44f16-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44f16-151">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="44f16-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="44f16-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44f16-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44f16-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44f16-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44f16-154">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44f16-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

