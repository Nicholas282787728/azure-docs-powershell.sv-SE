---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924106"
---
# <span data-ttu-id="65ab5-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="65ab5-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="65ab5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="65ab5-103">Startar fel sökning på en nätverks resurs i Azure.</span><span class="sxs-lookup"><span data-stu-id="65ab5-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="65ab5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65ab5-104">SYNTAX</span></span>

### <span data-ttu-id="65ab5-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="65ab5-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65ab5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="65ab5-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65ab5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65ab5-107">DESCRIPTION</span></span>
<span data-ttu-id="65ab5-108">Start-AzNetworkWatcherResourceTroubleshooting-cmdleten startar fel sökning för en nätverks resurs i Azure och returnerar information om potentiella problem och begränsningar.</span><span class="sxs-lookup"><span data-stu-id="65ab5-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="65ab5-109">För närvarande stöds virtuella nätverksgateway och anslutningar.</span><span class="sxs-lookup"><span data-stu-id="65ab5-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="65ab5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65ab5-110">EXAMPLES</span></span>

### <span data-ttu-id="65ab5-111">---Exempel 1: starta fel sökning på en virtuell nätverksgateway---</span><span class="sxs-lookup"><span data-stu-id="65ab5-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="65ab5-112">Exemplet ovan startar fel sökning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="65ab5-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="65ab5-113">Det kan ta några minuter att slutföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="65ab5-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="65ab5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65ab5-114">PARAMETERS</span></span>

### <span data-ttu-id="65ab5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ab5-115">-DefaultProfile</span></span>
<span data-ttu-id="65ab5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65ab5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65ab5-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65ab5-117">-NetworkWatcher</span></span>
<span data-ttu-id="65ab5-118">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="65ab5-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="65ab5-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="65ab5-119">-NetworkWatcherName</span></span>
<span data-ttu-id="65ab5-120">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="65ab5-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="65ab5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ab5-121">-ResourceGroupName</span></span>
<span data-ttu-id="65ab5-122">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="65ab5-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="65ab5-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="65ab5-123">-StorageId</span></span>
<span data-ttu-id="65ab5-124">Lagrings-ID.</span><span class="sxs-lookup"><span data-stu-id="65ab5-124">The storage ID.</span></span>

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

### <span data-ttu-id="65ab5-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="65ab5-125">-StoragePath</span></span>
<span data-ttu-id="65ab5-126">Lagrings Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="65ab5-126">The storage path.</span></span>

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

### <span data-ttu-id="65ab5-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="65ab5-127">-TargetResourceId</span></span>
<span data-ttu-id="65ab5-128">Anger resurs-ID för den resurs som ska felsökas.</span><span class="sxs-lookup"><span data-stu-id="65ab5-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="65ab5-129">Exempel format: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="65ab5-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="65ab5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ab5-130">CommonParameters</span></span>
<span data-ttu-id="65ab5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ab5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ab5-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ab5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ab5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65ab5-133">INPUTS</span></span>

### <span data-ttu-id="65ab5-134">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65ab5-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="65ab5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="65ab5-135">System.String</span></span>

## <span data-ttu-id="65ab5-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65ab5-136">OUTPUTS</span></span>

### <span data-ttu-id="65ab5-137">Microsoft. Azure. commands. Networks. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="65ab5-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="65ab5-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65ab5-138">NOTES</span></span>
<span data-ttu-id="65ab5-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, felsöka, VPN, anslutning</span><span class="sxs-lookup"><span data-stu-id="65ab5-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="65ab5-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65ab5-140">RELATED LINKS</span></span>

[<span data-ttu-id="65ab5-141">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="65ab5-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="65ab5-142">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65ab5-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="65ab5-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65ab5-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="65ab5-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65ab5-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="65ab5-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65ab5-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65ab5-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="65ab5-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="65ab5-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65ab5-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65ab5-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65ab5-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65ab5-149">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65ab5-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65ab5-150">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="65ab5-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="65ab5-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="65ab5-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="65ab5-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="65ab5-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="65ab5-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="65ab5-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
