---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
ms.openlocfilehash: a2caff32969ac771140bd8c6a5a3b142f4d61485
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929786"
---
# <span data-ttu-id="9fd27-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9fd27-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="9fd27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9fd27-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd27-103">Hämtar fel söknings resultatet från den tidigare körningen eller fel söknings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="9fd27-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fd27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9fd27-104">SYNTAX</span></span>

### <span data-ttu-id="9fd27-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="9fd27-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fd27-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9fd27-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fd27-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9fd27-107">DESCRIPTION</span></span>
<span data-ttu-id="9fd27-108">Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet får fel söknings resultatet från den tidigare körningen eller Start-AzureRmNetworkWatcherResourceTroubleshooting åtgärden.</span><span class="sxs-lookup"><span data-stu-id="9fd27-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="9fd27-109">Om det pågår en fel söknings åtgärd kan det ta några minuter att slutföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="9fd27-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="9fd27-110">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="9fd27-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="9fd27-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9fd27-111">EXAMPLES</span></span>

### <span data-ttu-id="9fd27-112">---Exempel 1: starta fel sökning på en virtuell nätverksgateway och hämta resultat---</span><span class="sxs-lookup"><span data-stu-id="9fd27-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="9fd27-113">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="9fd27-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="9fd27-114">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="9fd27-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="9fd27-115">När fel sökningen har startat görs ett Get-AzureRmNetworkWatcherTroubleshootingResult-samtal till resursen för att hämta resultatet av samtalet.</span><span class="sxs-lookup"><span data-stu-id="9fd27-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="9fd27-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9fd27-116">PARAMETERS</span></span>

### <span data-ttu-id="9fd27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd27-117">-DefaultProfile</span></span>
<span data-ttu-id="9fd27-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9fd27-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fd27-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9fd27-119">-NetworkWatcher</span></span>
<span data-ttu-id="9fd27-120">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="9fd27-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="9fd27-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9fd27-121">-NetworkWatcherName</span></span>
<span data-ttu-id="9fd27-122">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="9fd27-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="9fd27-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fd27-123">-ResourceGroupName</span></span>
<span data-ttu-id="9fd27-124">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9fd27-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9fd27-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9fd27-125">-TargetResourceId</span></span>
<span data-ttu-id="9fd27-126">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9fd27-126">The target resource ID.</span></span>

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

### <span data-ttu-id="9fd27-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd27-127">CommonParameters</span></span>
<span data-ttu-id="9fd27-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd27-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd27-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fd27-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd27-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9fd27-130">INPUTS</span></span>

### <span data-ttu-id="9fd27-131">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9fd27-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9fd27-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9fd27-132">System.String</span></span>

## <span data-ttu-id="9fd27-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9fd27-133">OUTPUTS</span></span>

### <span data-ttu-id="9fd27-134">Microsoft. Azure. commands. Networks. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="9fd27-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="9fd27-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9fd27-135">NOTES</span></span>
<span data-ttu-id="9fd27-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="9fd27-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="9fd27-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9fd27-137">RELATED LINKS</span></span>

[<span data-ttu-id="9fd27-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9fd27-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9fd27-139">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9fd27-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9fd27-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9fd27-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9fd27-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9fd27-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9fd27-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9fd27-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9fd27-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9fd27-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="9fd27-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9fd27-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9fd27-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9fd27-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9fd27-146">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9fd27-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9fd27-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9fd27-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="9fd27-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9fd27-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="9fd27-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9fd27-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9fd27-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9fd27-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
