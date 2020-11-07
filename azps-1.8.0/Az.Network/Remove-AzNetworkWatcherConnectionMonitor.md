---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 71b717ec1777dfd55e29925e82923d8d9f8d7a37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747859"
---
# <span data-ttu-id="29b2c-101">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29b2c-101">Remove-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="29b2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="29b2c-103">Ta bort anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="29b2c-103">Remove connection monitor.</span></span>

## <span data-ttu-id="29b2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29b2c-104">SYNTAX</span></span>

### <span data-ttu-id="29b2c-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="29b2c-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29b2c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="29b2c-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29b2c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="29b2c-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29b2c-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="29b2c-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29b2c-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="29b2c-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29b2c-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29b2c-110">DESCRIPTION</span></span>
<span data-ttu-id="29b2c-111">Cmdleten Remove-AzNetworkWatcherConnectionMonitor tar bort den angivna anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="29b2c-111">The remove-AzNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="29b2c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29b2c-112">EXAMPLES</span></span>

### <span data-ttu-id="29b2c-113">Exempel 1: ta bort den angivna anslutnings övervakaren</span><span class="sxs-lookup"><span data-stu-id="29b2c-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="29b2c-114">I det här exemplet tar vi bort anslutnings övervakaren som anges av plats och namn.</span><span class="sxs-lookup"><span data-stu-id="29b2c-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="29b2c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29b2c-115">PARAMETERS</span></span>

### <span data-ttu-id="29b2c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29b2c-116">-AsJob</span></span>
<span data-ttu-id="29b2c-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="29b2c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29b2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b2c-118">-DefaultProfile</span></span>
<span data-ttu-id="29b2c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29b2c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29b2c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29b2c-120">-InputObject</span></span>
<span data-ttu-id="29b2c-121">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="29b2c-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29b2c-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="29b2c-122">-Location</span></span>
<span data-ttu-id="29b2c-123">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="29b2c-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="29b2c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="29b2c-124">-Name</span></span>
<span data-ttu-id="29b2c-125">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="29b2c-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b2c-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29b2c-126">-NetworkWatcher</span></span>
<span data-ttu-id="29b2c-127">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="29b2c-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="29b2c-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="29b2c-128">-NetworkWatcherName</span></span>
<span data-ttu-id="29b2c-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="29b2c-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b2c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29b2c-130">-PassThru</span></span>
<span data-ttu-id="29b2c-131">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="29b2c-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="29b2c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29b2c-132">-ResourceGroupName</span></span>
<span data-ttu-id="29b2c-133">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="29b2c-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b2c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29b2c-134">-ResourceId</span></span>
<span data-ttu-id="29b2c-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="29b2c-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b2c-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29b2c-136">-Confirm</span></span>
<span data-ttu-id="29b2c-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29b2c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29b2c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29b2c-138">-WhatIf</span></span>
<span data-ttu-id="29b2c-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29b2c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29b2c-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29b2c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29b2c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b2c-141">CommonParameters</span></span>
<span data-ttu-id="29b2c-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29b2c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b2c-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b2c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b2c-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29b2c-144">INPUTS</span></span>

### <span data-ttu-id="29b2c-145">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29b2c-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="29b2c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="29b2c-146">System.String</span></span>

### <span data-ttu-id="29b2c-147">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="29b2c-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="29b2c-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29b2c-148">OUTPUTS</span></span>

### <span data-ttu-id="29b2c-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29b2c-149">System.Boolean</span></span>

## <span data-ttu-id="29b2c-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29b2c-150">NOTES</span></span>
<span data-ttu-id="29b2c-151">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="29b2c-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="29b2c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29b2c-152">RELATED LINKS</span></span>

[<span data-ttu-id="29b2c-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29b2c-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="29b2c-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29b2c-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="29b2c-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29b2c-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="29b2c-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="29b2c-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="29b2c-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="29b2c-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="29b2c-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="29b2c-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="29b2c-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="29b2c-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="29b2c-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29b2c-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29b2c-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="29b2c-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="29b2c-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29b2c-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29b2c-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29b2c-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29b2c-164">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29b2c-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29b2c-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29b2c-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29b2c-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="29b2c-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="29b2c-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29b2c-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29b2c-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29b2c-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29b2c-169">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29b2c-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29b2c-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29b2c-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29b2c-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="29b2c-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="29b2c-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="29b2c-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="29b2c-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="29b2c-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="29b2c-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="29b2c-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="29b2c-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29b2c-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29b2c-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="29b2c-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="29b2c-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="29b2c-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="29b2c-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="29b2c-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="29b2c-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="29b2c-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
