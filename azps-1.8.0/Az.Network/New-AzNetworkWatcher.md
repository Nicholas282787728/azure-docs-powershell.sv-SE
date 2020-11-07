---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 30b8fda9c29608759360e396f5dcecde3c9b95d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748027"
---
# <span data-ttu-id="93f8d-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93f8d-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="93f8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="93f8d-103">Skapar en ny resurs för nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="93f8d-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="93f8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93f8d-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93f8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93f8d-105">DESCRIPTION</span></span>
<span data-ttu-id="93f8d-106">New-AzNetworkWatcher-cmdleten skapar en ny nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="93f8d-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="93f8d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93f8d-107">EXAMPLES</span></span>

### <span data-ttu-id="93f8d-108">Exempel 1: skapa en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="93f8d-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="93f8d-109">I det här exemplet skapas en ny nätverks bevakning i en nyligen skapad resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="93f8d-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="93f8d-110">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="93f8d-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="93f8d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93f8d-111">PARAMETERS</span></span>

### <span data-ttu-id="93f8d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f8d-112">-DefaultProfile</span></span>
<span data-ttu-id="93f8d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93f8d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f8d-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="93f8d-114">-Location</span></span>
<span data-ttu-id="93f8d-115">Plats.</span><span class="sxs-lookup"><span data-stu-id="93f8d-115">Location.</span></span>

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

### <span data-ttu-id="93f8d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="93f8d-116">-Name</span></span>
<span data-ttu-id="93f8d-117">Namnet på nät övervakaren.</span><span class="sxs-lookup"><span data-stu-id="93f8d-117">The network watcher name.</span></span>

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

### <span data-ttu-id="93f8d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f8d-118">-ResourceGroupName</span></span>
<span data-ttu-id="93f8d-119">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="93f8d-119">The resource group name.</span></span>

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

### <span data-ttu-id="93f8d-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="93f8d-120">-Tag</span></span>
<span data-ttu-id="93f8d-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="93f8d-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="93f8d-122">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="93f8d-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="93f8d-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93f8d-123">-Confirm</span></span>
<span data-ttu-id="93f8d-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93f8d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93f8d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f8d-125">-WhatIf</span></span>
<span data-ttu-id="93f8d-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93f8d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f8d-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93f8d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93f8d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f8d-128">CommonParameters</span></span>
<span data-ttu-id="93f8d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f8d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f8d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f8d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f8d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93f8d-131">INPUTS</span></span>

### <span data-ttu-id="93f8d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="93f8d-132">System.String</span></span>

### <span data-ttu-id="93f8d-133">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="93f8d-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="93f8d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93f8d-134">OUTPUTS</span></span>

### <span data-ttu-id="93f8d-135">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93f8d-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="93f8d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93f8d-136">NOTES</span></span>
<span data-ttu-id="93f8d-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="93f8d-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="93f8d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93f8d-138">RELATED LINKS</span></span>

[<span data-ttu-id="93f8d-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93f8d-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="93f8d-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93f8d-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="93f8d-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93f8d-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="93f8d-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="93f8d-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="93f8d-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="93f8d-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="93f8d-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="93f8d-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="93f8d-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="93f8d-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="93f8d-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93f8d-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93f8d-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="93f8d-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="93f8d-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93f8d-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93f8d-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93f8d-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93f8d-150">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93f8d-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93f8d-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="93f8d-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="93f8d-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="93f8d-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="93f8d-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="93f8d-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="93f8d-154">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93f8d-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93f8d-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93f8d-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93f8d-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93f8d-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93f8d-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="93f8d-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="93f8d-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93f8d-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93f8d-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93f8d-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93f8d-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="93f8d-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="93f8d-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="93f8d-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="93f8d-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="93f8d-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="93f8d-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="93f8d-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="93f8d-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="93f8d-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="93f8d-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93f8d-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
