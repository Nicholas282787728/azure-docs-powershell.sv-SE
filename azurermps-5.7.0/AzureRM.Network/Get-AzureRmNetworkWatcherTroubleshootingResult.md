---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: ef730b8ee6e6c35408b9d57d9dc23b0ab51a63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574919"
---
# <span data-ttu-id="a0023-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a0023-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="a0023-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0023-102">SYNOPSIS</span></span>
<span data-ttu-id="a0023-103">Hämtar fel söknings resultatet från den tidigare körningen eller fel söknings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a0023-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0023-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0023-104">SYNTAX</span></span>

### <span data-ttu-id="a0023-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="a0023-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0023-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a0023-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0023-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0023-107">DESCRIPTION</span></span>
<span data-ttu-id="a0023-108">Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet får fel söknings resultatet från den tidigare körningen eller Start-AzureRmNetworkWatcherResourceTroubleshooting åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a0023-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="a0023-109">Om det pågår en fel söknings åtgärd kan det ta några minuter att slutföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a0023-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="a0023-110">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="a0023-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="a0023-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0023-111">EXAMPLES</span></span>

### <span data-ttu-id="a0023-112">---Exempel 1: starta fel sökning på en virtuell nätverksgateway och hämta resultat---</span><span class="sxs-lookup"><span data-stu-id="a0023-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="a0023-113">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="a0023-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="a0023-114">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a0023-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="a0023-115">När fel sökningen har startat görs ett Get-AzureRmNetworkWatcherTroubleshootingResult-samtal till resursen för att hämta resultatet av samtalet.</span><span class="sxs-lookup"><span data-stu-id="a0023-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="a0023-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0023-116">PARAMETERS</span></span>

### <span data-ttu-id="a0023-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0023-117">-DefaultProfile</span></span>
<span data-ttu-id="a0023-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0023-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0023-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0023-119">-NetworkWatcher</span></span>
<span data-ttu-id="a0023-120">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="a0023-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="a0023-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a0023-121">-NetworkWatcherName</span></span>
<span data-ttu-id="a0023-122">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="a0023-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="a0023-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0023-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0023-124">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0023-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a0023-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a0023-125">-TargetResourceId</span></span>
<span data-ttu-id="a0023-126">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a0023-126">The target resource ID.</span></span>

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

### <span data-ttu-id="a0023-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0023-127">CommonParameters</span></span>
<span data-ttu-id="a0023-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0023-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0023-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0023-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0023-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0023-130">INPUTS</span></span>

### <span data-ttu-id="a0023-131">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0023-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a0023-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a0023-132">System.String</span></span>

## <span data-ttu-id="a0023-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0023-133">OUTPUTS</span></span>

### <span data-ttu-id="a0023-134">Microsoft. Azure. commands. Networks. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="a0023-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="a0023-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0023-135">NOTES</span></span>
<span data-ttu-id="a0023-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="a0023-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="a0023-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0023-137">RELATED LINKS</span></span>

[<span data-ttu-id="a0023-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a0023-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a0023-139">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0023-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a0023-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0023-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a0023-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0023-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a0023-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0023-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0023-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a0023-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a0023-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0023-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0023-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0023-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0023-146">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0023-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0023-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a0023-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a0023-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a0023-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a0023-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a0023-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a0023-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a0023-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
