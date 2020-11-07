---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922236"
---
# <span data-ttu-id="af32a-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="af32a-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="af32a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af32a-102">SYNOPSIS</span></span>
<span data-ttu-id="af32a-103">Hämtar fel söknings resultatet från den tidigare körningen eller fel söknings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="af32a-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="af32a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af32a-104">SYNTAX</span></span>

### <span data-ttu-id="af32a-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="af32a-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af32a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="af32a-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af32a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af32a-107">DESCRIPTION</span></span>
<span data-ttu-id="af32a-108">Get-AzNetworkWatcherTroubleshootingResult cmdlet får fel söknings resultatet från den tidigare körningen eller Start-AzNetworkWatcherResourceTroubleshooting åtgärden.</span><span class="sxs-lookup"><span data-stu-id="af32a-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="af32a-109">Om det pågår en fel söknings åtgärd kan det ta några minuter att slutföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="af32a-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="af32a-110">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="af32a-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="af32a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af32a-111">EXAMPLES</span></span>

### <span data-ttu-id="af32a-112">---Exempel 1: starta fel sökning på en virtuell nätverksgateway och hämta resultat---</span><span class="sxs-lookup"><span data-stu-id="af32a-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="af32a-113">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="af32a-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="af32a-114">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="af32a-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="af32a-115">När fel sökningen har startat görs ett Get-AzNetworkWatcherTroubleshootingResult-samtal till resursen för att hämta resultatet av samtalet.</span><span class="sxs-lookup"><span data-stu-id="af32a-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="af32a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af32a-116">PARAMETERS</span></span>

### <span data-ttu-id="af32a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af32a-117">-DefaultProfile</span></span>
<span data-ttu-id="af32a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af32a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af32a-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af32a-119">-NetworkWatcher</span></span>
<span data-ttu-id="af32a-120">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="af32a-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="af32a-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="af32a-121">-NetworkWatcherName</span></span>
<span data-ttu-id="af32a-122">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="af32a-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="af32a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af32a-123">-ResourceGroupName</span></span>
<span data-ttu-id="af32a-124">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="af32a-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="af32a-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="af32a-125">-TargetResourceId</span></span>
<span data-ttu-id="af32a-126">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="af32a-126">The target resource ID.</span></span>

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

### <span data-ttu-id="af32a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af32a-127">CommonParameters</span></span>
<span data-ttu-id="af32a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af32a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af32a-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af32a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af32a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af32a-130">INPUTS</span></span>

### <span data-ttu-id="af32a-131">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af32a-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="af32a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="af32a-132">System.String</span></span>

## <span data-ttu-id="af32a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af32a-133">OUTPUTS</span></span>

### <span data-ttu-id="af32a-134">Microsoft. Azure. commands. Networks. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="af32a-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="af32a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af32a-135">NOTES</span></span>
<span data-ttu-id="af32a-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="af32a-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="af32a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af32a-137">RELATED LINKS</span></span>

[<span data-ttu-id="af32a-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="af32a-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="af32a-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af32a-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="af32a-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af32a-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="af32a-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af32a-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="af32a-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af32a-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="af32a-143">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="af32a-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="af32a-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af32a-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="af32a-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af32a-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="af32a-146">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af32a-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="af32a-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="af32a-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="af32a-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="af32a-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="af32a-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="af32a-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="af32a-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="af32a-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
