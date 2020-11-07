---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 01e8a41c8d8854527037c447545f3d0601d4daf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757562"
---
# <span data-ttu-id="affd5-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="affd5-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="affd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="affd5-102">SYNOPSIS</span></span>
<span data-ttu-id="affd5-103">Ta bort anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="affd5-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="affd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="affd5-104">SYNTAX</span></span>

### <span data-ttu-id="affd5-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="affd5-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="affd5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="affd5-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="affd5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="affd5-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="affd5-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="affd5-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="affd5-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="affd5-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="affd5-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="affd5-110">DESCRIPTION</span></span>
<span data-ttu-id="affd5-111">Cmdleten Remove-AzureRmNetworkWatcherConnectionMonitor tar bort den angivna anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="affd5-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="affd5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="affd5-112">EXAMPLES</span></span>

### <span data-ttu-id="affd5-113">Exempel 1: ta bort den angivna anslutnings övervakaren</span><span class="sxs-lookup"><span data-stu-id="affd5-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="affd5-114">I det här exemplet tar vi bort anslutnings övervakaren som anges av plats och namn.</span><span class="sxs-lookup"><span data-stu-id="affd5-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="affd5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="affd5-115">PARAMETERS</span></span>

### <span data-ttu-id="affd5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="affd5-116">-AsJob</span></span>
<span data-ttu-id="affd5-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="affd5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="affd5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affd5-118">-DefaultProfile</span></span>
<span data-ttu-id="affd5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="affd5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="affd5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="affd5-120">-InputObject</span></span>
<span data-ttu-id="affd5-121">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="affd5-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="affd5-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="affd5-122">-Location</span></span>
<span data-ttu-id="affd5-123">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="affd5-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="affd5-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="affd5-124">-Name</span></span>
<span data-ttu-id="affd5-125">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="affd5-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="affd5-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="affd5-126">-NetworkWatcher</span></span>
<span data-ttu-id="affd5-127">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="affd5-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="affd5-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="affd5-128">-NetworkWatcherName</span></span>
<span data-ttu-id="affd5-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="affd5-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="affd5-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="affd5-130">-PassThru</span></span>
<span data-ttu-id="affd5-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="affd5-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="affd5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="affd5-132">-ResourceGroupName</span></span>
<span data-ttu-id="affd5-133">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="affd5-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="affd5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="affd5-134">-ResourceId</span></span>
<span data-ttu-id="affd5-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="affd5-135">Resource ID.</span></span>

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

### <span data-ttu-id="affd5-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="affd5-136">-Confirm</span></span>
<span data-ttu-id="affd5-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="affd5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="affd5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="affd5-138">-WhatIf</span></span>
<span data-ttu-id="affd5-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="affd5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="affd5-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="affd5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="affd5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affd5-141">CommonParameters</span></span>
<span data-ttu-id="affd5-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="affd5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affd5-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="affd5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affd5-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="affd5-144">INPUTS</span></span>

### <span data-ttu-id="affd5-145">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="affd5-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="affd5-146">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="affd5-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="affd5-147">System. String</span><span class="sxs-lookup"><span data-stu-id="affd5-147">System.String</span></span>

### <span data-ttu-id="affd5-148">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="affd5-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="affd5-149">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="affd5-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="affd5-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="affd5-150">OUTPUTS</span></span>

### <span data-ttu-id="affd5-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="affd5-151">System.Boolean</span></span>

## <span data-ttu-id="affd5-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="affd5-152">NOTES</span></span>
<span data-ttu-id="affd5-153">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="affd5-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="affd5-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="affd5-154">RELATED LINKS</span></span>

[<span data-ttu-id="affd5-155">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="affd5-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="affd5-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="affd5-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="affd5-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="affd5-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="affd5-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="affd5-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="affd5-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="affd5-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="affd5-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="affd5-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="affd5-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="affd5-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="affd5-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="affd5-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="affd5-163">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="affd5-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="affd5-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="affd5-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="affd5-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="affd5-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="affd5-166">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="affd5-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="affd5-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="affd5-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="affd5-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="affd5-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="affd5-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="affd5-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="affd5-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="affd5-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="affd5-171">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="affd5-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="affd5-172">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="affd5-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="affd5-173">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="affd5-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="affd5-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="affd5-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="affd5-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="affd5-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="affd5-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="affd5-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="affd5-177">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="affd5-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="affd5-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="affd5-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="affd5-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="affd5-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="affd5-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="affd5-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="affd5-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="affd5-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
