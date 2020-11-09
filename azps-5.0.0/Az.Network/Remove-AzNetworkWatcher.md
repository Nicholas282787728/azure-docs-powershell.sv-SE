---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323250"
---
# <span data-ttu-id="debc3-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="debc3-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="debc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="debc3-102">SYNOPSIS</span></span>
<span data-ttu-id="debc3-103">Tar bort en nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="debc3-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="debc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="debc3-104">SYNTAX</span></span>

### <span data-ttu-id="debc3-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="debc3-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="debc3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="debc3-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="debc3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="debc3-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="debc3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="debc3-108">DESCRIPTION</span></span>
<span data-ttu-id="debc3-109">Remove-AzNetworkWatcher cmdlet tar bort en nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="debc3-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="debc3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="debc3-110">EXAMPLES</span></span>

### <span data-ttu-id="debc3-111">Exempel 1: skapa och ta bort en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="debc3-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="debc3-112">I det här exemplet skapas en nätverks bevakning i en resurs grupp och sedan tas den omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="debc3-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="debc3-113">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="debc3-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="debc3-114">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="debc3-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="debc3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="debc3-115">PARAMETERS</span></span>

### <span data-ttu-id="debc3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="debc3-116">-AsJob</span></span>
<span data-ttu-id="debc3-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="debc3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="debc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debc3-118">-DefaultProfile</span></span>
<span data-ttu-id="debc3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="debc3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="debc3-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="debc3-120">-Location</span></span>
<span data-ttu-id="debc3-121">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="debc3-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="debc3-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="debc3-122">-Name</span></span>
<span data-ttu-id="debc3-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="debc3-123">The resource name.</span></span>

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

### <span data-ttu-id="debc3-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="debc3-124">-NetworkWatcher</span></span>
<span data-ttu-id="debc3-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="debc3-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="debc3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="debc3-126">-PassThru</span></span>
<span data-ttu-id="debc3-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="debc3-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="debc3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="debc3-128">-ResourceGroupName</span></span>
<span data-ttu-id="debc3-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="debc3-129">The resource group name.</span></span>

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

### <span data-ttu-id="debc3-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="debc3-130">-Confirm</span></span>
<span data-ttu-id="debc3-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="debc3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="debc3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="debc3-132">-WhatIf</span></span>
<span data-ttu-id="debc3-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="debc3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="debc3-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="debc3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="debc3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debc3-135">CommonParameters</span></span>
<span data-ttu-id="debc3-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="debc3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debc3-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="debc3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debc3-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="debc3-138">INPUTS</span></span>

### <span data-ttu-id="debc3-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="debc3-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="debc3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="debc3-140">System.String</span></span>

## <span data-ttu-id="debc3-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="debc3-141">OUTPUTS</span></span>

### <span data-ttu-id="debc3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="debc3-142">System.Boolean</span></span>

## <span data-ttu-id="debc3-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="debc3-143">NOTES</span></span>
<span data-ttu-id="debc3-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="debc3-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="debc3-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="debc3-145">RELATED LINKS</span></span>

[<span data-ttu-id="debc3-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="debc3-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="debc3-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="debc3-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="debc3-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="debc3-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="debc3-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="debc3-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="debc3-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="debc3-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="debc3-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="debc3-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="debc3-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="debc3-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="debc3-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="debc3-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="debc3-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="debc3-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="debc3-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="debc3-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="debc3-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="debc3-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="debc3-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="debc3-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="debc3-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="debc3-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="debc3-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="debc3-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="debc3-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="debc3-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="debc3-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="debc3-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="debc3-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="debc3-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="debc3-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="debc3-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="debc3-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="debc3-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="debc3-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="debc3-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="debc3-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="debc3-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="debc3-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="debc3-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="debc3-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="debc3-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="debc3-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="debc3-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="debc3-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="debc3-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="debc3-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="debc3-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="debc3-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="debc3-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
