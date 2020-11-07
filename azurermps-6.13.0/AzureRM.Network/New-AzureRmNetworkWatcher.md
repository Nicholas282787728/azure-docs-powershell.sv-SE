---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: f098e0d776ab115211fb562ed4889502995ffdd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758158"
---
# <span data-ttu-id="33f5b-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33f5b-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="33f5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="33f5b-103">Skapar en ny resurs för nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="33f5b-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33f5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33f5b-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33f5b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33f5b-105">DESCRIPTION</span></span>
<span data-ttu-id="33f5b-106">New-AzureRmNetworkWatcher-cmdleten skapar en ny nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="33f5b-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="33f5b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33f5b-107">EXAMPLES</span></span>

### <span data-ttu-id="33f5b-108">Exempel 1: skapa en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="33f5b-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="33f5b-109">I det här exemplet skapas en ny nätverks bevakning i en nyligen skapad resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="33f5b-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="33f5b-110">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="33f5b-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="33f5b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33f5b-111">PARAMETERS</span></span>

### <span data-ttu-id="33f5b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f5b-112">-DefaultProfile</span></span>
<span data-ttu-id="33f5b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33f5b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33f5b-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="33f5b-114">-Location</span></span>
<span data-ttu-id="33f5b-115">Plats.</span><span class="sxs-lookup"><span data-stu-id="33f5b-115">Location.</span></span>

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

### <span data-ttu-id="33f5b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="33f5b-116">-Name</span></span>
<span data-ttu-id="33f5b-117">Namnet på nät övervakaren.</span><span class="sxs-lookup"><span data-stu-id="33f5b-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33f5b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33f5b-118">-ResourceGroupName</span></span>
<span data-ttu-id="33f5b-119">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="33f5b-119">The resource group name.</span></span>

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

### <span data-ttu-id="33f5b-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="33f5b-120">-Tag</span></span>
<span data-ttu-id="33f5b-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="33f5b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="33f5b-122">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="33f5b-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33f5b-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33f5b-123">-Confirm</span></span>
<span data-ttu-id="33f5b-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33f5b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f5b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33f5b-125">-WhatIf</span></span>
<span data-ttu-id="33f5b-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33f5b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33f5b-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33f5b-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f5b-128">CommonParameters</span></span>
<span data-ttu-id="33f5b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f5b-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33f5b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f5b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33f5b-131">INPUTS</span></span>

### <span data-ttu-id="33f5b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="33f5b-132">System.String</span></span>

### <span data-ttu-id="33f5b-133">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="33f5b-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="33f5b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33f5b-134">OUTPUTS</span></span>

### <span data-ttu-id="33f5b-135">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33f5b-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="33f5b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33f5b-136">NOTES</span></span>
<span data-ttu-id="33f5b-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="33f5b-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="33f5b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33f5b-138">RELATED LINKS</span></span>

[<span data-ttu-id="33f5b-139">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33f5b-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="33f5b-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33f5b-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="33f5b-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33f5b-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="33f5b-142">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="33f5b-142">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="33f5b-143">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="33f5b-143">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="33f5b-144">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="33f5b-144">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="33f5b-145">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="33f5b-145">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="33f5b-146">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="33f5b-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="33f5b-147">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="33f5b-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="33f5b-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="33f5b-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="33f5b-149">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="33f5b-149">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="33f5b-150">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="33f5b-150">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="33f5b-151">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="33f5b-151">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="33f5b-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="33f5b-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="33f5b-153">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="33f5b-153">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="33f5b-154">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="33f5b-154">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="33f5b-155">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="33f5b-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="33f5b-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="33f5b-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="33f5b-157">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="33f5b-157">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="33f5b-158">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="33f5b-158">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="33f5b-159">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="33f5b-159">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="33f5b-160">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="33f5b-160">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="33f5b-161">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="33f5b-161">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="33f5b-162">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="33f5b-162">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="33f5b-163">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="33f5b-163">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="33f5b-164">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="33f5b-164">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="33f5b-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="33f5b-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
