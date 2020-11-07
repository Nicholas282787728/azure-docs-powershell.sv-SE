---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: f6c25d58588d0b75f67163c50cfa91a6f8e982da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924086"
---
# <span data-ttu-id="81dfb-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="81dfb-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="81dfb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="81dfb-103">Returnerar anslutnings information för en angiven källa för en virtuell dator och en destination.</span><span class="sxs-lookup"><span data-stu-id="81dfb-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="81dfb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81dfb-104">SYNTAX</span></span>

### <span data-ttu-id="81dfb-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="81dfb-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81dfb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="81dfb-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81dfb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81dfb-107">DESCRIPTION</span></span>
<span data-ttu-id="81dfb-108">Den Test-AzNetworkWatcherConnectivity cmdleten returnerar anslutnings information för en viss angiven källa och ett mål.</span><span class="sxs-lookup"><span data-stu-id="81dfb-108">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="81dfb-109">Om det inte går att upprätta anslutningen mellan källan och målet returnerar cmdleten information om problemet.</span><span class="sxs-lookup"><span data-stu-id="81dfb-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="81dfb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81dfb-110">EXAMPLES</span></span>

### <span data-ttu-id="81dfb-111">---------------Exempel 1: testa nätverks bevakning från en virtuell dator till en webbplats---------------</span><span class="sxs-lookup"><span data-stu-id="81dfb-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


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

<span data-ttu-id="81dfb-112">I det här exemplet testar vi anslutningen från en VM i Azure till www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="81dfb-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="81dfb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81dfb-113">PARAMETERS</span></span>

### <span data-ttu-id="81dfb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81dfb-114">-AsJob</span></span>
<span data-ttu-id="81dfb-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="81dfb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81dfb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81dfb-116">-DefaultProfile</span></span>
<span data-ttu-id="81dfb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81dfb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81dfb-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="81dfb-118">-DestinationAddress</span></span>
<span data-ttu-id="81dfb-119">Den IP-adress eller URI som resursen som ett anslutnings försök ska göras till.</span><span class="sxs-lookup"><span data-stu-id="81dfb-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="81dfb-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="81dfb-120">-DestinationId</span></span>
<span data-ttu-id="81dfb-121">ID för den resurs som ett anslutnings försök ska skapas från.</span><span class="sxs-lookup"><span data-stu-id="81dfb-121">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="81dfb-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="81dfb-122">-DestinationPort</span></span>
<span data-ttu-id="81dfb-123">Den port som kontroll anslutningen ska utföras på.</span><span class="sxs-lookup"><span data-stu-id="81dfb-123">Port on which check connectivity will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81dfb-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81dfb-124">-NetworkWatcher</span></span>
<span data-ttu-id="81dfb-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="81dfb-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="81dfb-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="81dfb-126">-NetworkWatcherName</span></span>
<span data-ttu-id="81dfb-127">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="81dfb-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81dfb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81dfb-128">-ResourceGroupName</span></span>
<span data-ttu-id="81dfb-129">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="81dfb-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="81dfb-130">-SourceId</span><span class="sxs-lookup"><span data-stu-id="81dfb-130">-SourceId</span></span>
<span data-ttu-id="81dfb-131">ID för resursen som en anslutnings kontroll kommer att startas från.</span><span class="sxs-lookup"><span data-stu-id="81dfb-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="81dfb-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="81dfb-132">-SourcePort</span></span>
<span data-ttu-id="81dfb-133">Käll porten från vilken en anslutnings kontroll utförs.</span><span class="sxs-lookup"><span data-stu-id="81dfb-133">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81dfb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81dfb-134">CommonParameters</span></span>
<span data-ttu-id="81dfb-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81dfb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81dfb-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81dfb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81dfb-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81dfb-137">INPUTS</span></span>

### <span data-ttu-id="81dfb-138">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="81dfb-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="81dfb-139">System. String system. Int32</span><span class="sxs-lookup"><span data-stu-id="81dfb-139">System.String System.Int32</span></span>

## <span data-ttu-id="81dfb-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81dfb-140">OUTPUTS</span></span>

### <span data-ttu-id="81dfb-141">Microsoft. Azure. commands. Networks. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="81dfb-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="81dfb-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81dfb-142">NOTES</span></span>
<span data-ttu-id="81dfb-143">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="81dfb-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="81dfb-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81dfb-144">RELATED LINKS</span></span>

<span data-ttu-id="81dfb-145">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="81dfb-145">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="81dfb-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="81dfb-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="81dfb-147">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="81dfb-147">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>
