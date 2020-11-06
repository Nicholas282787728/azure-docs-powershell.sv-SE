---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 20d350bec1e344ed359a62f0026c490361140fcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576709"
---
# <span data-ttu-id="f499a-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f499a-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="f499a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f499a-102">SYNOPSIS</span></span>
<span data-ttu-id="f499a-103">Hämtar fel söknings resultatet från den tidigare körningen eller fel söknings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f499a-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f499a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f499a-104">SYNTAX</span></span>

### <span data-ttu-id="f499a-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="f499a-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f499a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f499a-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f499a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f499a-107">DESCRIPTION</span></span>
<span data-ttu-id="f499a-108">Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet får fel söknings resultatet från den tidigare körningen eller Start-AzureRmNetworkWatcherResourceTroubleshooting åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f499a-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="f499a-109">Om det pågår en fel söknings åtgärd kan det ta några minuter att slutföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f499a-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="f499a-110">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="f499a-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="f499a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f499a-111">EXAMPLES</span></span>

### <span data-ttu-id="f499a-112">---Exempel 1: starta fel sökning på en virtuell nätverksgateway och hämta resultat---</span><span class="sxs-lookup"><span data-stu-id="f499a-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="f499a-113">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="f499a-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="f499a-114">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f499a-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="f499a-115">När fel sökningen har startat görs ett Get-AzureRmNetworkWatcherTroubleshootingResult-samtal till resursen för att hämta resultatet av samtalet.</span><span class="sxs-lookup"><span data-stu-id="f499a-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="f499a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f499a-116">PARAMETERS</span></span>

### <span data-ttu-id="f499a-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f499a-117">-NetworkWatcher</span></span>
<span data-ttu-id="f499a-118">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="f499a-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="f499a-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f499a-119">-NetworkWatcherName</span></span>
<span data-ttu-id="f499a-120">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="f499a-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="f499a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f499a-121">-ResourceGroupName</span></span>
<span data-ttu-id="f499a-122">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f499a-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f499a-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f499a-123">-TargetResourceId</span></span>
<span data-ttu-id="f499a-124">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f499a-124">The target resource ID.</span></span>

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

### <span data-ttu-id="f499a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f499a-125">-DefaultProfile</span></span>
<span data-ttu-id="f499a-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f499a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f499a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f499a-127">CommonParameters</span></span>
<span data-ttu-id="f499a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f499a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f499a-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f499a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f499a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f499a-130">INPUTS</span></span>

### <span data-ttu-id="f499a-131">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f499a-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f499a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f499a-132">System.String</span></span>

## <span data-ttu-id="f499a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f499a-133">OUTPUTS</span></span>

### <span data-ttu-id="f499a-134">Microsoft. Azure. commands. Networks. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="f499a-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="f499a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f499a-135">NOTES</span></span>
<span data-ttu-id="f499a-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="f499a-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="f499a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f499a-137">RELATED LINKS</span></span>

[<span data-ttu-id="f499a-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f499a-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f499a-139">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f499a-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f499a-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f499a-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f499a-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f499a-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f499a-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f499a-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f499a-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f499a-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f499a-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f499a-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f499a-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f499a-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f499a-146">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f499a-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f499a-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f499a-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f499a-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f499a-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f499a-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f499a-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f499a-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f499a-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
