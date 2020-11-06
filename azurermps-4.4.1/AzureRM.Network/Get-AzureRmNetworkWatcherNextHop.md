---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: d26f50768c561e05b4dc27ad829c063b73c5a336
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585423"
---
# <span data-ttu-id="c4b8f-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c4b8f-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="c4b8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b8f-103">Hämtar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4b8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4b8f-104">SYNTAX</span></span>

### <span data-ttu-id="c4b8f-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="c4b8f-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4b8f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c4b8f-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4b8f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4b8f-107">DESCRIPTION</span></span>
<span data-ttu-id="c4b8f-108">Get-AzureRmNetworkWatcherNextHop cmdlet tar nästa hopp från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="c4b8f-109">Med nästa hopp kan du Visa typen av Azure-resurs, den associerade IP-adressen för den resursen och regeln för routningstabellen som är ansvarig för vägen.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="c4b8f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4b8f-110">EXAMPLES</span></span>

### <span data-ttu-id="c4b8f-111">--Exempel 1: få nästa hopp när du kommunicerar med en Internet-IP--</span><span class="sxs-lookup"><span data-stu-id="c4b8f-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="c4b8f-112">Får nästa hopp för utgående kommunikation från det primära nätverks gränssnittet på den angivna virtuella Vachine till 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="c4b8f-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="c4b8f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4b8f-113">PARAMETERS</span></span>

### <span data-ttu-id="c4b8f-114">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4b8f-114">-DestinationIPAddress</span></span>
<span data-ttu-id="c4b8f-115">Mål-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-115">Destination IP address.</span></span>

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

### <span data-ttu-id="c4b8f-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c4b8f-116">-NetworkWatcher</span></span>
<span data-ttu-id="c4b8f-117">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="c4b8f-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c4b8f-118">-NetworkWatcherName</span></span>
<span data-ttu-id="c4b8f-119">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="c4b8f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b8f-120">-ResourceGroupName</span></span>
<span data-ttu-id="c4b8f-121">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c4b8f-122">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4b8f-122">-SourceIPAddress</span></span>
<span data-ttu-id="c4b8f-123">Käll-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-123">Source IP address.</span></span>

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

### <span data-ttu-id="c4b8f-124">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="c4b8f-124">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="c4b8f-125">Mål nätverks gränssnittets ID.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-125">Target network interface Id.</span></span>

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

### <span data-ttu-id="c4b8f-126">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c4b8f-126">-TargetVirtualMachineId</span></span>
<span data-ttu-id="c4b8f-127">Mål datorns ID.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-127">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="c4b8f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b8f-128">-DefaultProfile</span></span>
<span data-ttu-id="c4b8f-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4b8f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b8f-130">CommonParameters</span></span>
<span data-ttu-id="c4b8f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b8f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b8f-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b8f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b8f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4b8f-133">INPUTS</span></span>

### <span data-ttu-id="c4b8f-134">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c4b8f-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c4b8f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c4b8f-135">System.String</span></span>

## <span data-ttu-id="c4b8f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4b8f-136">OUTPUTS</span></span>

### <span data-ttu-id="c4b8f-137">Microsoft. Azure. commands. Networks. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="c4b8f-137">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="c4b8f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4b8f-138">NOTES</span></span>
<span data-ttu-id="c4b8f-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="c4b8f-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="c4b8f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4b8f-140">RELATED LINKS</span></span>

[<span data-ttu-id="c4b8f-141">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c4b8f-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c4b8f-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c4b8f-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c4b8f-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c4b8f-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c4b8f-144">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c4b8f-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c4b8f-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c4b8f-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c4b8f-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c4b8f-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c4b8f-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c4b8f-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c4b8f-148">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c4b8f-148">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c4b8f-149">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c4b8f-149">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c4b8f-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c4b8f-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c4b8f-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c4b8f-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c4b8f-152">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c4b8f-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

