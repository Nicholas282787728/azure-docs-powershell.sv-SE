---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258177"
---
# <span data-ttu-id="0601a-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0601a-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="0601a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0601a-102">SYNOPSIS</span></span>
<span data-ttu-id="0601a-103">Tar bort en nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="0601a-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="0601a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0601a-104">SYNTAX</span></span>

### <span data-ttu-id="0601a-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0601a-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0601a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0601a-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0601a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0601a-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0601a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0601a-108">DESCRIPTION</span></span>
<span data-ttu-id="0601a-109">Remove-AzNetworkWatcher cmdlet tar bort en nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="0601a-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="0601a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0601a-110">EXAMPLES</span></span>

### <span data-ttu-id="0601a-111">Exempel 1: skapa och ta bort en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="0601a-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="0601a-112">I det här exemplet skapas en nätverks bevakning i en resurs grupp och sedan tas den omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="0601a-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="0601a-113">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0601a-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="0601a-114">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="0601a-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="0601a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0601a-115">PARAMETERS</span></span>

### <span data-ttu-id="0601a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0601a-116">-AsJob</span></span>
<span data-ttu-id="0601a-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0601a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0601a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0601a-118">-DefaultProfile</span></span>
<span data-ttu-id="0601a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0601a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0601a-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="0601a-120">-Location</span></span>
<span data-ttu-id="0601a-121">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="0601a-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0601a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0601a-122">-Name</span></span>
<span data-ttu-id="0601a-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0601a-123">The resource name.</span></span>

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

### <span data-ttu-id="0601a-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0601a-124">-NetworkWatcher</span></span>
<span data-ttu-id="0601a-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="0601a-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="0601a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0601a-126">-PassThru</span></span>
<span data-ttu-id="0601a-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0601a-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="0601a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0601a-128">-ResourceGroupName</span></span>
<span data-ttu-id="0601a-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0601a-129">The resource group name.</span></span>

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

### <span data-ttu-id="0601a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0601a-130">-Confirm</span></span>
<span data-ttu-id="0601a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0601a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0601a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0601a-132">-WhatIf</span></span>
<span data-ttu-id="0601a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0601a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0601a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0601a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0601a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0601a-135">CommonParameters</span></span>
<span data-ttu-id="0601a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0601a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0601a-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0601a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0601a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0601a-138">INPUTS</span></span>

### <span data-ttu-id="0601a-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0601a-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0601a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0601a-140">System.String</span></span>

## <span data-ttu-id="0601a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0601a-141">OUTPUTS</span></span>

### <span data-ttu-id="0601a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0601a-142">System.Boolean</span></span>

## <span data-ttu-id="0601a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0601a-143">NOTES</span></span>
<span data-ttu-id="0601a-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="0601a-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="0601a-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0601a-145">RELATED LINKS</span></span>

[<span data-ttu-id="0601a-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0601a-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0601a-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0601a-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0601a-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0601a-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0601a-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0601a-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0601a-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0601a-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0601a-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0601a-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0601a-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0601a-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0601a-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0601a-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0601a-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0601a-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0601a-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0601a-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0601a-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0601a-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0601a-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0601a-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0601a-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0601a-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0601a-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0601a-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0601a-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0601a-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0601a-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0601a-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0601a-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0601a-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0601a-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0601a-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0601a-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0601a-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0601a-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0601a-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0601a-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0601a-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0601a-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0601a-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0601a-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0601a-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0601a-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0601a-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0601a-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0601a-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0601a-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0601a-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0601a-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0601a-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
