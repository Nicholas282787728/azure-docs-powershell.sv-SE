---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
ms.openlocfilehash: 36a584be829cd3d85d900c1e0b251dc7d49e95e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577126"
---
# <span data-ttu-id="56151-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="56151-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="56151-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56151-102">SYNOPSIS</span></span>
<span data-ttu-id="56151-103">Returnerar anslutnings information för en angiven källa för en virtuell dator och en destination.</span><span class="sxs-lookup"><span data-stu-id="56151-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56151-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56151-104">SYNTAX</span></span>

### <span data-ttu-id="56151-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="56151-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56151-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="56151-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56151-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56151-107">DESCRIPTION</span></span>
<span data-ttu-id="56151-108">Den Test-AzureRmNetworkWatcherConnectivity cmdleten returnerar anslutnings information för en viss angiven källa och ett mål.</span><span class="sxs-lookup"><span data-stu-id="56151-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="56151-109">Om det inte går att upprätta anslutningen mellan källan och målet returnerar cmdleten information om problemet.</span><span class="sxs-lookup"><span data-stu-id="56151-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="56151-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56151-110">EXAMPLES</span></span>

### <span data-ttu-id="56151-111">---------------Exempel 1: testa nätverks bevakning från en virtuell dator till en webbplats---------------</span><span class="sxs-lookup"><span data-stu-id="56151-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
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

<span data-ttu-id="56151-112">I det här exemplet testar vi anslutningen från en VM i Azure till www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="56151-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="56151-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56151-113">PARAMETERS</span></span>

### <span data-ttu-id="56151-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56151-114">-AsJob</span></span>
<span data-ttu-id="56151-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="56151-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56151-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56151-116">-DefaultProfile</span></span>
<span data-ttu-id="56151-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56151-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56151-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="56151-118">-DestinationAddress</span></span>
<span data-ttu-id="56151-119">Den IP-adress eller URI som resursen som ett anslutnings försök ska göras till.</span><span class="sxs-lookup"><span data-stu-id="56151-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="56151-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="56151-120">-DestinationId</span></span>
<span data-ttu-id="56151-121">ID för den resurs som ett anslutnings försök ska skapas från.</span><span class="sxs-lookup"><span data-stu-id="56151-121">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="56151-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="56151-122">-DestinationPort</span></span>
<span data-ttu-id="56151-123">Den port som kontroll anslutningen ska utföras på.</span><span class="sxs-lookup"><span data-stu-id="56151-123">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="56151-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56151-124">-NetworkWatcher</span></span>
<span data-ttu-id="56151-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="56151-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="56151-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="56151-126">-NetworkWatcherName</span></span>
<span data-ttu-id="56151-127">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="56151-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="56151-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56151-128">-ResourceGroupName</span></span>
<span data-ttu-id="56151-129">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="56151-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="56151-130">-SourceId</span><span class="sxs-lookup"><span data-stu-id="56151-130">-SourceId</span></span>
<span data-ttu-id="56151-131">ID för resursen som en anslutnings kontroll kommer att startas från.</span><span class="sxs-lookup"><span data-stu-id="56151-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="56151-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="56151-132">-SourcePort</span></span>
<span data-ttu-id="56151-133">Käll porten från vilken en anslutnings kontroll utförs.</span><span class="sxs-lookup"><span data-stu-id="56151-133">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="56151-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56151-134">CommonParameters</span></span>
<span data-ttu-id="56151-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56151-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56151-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56151-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56151-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56151-137">INPUTS</span></span>

### <span data-ttu-id="56151-138">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56151-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="56151-139">System. String system. Int32</span><span class="sxs-lookup"><span data-stu-id="56151-139">System.String System.Int32</span></span>

## <span data-ttu-id="56151-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56151-140">OUTPUTS</span></span>

### <span data-ttu-id="56151-141">Microsoft. Azure. commands. Networks. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="56151-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="56151-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56151-142">NOTES</span></span>
<span data-ttu-id="56151-143">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="56151-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="56151-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56151-144">RELATED LINKS</span></span>

<span data-ttu-id="56151-145">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="56151-145">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="56151-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="56151-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="56151-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="56151-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
