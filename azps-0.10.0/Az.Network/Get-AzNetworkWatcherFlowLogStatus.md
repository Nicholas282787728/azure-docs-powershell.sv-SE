---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922243"
---
# <span data-ttu-id="8dc92-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8dc92-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="8dc92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8dc92-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc92-103">Hämtar status för flödes loggning för en resurs.</span><span class="sxs-lookup"><span data-stu-id="8dc92-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="8dc92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8dc92-104">SYNTAX</span></span>

### <span data-ttu-id="8dc92-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="8dc92-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dc92-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8dc92-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dc92-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8dc92-107">DESCRIPTION</span></span>
<span data-ttu-id="8dc92-108">Get-AzNetworkWatcherFlowLogStatus cmdlet får statusen för flödes loggning för en resurs.</span><span class="sxs-lookup"><span data-stu-id="8dc92-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="8dc92-109">Statusen inkluderar om flödes loggning är aktiverat för den angivna resursen, det konfigurerade lagrings kontot för att skicka loggar och bevarande princip för loggarna.</span><span class="sxs-lookup"><span data-stu-id="8dc92-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="8dc92-110">För närvarande stöds nätverks säkerhets grupper för flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="8dc92-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="8dc92-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8dc92-111">EXAMPLES</span></span>

### <span data-ttu-id="8dc92-112">---Exempel 1: Hämta loggnings status för flödet för ett angivet NSG---</span><span class="sxs-lookup"><span data-stu-id="8dc92-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="8dc92-113">I det här exemplet får du status för flödes loggning för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="8dc92-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="8dc92-114">Den angivna NSG har flödes loggning aktive rad och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="8dc92-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="8dc92-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8dc92-115">PARAMETERS</span></span>

### <span data-ttu-id="8dc92-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dc92-116">-AsJob</span></span>
<span data-ttu-id="8dc92-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8dc92-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dc92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc92-118">-DefaultProfile</span></span>
<span data-ttu-id="8dc92-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc92-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dc92-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dc92-120">-NetworkWatcher</span></span>
<span data-ttu-id="8dc92-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="8dc92-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="8dc92-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8dc92-122">-NetworkWatcherName</span></span>
<span data-ttu-id="8dc92-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="8dc92-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="8dc92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc92-124">-ResourceGroupName</span></span>
<span data-ttu-id="8dc92-125">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8dc92-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8dc92-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc92-126">-TargetResourceId</span></span>
<span data-ttu-id="8dc92-127">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="8dc92-127">The target resource ID.</span></span>

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

### <span data-ttu-id="8dc92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc92-128">CommonParameters</span></span>
<span data-ttu-id="8dc92-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc92-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dc92-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc92-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8dc92-131">INPUTS</span></span>

### <span data-ttu-id="8dc92-132">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dc92-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8dc92-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8dc92-133">System.String</span></span>

## <span data-ttu-id="8dc92-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8dc92-134">OUTPUTS</span></span>

### <span data-ttu-id="8dc92-135">Microsoft. Azure. commands. Networks. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="8dc92-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="8dc92-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8dc92-136">NOTES</span></span>
<span data-ttu-id="8dc92-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, flöde, loggar, flowlog, loggning</span><span class="sxs-lookup"><span data-stu-id="8dc92-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="8dc92-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8dc92-138">RELATED LINKS</span></span>

[<span data-ttu-id="8dc92-139">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8dc92-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8dc92-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dc92-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8dc92-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dc92-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8dc92-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dc92-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8dc92-143">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dc92-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dc92-144">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8dc92-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8dc92-145">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dc92-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dc92-146">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dc92-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dc92-147">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dc92-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dc92-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8dc92-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8dc92-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8dc92-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8dc92-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8dc92-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8dc92-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8dc92-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8dc92-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8dc92-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8dc92-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8dc92-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
