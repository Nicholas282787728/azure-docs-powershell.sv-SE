---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 1904e9df565a5f9e8d3738e723348ec96010f97a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578143"
---
# <span data-ttu-id="a2706-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a2706-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="a2706-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2706-102">SYNOPSIS</span></span>
<span data-ttu-id="a2706-103">Hämtar status för flödes loggning för en resurs.</span><span class="sxs-lookup"><span data-stu-id="a2706-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2706-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2706-104">SYNTAX</span></span>

### <span data-ttu-id="a2706-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="a2706-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2706-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a2706-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2706-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2706-107">DESCRIPTION</span></span>
<span data-ttu-id="a2706-108">Get-AzureRmNetworkWatcherFlowLogStatus cmdlet får statusen för flödes loggning för en resurs.</span><span class="sxs-lookup"><span data-stu-id="a2706-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="a2706-109">Statusen inkluderar om flödes loggning är aktiverat för den angivna resursen, det konfigurerade lagrings kontot för att skicka loggar och bevarande princip för loggarna.</span><span class="sxs-lookup"><span data-stu-id="a2706-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="a2706-110">För närvarande stöds nätverks säkerhets grupper för flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="a2706-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="a2706-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2706-111">EXAMPLES</span></span>

### <span data-ttu-id="a2706-112">---Exempel 1: Hämta loggnings status för flödet för ett angivet NSG---</span><span class="sxs-lookup"><span data-stu-id="a2706-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="a2706-113">I det här exemplet får du status för flödes loggning för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="a2706-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="a2706-114">Den angivna NSG har flödes loggning aktive rad och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="a2706-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="a2706-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2706-115">PARAMETERS</span></span>

### <span data-ttu-id="a2706-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2706-116">-AsJob</span></span>
<span data-ttu-id="a2706-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a2706-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2706-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2706-118">-DefaultProfile</span></span>
<span data-ttu-id="a2706-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2706-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2706-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2706-120">-NetworkWatcher</span></span>
<span data-ttu-id="a2706-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="a2706-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="a2706-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a2706-122">-NetworkWatcherName</span></span>
<span data-ttu-id="a2706-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="a2706-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="a2706-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2706-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2706-125">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a2706-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a2706-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a2706-126">-TargetResourceId</span></span>
<span data-ttu-id="a2706-127">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a2706-127">The target resource ID.</span></span>

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

### <span data-ttu-id="a2706-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2706-128">CommonParameters</span></span>
<span data-ttu-id="a2706-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2706-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2706-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2706-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2706-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2706-131">INPUTS</span></span>

### <span data-ttu-id="a2706-132">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2706-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a2706-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a2706-133">System.String</span></span>

## <span data-ttu-id="a2706-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2706-134">OUTPUTS</span></span>

### <span data-ttu-id="a2706-135">Microsoft. Azure. commands. Networks. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="a2706-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="a2706-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2706-136">NOTES</span></span>
<span data-ttu-id="a2706-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, flöde, loggar, flowlog, loggning</span><span class="sxs-lookup"><span data-stu-id="a2706-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="a2706-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2706-138">RELATED LINKS</span></span>

[<span data-ttu-id="a2706-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a2706-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a2706-140">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2706-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a2706-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2706-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a2706-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2706-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a2706-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2706-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2706-144">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a2706-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a2706-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2706-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2706-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2706-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2706-147">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2706-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2706-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a2706-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a2706-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a2706-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a2706-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a2706-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a2706-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a2706-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="a2706-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a2706-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a2706-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a2706-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
