---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
ms.openlocfilehash: 6e851b8ac695a2c5fcfd9ef84571899492386124
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757837"
---
# <span data-ttu-id="44aa4-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="44aa4-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="44aa4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="44aa4-103">Returnerar anslutnings information för en angiven källa för en virtuell dator och en destination.</span><span class="sxs-lookup"><span data-stu-id="44aa4-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44aa4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44aa4-104">SYNTAX</span></span>

### <span data-ttu-id="44aa4-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="44aa4-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44aa4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="44aa4-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44aa4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="44aa4-107">SetByLocation</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44aa4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44aa4-108">DESCRIPTION</span></span>
<span data-ttu-id="44aa4-109">Den Test-AzureRmNetworkWatcherConnectivity cmdleten returnerar anslutnings information för en viss angiven källa och ett mål.</span><span class="sxs-lookup"><span data-stu-id="44aa4-109">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="44aa4-110">Om det inte går att upprätta anslutningen mellan källan och målet returnerar cmdleten information om problemet.</span><span class="sxs-lookup"><span data-stu-id="44aa4-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="44aa4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44aa4-111">EXAMPLES</span></span>

### <span data-ttu-id="44aa4-112">Exempel 1: testa nätverks Watchers anslutning från en virtuell dator till en webbplats</span><span class="sxs-lookup"><span data-stu-id="44aa4-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="44aa4-113">I det här exemplet testar vi anslutningen från en VM i Azure till www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="44aa4-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="44aa4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44aa4-114">PARAMETERS</span></span>

### <span data-ttu-id="44aa4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44aa4-115">-AsJob</span></span>
<span data-ttu-id="44aa4-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="44aa4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44aa4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44aa4-117">-DefaultProfile</span></span>
<span data-ttu-id="44aa4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44aa4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44aa4-119">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="44aa4-119">-DestinationAddress</span></span>
<span data-ttu-id="44aa4-120">Den IP-adress eller URI som resursen som ett anslutnings försök ska göras till.</span><span class="sxs-lookup"><span data-stu-id="44aa4-120">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="44aa4-121">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="44aa4-121">-DestinationId</span></span>
<span data-ttu-id="44aa4-122">ID för den resurs som ett anslutnings försök ska skapas från.</span><span class="sxs-lookup"><span data-stu-id="44aa4-122">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="44aa4-123">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="44aa4-123">-DestinationPort</span></span>
<span data-ttu-id="44aa4-124">Den port som kontroll anslutningen ska utföras på.</span><span class="sxs-lookup"><span data-stu-id="44aa4-124">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44aa4-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="44aa4-125">-Location</span></span>
<span data-ttu-id="44aa4-126">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="44aa4-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="44aa4-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44aa4-127">-NetworkWatcher</span></span>
<span data-ttu-id="44aa4-128">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="44aa4-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="44aa4-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="44aa4-129">-NetworkWatcherName</span></span>
<span data-ttu-id="44aa4-130">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="44aa4-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44aa4-131">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="44aa4-131">-ProtocolConfiguration</span></span>
<span data-ttu-id="44aa4-132">Protocal-konfiguration där kontrol lera anslutningen ska utföras.</span><span class="sxs-lookup"><span data-stu-id="44aa4-132">Protocal configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44aa4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44aa4-133">-ResourceGroupName</span></span>
<span data-ttu-id="44aa4-134">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="44aa4-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="44aa4-135">-SourceId</span><span class="sxs-lookup"><span data-stu-id="44aa4-135">-SourceId</span></span>
<span data-ttu-id="44aa4-136">ID för resursen som en anslutnings kontroll kommer att startas från.</span><span class="sxs-lookup"><span data-stu-id="44aa4-136">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="44aa4-137">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="44aa4-137">-SourcePort</span></span>
<span data-ttu-id="44aa4-138">Käll porten från vilken en anslutnings kontroll utförs.</span><span class="sxs-lookup"><span data-stu-id="44aa4-138">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44aa4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44aa4-139">CommonParameters</span></span>
<span data-ttu-id="44aa4-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44aa4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44aa4-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44aa4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44aa4-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44aa4-142">INPUTS</span></span>

### <span data-ttu-id="44aa4-143">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44aa4-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="44aa4-144">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="44aa4-144">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="44aa4-145">System. String</span><span class="sxs-lookup"><span data-stu-id="44aa4-145">System.String</span></span>

### <span data-ttu-id="44aa4-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="44aa4-146">System.Int32</span></span>

## <span data-ttu-id="44aa4-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44aa4-147">OUTPUTS</span></span>

### <span data-ttu-id="44aa4-148">Microsoft. Azure. commands. Networks. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="44aa4-148">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="44aa4-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44aa4-149">NOTES</span></span>
<span data-ttu-id="44aa4-150">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="44aa4-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="44aa4-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44aa4-151">RELATED LINKS</span></span>

<span data-ttu-id="44aa4-152">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="44aa4-152">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="44aa4-153">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="44aa4-153">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="44aa4-154">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="44aa4-154">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="44aa4-155">[Start-AzureRmNetworkWatcherResourceTroubleshooting](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md) 
 [New-AzureRmNetworkWatcherProtocolConfiguration](./New-AzureRmNetworkWatcherProtocolConfiguration.md) 
 [Test-AzureRmNetworkWatcherIPFlow](./Test-AzureRmNetworkWatcherIPFlow.md) 
 [Test-AzureRmNetworkWatcherConnectivity](./Test-AzureRmNetworkWatcherConnectivity.md) 
 [Stopp-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConfigFlowLog](./Set-AzureRmNetworkWatcherConfigFlowLog.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRMNetworkWatcherReachabilityReport](./Get-AzureRMNetworkWatcherReachabilityReport.md) 
 [Get-AzureRmNetworkWatcherReachabilityProvidersList](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzureRmNetworkWatcherFlowLogStatus](./Get-AzureRmNetworkWatcherFlowLogStatus.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="44aa4-155">[Start-AzureRmNetworkWatcherResourceTroubleshooting](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
[New-AzureRmNetworkWatcherProtocolConfiguration](./New-AzureRmNetworkWatcherProtocolConfiguration.md)
[Test-AzureRmNetworkWatcherIPFlow](./Test-AzureRmNetworkWatcherIPFlow.md)
[Test-AzureRmNetworkWatcherConnectivity](./Test-AzureRmNetworkWatcherConnectivity.md)
[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConfigFlowLog](./Set-AzureRmNetworkWatcherConfigFlowLog.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRMNetworkWatcherReachabilityReport](./Get-AzureRMNetworkWatcherReachabilityReport.md)
[Get-AzureRmNetworkWatcherReachabilityProvidersList](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)
[Get-AzureRmNetworkWatcherFlowLogStatus](./Get-AzureRmNetworkWatcherFlowLogStatus.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor)</span></span>
