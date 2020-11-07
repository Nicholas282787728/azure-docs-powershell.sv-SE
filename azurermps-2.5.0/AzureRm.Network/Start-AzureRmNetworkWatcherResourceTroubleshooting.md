---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
ms.openlocfilehash: 411b70fb6018b71b1c1c7fbf67816d0c86e6d3b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929270"
---
# <span data-ttu-id="c995d-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c995d-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="c995d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c995d-102">SYNOPSIS</span></span>
<span data-ttu-id="c995d-103">Startar fel sökning på en nätverks resurs i Azure.</span><span class="sxs-lookup"><span data-stu-id="c995d-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c995d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c995d-104">SYNTAX</span></span>

### <span data-ttu-id="c995d-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="c995d-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c995d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c995d-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c995d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c995d-107">DESCRIPTION</span></span>
<span data-ttu-id="c995d-108">Start-AzureRmNetworkWatcherResourceTroubleshooting-cmdleten startar fel sökning för en nätverks resurs i Azure och returnerar information om potentiella problem och begränsningar.</span><span class="sxs-lookup"><span data-stu-id="c995d-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="c995d-109">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="c995d-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="c995d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c995d-110">EXAMPLES</span></span>

### <span data-ttu-id="c995d-111">---Exempel 1: starta fel sökning på en virtuell nätverksgateway---</span><span class="sxs-lookup"><span data-stu-id="c995d-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="c995d-112">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="c995d-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="c995d-113">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c995d-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="c995d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c995d-114">PARAMETERS</span></span>

### <span data-ttu-id="c995d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c995d-115">-DefaultProfile</span></span>
<span data-ttu-id="c995d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c995d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c995d-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c995d-117">-NetworkWatcher</span></span>
<span data-ttu-id="c995d-118">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="c995d-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="c995d-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c995d-119">-NetworkWatcherName</span></span>
<span data-ttu-id="c995d-120">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="c995d-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="c995d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c995d-121">-ResourceGroupName</span></span>
<span data-ttu-id="c995d-122">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c995d-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c995d-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="c995d-123">-StorageId</span></span>
<span data-ttu-id="c995d-124">Lagrings-ID.</span><span class="sxs-lookup"><span data-stu-id="c995d-124">The storage ID.</span></span>

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

### <span data-ttu-id="c995d-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="c995d-125">-StoragePath</span></span>
<span data-ttu-id="c995d-126">Lagrings Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="c995d-126">The storage path.</span></span>

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

### <span data-ttu-id="c995d-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c995d-127">-TargetResourceId</span></span>
<span data-ttu-id="c995d-128">Anger resurs-ID för den resurs som ska felsökas.</span><span class="sxs-lookup"><span data-stu-id="c995d-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="c995d-129">Exempel format: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="c995d-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="c995d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c995d-130">CommonParameters</span></span>
<span data-ttu-id="c995d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c995d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c995d-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c995d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c995d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c995d-133">INPUTS</span></span>

### <span data-ttu-id="c995d-134">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c995d-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c995d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c995d-135">System.String</span></span>

## <span data-ttu-id="c995d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c995d-136">OUTPUTS</span></span>

### <span data-ttu-id="c995d-137">Microsoft. Azure. commands. Networks. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="c995d-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="c995d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c995d-138">NOTES</span></span>
<span data-ttu-id="c995d-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="c995d-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="c995d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c995d-140">RELATED LINKS</span></span>

[<span data-ttu-id="c995d-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c995d-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c995d-142">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c995d-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c995d-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c995d-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c995d-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c995d-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c995d-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c995d-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c995d-146">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c995d-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c995d-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c995d-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c995d-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c995d-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c995d-149">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c995d-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c995d-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c995d-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c995d-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c995d-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c995d-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c995d-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c995d-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c995d-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
