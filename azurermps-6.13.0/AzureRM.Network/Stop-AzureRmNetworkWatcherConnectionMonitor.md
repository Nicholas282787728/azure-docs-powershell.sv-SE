---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3cb69a6dbf2a08c242d0a49e6d023692663b7f19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578852"
---
# <span data-ttu-id="8ca16-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca16-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="8ca16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ca16-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca16-103">Stoppa en anslutnings övervakare</span><span class="sxs-lookup"><span data-stu-id="8ca16-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ca16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ca16-104">SYNTAX</span></span>

### <span data-ttu-id="8ca16-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="8ca16-105">SetByName (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ca16-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8ca16-106">SetByResource</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ca16-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8ca16-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ca16-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ca16-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ca16-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ca16-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ca16-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ca16-110">DESCRIPTION</span></span>
<span data-ttu-id="8ca16-111">Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stoppar den angivna anslutnings skärmen.</span><span class="sxs-lookup"><span data-stu-id="8ca16-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="8ca16-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ca16-112">EXAMPLES</span></span>

### <span data-ttu-id="8ca16-113">Exempel 1: stoppa en anslutnings bildskärm</span><span class="sxs-lookup"><span data-stu-id="8ca16-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="8ca16-114">I det här exemplet stoppar vi anslutnings övervakaren som anges med namn och nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="8ca16-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="8ca16-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ca16-115">PARAMETERS</span></span>

### <span data-ttu-id="8ca16-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ca16-116">-AsJob</span></span>
<span data-ttu-id="8ca16-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8ca16-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ca16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca16-118">-DefaultProfile</span></span>
<span data-ttu-id="8ca16-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca16-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ca16-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ca16-120">-InputObject</span></span>
<span data-ttu-id="8ca16-121">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="8ca16-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="8ca16-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="8ca16-122">-Location</span></span>
<span data-ttu-id="8ca16-123">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="8ca16-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8ca16-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="8ca16-124">-Name</span></span>
<span data-ttu-id="8ca16-125">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="8ca16-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="8ca16-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca16-126">-NetworkWatcher</span></span>
<span data-ttu-id="8ca16-127">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="8ca16-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="8ca16-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8ca16-128">-NetworkWatcherName</span></span>
<span data-ttu-id="8ca16-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="8ca16-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="8ca16-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ca16-130">-PassThru</span></span>
<span data-ttu-id="8ca16-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8ca16-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8ca16-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ca16-132">-ResourceGroupName</span></span>
<span data-ttu-id="8ca16-133">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8ca16-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8ca16-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ca16-134">-ResourceId</span></span>
<span data-ttu-id="8ca16-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="8ca16-135">Resource ID.</span></span>

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

### <span data-ttu-id="8ca16-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8ca16-136">-Confirm</span></span>
<span data-ttu-id="8ca16-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ca16-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ca16-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ca16-138">-WhatIf</span></span>
<span data-ttu-id="8ca16-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8ca16-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ca16-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8ca16-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ca16-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca16-141">CommonParameters</span></span>
<span data-ttu-id="8ca16-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ca16-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca16-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ca16-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca16-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ca16-144">INPUTS</span></span>

### <span data-ttu-id="8ca16-145">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca16-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8ca16-146">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ca16-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="8ca16-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8ca16-147">System.String</span></span>

### <span data-ttu-id="8ca16-148">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="8ca16-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="8ca16-149">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ca16-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8ca16-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ca16-150">OUTPUTS</span></span>

### <span data-ttu-id="8ca16-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ca16-151">System.Boolean</span></span>

## <span data-ttu-id="8ca16-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ca16-152">NOTES</span></span>
<span data-ttu-id="8ca16-153">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="8ca16-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="8ca16-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ca16-154">RELATED LINKS</span></span>

[<span data-ttu-id="8ca16-155">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca16-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8ca16-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca16-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8ca16-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca16-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8ca16-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8ca16-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="8ca16-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8ca16-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="8ca16-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8ca16-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="8ca16-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8ca16-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="8ca16-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ca16-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8ca16-163">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8ca16-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="8ca16-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ca16-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8ca16-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ca16-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8ca16-166">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ca16-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8ca16-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca16-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca16-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8ca16-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="8ca16-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca16-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca16-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca16-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca16-171">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca16-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca16-172">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca16-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca16-173">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca16-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="8ca16-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8ca16-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="8ca16-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8ca16-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="8ca16-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8ca16-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="8ca16-177">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca16-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca16-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8ca16-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="8ca16-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8ca16-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="8ca16-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8ca16-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="8ca16-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8ca16-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
