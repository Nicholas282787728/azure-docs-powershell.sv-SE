---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: b06540e1f03058fd36302616d22375270b521b8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747858"
---
# <span data-ttu-id="86f21-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f21-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="86f21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86f21-102">SYNOPSIS</span></span>
<span data-ttu-id="86f21-103">Tar bort en nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="86f21-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="86f21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86f21-104">SYNTAX</span></span>

### <span data-ttu-id="86f21-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="86f21-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86f21-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="86f21-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86f21-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="86f21-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86f21-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86f21-108">DESCRIPTION</span></span>
<span data-ttu-id="86f21-109">Remove-AzNetworkWatcher cmdlet tar bort en nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="86f21-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="86f21-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86f21-110">EXAMPLES</span></span>

### <span data-ttu-id="86f21-111">Exempel 1: skapa och ta bort en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="86f21-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="86f21-112">I det här exemplet skapas en nätverks bevakning i en resurs grupp och sedan tas den omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="86f21-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="86f21-113">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="86f21-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="86f21-114">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="86f21-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="86f21-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86f21-115">PARAMETERS</span></span>

### <span data-ttu-id="86f21-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86f21-116">-AsJob</span></span>
<span data-ttu-id="86f21-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="86f21-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86f21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f21-118">-DefaultProfile</span></span>
<span data-ttu-id="86f21-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86f21-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86f21-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="86f21-120">-Location</span></span>
<span data-ttu-id="86f21-121">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="86f21-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="86f21-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="86f21-122">-Name</span></span>
<span data-ttu-id="86f21-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="86f21-123">The resource name.</span></span>

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

### <span data-ttu-id="86f21-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f21-124">-NetworkWatcher</span></span>
<span data-ttu-id="86f21-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="86f21-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="86f21-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86f21-126">-PassThru</span></span>
<span data-ttu-id="86f21-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="86f21-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="86f21-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f21-128">-ResourceGroupName</span></span>
<span data-ttu-id="86f21-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="86f21-129">The resource group name.</span></span>

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

### <span data-ttu-id="86f21-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86f21-130">-Confirm</span></span>
<span data-ttu-id="86f21-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86f21-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86f21-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86f21-132">-WhatIf</span></span>
<span data-ttu-id="86f21-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86f21-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86f21-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86f21-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86f21-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f21-135">CommonParameters</span></span>
<span data-ttu-id="86f21-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f21-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f21-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f21-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f21-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86f21-138">INPUTS</span></span>

### <span data-ttu-id="86f21-139">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f21-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="86f21-140">System. String</span><span class="sxs-lookup"><span data-stu-id="86f21-140">System.String</span></span>

## <span data-ttu-id="86f21-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86f21-141">OUTPUTS</span></span>

### <span data-ttu-id="86f21-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86f21-142">System.Boolean</span></span>

## <span data-ttu-id="86f21-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86f21-143">NOTES</span></span>
<span data-ttu-id="86f21-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="86f21-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="86f21-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86f21-145">RELATED LINKS</span></span>

[<span data-ttu-id="86f21-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f21-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="86f21-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f21-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="86f21-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f21-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="86f21-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="86f21-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="86f21-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86f21-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="86f21-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="86f21-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="86f21-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="86f21-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="86f21-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86f21-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86f21-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="86f21-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="86f21-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86f21-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86f21-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86f21-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86f21-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86f21-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86f21-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="86f21-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="86f21-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="86f21-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="86f21-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="86f21-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="86f21-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f21-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f21-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f21-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f21-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f21-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f21-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="86f21-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="86f21-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f21-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f21-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f21-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f21-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="86f21-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="86f21-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="86f21-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="86f21-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="86f21-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="86f21-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="86f21-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="86f21-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="86f21-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="86f21-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f21-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
