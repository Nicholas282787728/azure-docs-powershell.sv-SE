---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525820"
---
# <span data-ttu-id="31809-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31809-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="31809-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31809-102">SYNOPSIS</span></span>
<span data-ttu-id="31809-103">Tar bort en nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="31809-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="31809-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31809-104">SYNTAX</span></span>

### <span data-ttu-id="31809-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="31809-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31809-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="31809-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31809-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="31809-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31809-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31809-108">DESCRIPTION</span></span>
<span data-ttu-id="31809-109">Remove-AzNetworkWatcher cmdlet tar bort en nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="31809-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="31809-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31809-110">EXAMPLES</span></span>

### <span data-ttu-id="31809-111">Exempel 1: skapa och ta bort en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="31809-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="31809-112">I det här exemplet skapas en nätverks bevakning i en resurs grupp och sedan tas den omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="31809-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="31809-113">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="31809-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="31809-114">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="31809-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="31809-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31809-115">PARAMETERS</span></span>

### <span data-ttu-id="31809-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31809-116">-AsJob</span></span>
<span data-ttu-id="31809-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="31809-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31809-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31809-118">-DefaultProfile</span></span>
<span data-ttu-id="31809-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31809-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31809-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="31809-120">-Location</span></span>
<span data-ttu-id="31809-121">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="31809-121">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31809-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="31809-122">-Name</span></span>
<span data-ttu-id="31809-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="31809-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31809-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31809-124">-NetworkWatcher</span></span>
<span data-ttu-id="31809-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="31809-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="31809-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31809-126">-PassThru</span></span>
<span data-ttu-id="31809-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="31809-127">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31809-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31809-128">-ResourceGroupName</span></span>
<span data-ttu-id="31809-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="31809-129">The resource group name.</span></span>

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

### <span data-ttu-id="31809-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="31809-130">-Confirm</span></span>
<span data-ttu-id="31809-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="31809-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31809-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31809-132">-WhatIf</span></span>
<span data-ttu-id="31809-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="31809-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31809-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="31809-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31809-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31809-135">CommonParameters</span></span>
<span data-ttu-id="31809-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31809-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31809-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31809-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31809-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31809-138">INPUTS</span></span>

### <span data-ttu-id="31809-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31809-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="31809-140">System. String</span><span class="sxs-lookup"><span data-stu-id="31809-140">System.String</span></span>

## <span data-ttu-id="31809-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31809-141">OUTPUTS</span></span>

### <span data-ttu-id="31809-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31809-142">System.Boolean</span></span>

## <span data-ttu-id="31809-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31809-143">NOTES</span></span>
<span data-ttu-id="31809-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="31809-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="31809-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31809-145">RELATED LINKS</span></span>

[<span data-ttu-id="31809-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31809-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="31809-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31809-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="31809-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31809-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="31809-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="31809-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="31809-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="31809-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="31809-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="31809-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="31809-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="31809-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="31809-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31809-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31809-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="31809-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="31809-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31809-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31809-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31809-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31809-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31809-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31809-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="31809-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="31809-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="31809-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="31809-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="31809-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="31809-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31809-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="31809-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31809-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="31809-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31809-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="31809-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="31809-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="31809-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31809-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="31809-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31809-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="31809-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="31809-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="31809-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="31809-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="31809-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="31809-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="31809-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="31809-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="31809-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="31809-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="31809-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="31809-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
