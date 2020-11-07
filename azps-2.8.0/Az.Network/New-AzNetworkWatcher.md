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
ms.locfileid: "93919091"
---
# <span data-ttu-id="deb34-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="deb34-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="deb34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="deb34-102">SYNOPSIS</span></span>
<span data-ttu-id="deb34-103">Skapar en ny resurs för nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="deb34-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="deb34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="deb34-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deb34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="deb34-105">DESCRIPTION</span></span>
<span data-ttu-id="deb34-106">New-AzNetworkWatcher-cmdleten skapar en ny nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="deb34-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="deb34-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="deb34-107">EXAMPLES</span></span>

### <span data-ttu-id="deb34-108">Exempel 1: skapa en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="deb34-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="deb34-109">I det här exemplet skapas en ny nätverks bevakning i en nyligen skapad resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="deb34-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="deb34-110">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="deb34-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="deb34-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="deb34-111">PARAMETERS</span></span>

### <span data-ttu-id="deb34-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb34-112">-DefaultProfile</span></span>
<span data-ttu-id="deb34-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="deb34-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deb34-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="deb34-114">-Location</span></span>
<span data-ttu-id="deb34-115">Plats.</span><span class="sxs-lookup"><span data-stu-id="deb34-115">Location.</span></span>

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

### <span data-ttu-id="deb34-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="deb34-116">-Name</span></span>
<span data-ttu-id="deb34-117">Namnet på nät övervakaren.</span><span class="sxs-lookup"><span data-stu-id="deb34-117">The network watcher name.</span></span>

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

### <span data-ttu-id="deb34-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb34-118">-ResourceGroupName</span></span>
<span data-ttu-id="deb34-119">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="deb34-119">The resource group name.</span></span>

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

### <span data-ttu-id="deb34-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="deb34-120">-Tag</span></span>
<span data-ttu-id="deb34-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="deb34-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="deb34-122">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="deb34-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="deb34-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="deb34-123">-Confirm</span></span>
<span data-ttu-id="deb34-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="deb34-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb34-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb34-125">-WhatIf</span></span>
<span data-ttu-id="deb34-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="deb34-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb34-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="deb34-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb34-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb34-128">CommonParameters</span></span>
<span data-ttu-id="deb34-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb34-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb34-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb34-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb34-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="deb34-131">INPUTS</span></span>

### <span data-ttu-id="deb34-132">System. String</span><span class="sxs-lookup"><span data-stu-id="deb34-132">System.String</span></span>

### <span data-ttu-id="deb34-133">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="deb34-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="deb34-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="deb34-134">OUTPUTS</span></span>

### <span data-ttu-id="deb34-135">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="deb34-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="deb34-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="deb34-136">NOTES</span></span>
<span data-ttu-id="deb34-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="deb34-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="deb34-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="deb34-138">RELATED LINKS</span></span>

[<span data-ttu-id="deb34-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="deb34-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="deb34-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="deb34-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="deb34-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="deb34-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="deb34-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="deb34-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="deb34-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="deb34-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="deb34-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="deb34-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="deb34-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="deb34-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="deb34-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="deb34-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="deb34-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="deb34-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="deb34-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="deb34-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="deb34-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="deb34-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="deb34-150">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="deb34-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="deb34-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="deb34-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="deb34-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="deb34-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="deb34-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="deb34-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="deb34-154">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="deb34-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="deb34-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="deb34-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="deb34-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="deb34-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="deb34-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="deb34-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="deb34-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="deb34-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="deb34-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="deb34-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="deb34-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="deb34-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="deb34-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="deb34-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="deb34-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="deb34-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="deb34-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="deb34-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="deb34-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="deb34-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="deb34-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="deb34-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
