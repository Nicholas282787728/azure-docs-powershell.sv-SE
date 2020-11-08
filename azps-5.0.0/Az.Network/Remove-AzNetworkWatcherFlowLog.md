---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 9906af7da12f76650ebbe45ff764da78c90ef340
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269187"
---
# <span data-ttu-id="f19dd-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="f19dd-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="f19dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f19dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f19dd-103">Tar bort den angivna flödes logg resursen.</span><span class="sxs-lookup"><span data-stu-id="f19dd-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="f19dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f19dd-104">SYNTAX</span></span>

### <span data-ttu-id="f19dd-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="f19dd-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19dd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f19dd-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19dd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f19dd-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19dd-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f19dd-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19dd-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f19dd-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f19dd-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f19dd-110">DESCRIPTION</span></span>
<span data-ttu-id="f19dd-111">Tar bort den angivna flödes logg resursen.</span><span class="sxs-lookup"><span data-stu-id="f19dd-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="f19dd-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f19dd-112">EXAMPLES</span></span>

### <span data-ttu-id="f19dd-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f19dd-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="f19dd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f19dd-114">PARAMETERS</span></span>

### <span data-ttu-id="f19dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f19dd-115">-AsJob</span></span>
<span data-ttu-id="f19dd-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f19dd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f19dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19dd-117">-DefaultProfile</span></span>
<span data-ttu-id="f19dd-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f19dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19dd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f19dd-119">-InputObject</span></span>
<span data-ttu-id="f19dd-120">Flödes logg objekt.</span><span class="sxs-lookup"><span data-stu-id="f19dd-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f19dd-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="f19dd-121">-Location</span></span>
<span data-ttu-id="f19dd-122">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="f19dd-122">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19dd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="f19dd-123">-Name</span></span>
<span data-ttu-id="f19dd-124">Flödets logg namn.</span><span class="sxs-lookup"><span data-stu-id="f19dd-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19dd-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f19dd-125">-NetworkWatcher</span></span>
<span data-ttu-id="f19dd-126">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="f19dd-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="f19dd-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f19dd-127">-NetworkWatcherName</span></span>
<span data-ttu-id="f19dd-128">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="f19dd-128">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19dd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f19dd-129">-PassThru</span></span>
<span data-ttu-id="f19dd-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f19dd-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f19dd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f19dd-131">-ResourceGroupName</span></span>
<span data-ttu-id="f19dd-132">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f19dd-132">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19dd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f19dd-133">-ResourceId</span></span>
<span data-ttu-id="f19dd-134">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f19dd-134">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f19dd-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f19dd-135">-Confirm</span></span>
<span data-ttu-id="f19dd-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f19dd-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19dd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19dd-137">-WhatIf</span></span>
<span data-ttu-id="f19dd-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f19dd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19dd-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f19dd-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19dd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19dd-140">CommonParameters</span></span>
<span data-ttu-id="f19dd-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f19dd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19dd-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f19dd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19dd-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f19dd-143">INPUTS</span></span>

### <span data-ttu-id="f19dd-144">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f19dd-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f19dd-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f19dd-145">System.String</span></span>

### <span data-ttu-id="f19dd-146">Microsoft. Azure. commands. Networks. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="f19dd-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="f19dd-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f19dd-147">OUTPUTS</span></span>

### <span data-ttu-id="f19dd-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f19dd-148">System.Boolean</span></span>

## <span data-ttu-id="f19dd-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f19dd-149">NOTES</span></span>

## <span data-ttu-id="f19dd-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f19dd-150">RELATED LINKS</span></span>

[<span data-ttu-id="f19dd-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f19dd-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f19dd-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f19dd-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f19dd-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f19dd-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f19dd-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f19dd-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f19dd-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f19dd-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f19dd-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f19dd-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f19dd-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f19dd-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f19dd-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f19dd-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f19dd-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f19dd-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f19dd-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f19dd-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f19dd-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f19dd-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f19dd-162">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f19dd-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f19dd-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f19dd-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f19dd-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f19dd-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f19dd-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f19dd-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f19dd-166">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f19dd-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f19dd-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f19dd-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f19dd-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f19dd-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f19dd-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f19dd-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f19dd-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f19dd-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f19dd-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f19dd-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f19dd-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f19dd-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f19dd-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f19dd-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f19dd-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f19dd-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f19dd-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f19dd-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f19dd-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f19dd-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f19dd-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f19dd-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="f19dd-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="f19dd-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="f19dd-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="f19dd-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="f19dd-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="f19dd-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)
