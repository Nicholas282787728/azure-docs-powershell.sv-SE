---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273189"
---
# <span data-ttu-id="80c18-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="80c18-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="80c18-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80c18-102">SYNOPSIS</span></span>
<span data-ttu-id="80c18-103">Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="80c18-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="80c18-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80c18-104">SYNTAX</span></span>

### <span data-ttu-id="80c18-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="80c18-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80c18-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="80c18-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80c18-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="80c18-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80c18-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80c18-108">DESCRIPTION</span></span>
<span data-ttu-id="80c18-109">Med Get-AzNetworkWatcherSecurityGroupView kan du Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="80c18-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="80c18-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80c18-110">EXAMPLES</span></span>

### <span data-ttu-id="80c18-111">Exempel 1: skapa ett samtal för en säkerhets grupp på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="80c18-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="80c18-112">I exemplet ovan skaffa vi först den regionala nätverks Watchheten och sedan en VM i regionen.</span><span class="sxs-lookup"><span data-stu-id="80c18-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="80c18-113">Då ringer vi ett samtal på den angivna virtuella datorns säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="80c18-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="80c18-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80c18-114">PARAMETERS</span></span>

### <span data-ttu-id="80c18-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80c18-115">-AsJob</span></span>
<span data-ttu-id="80c18-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="80c18-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80c18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c18-117">-DefaultProfile</span></span>
<span data-ttu-id="80c18-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80c18-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80c18-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="80c18-119">-Location</span></span>
<span data-ttu-id="80c18-120">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="80c18-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="80c18-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="80c18-121">-NetworkWatcher</span></span>
<span data-ttu-id="80c18-122">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="80c18-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="80c18-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="80c18-123">-NetworkWatcherName</span></span>
<span data-ttu-id="80c18-124">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="80c18-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80c18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c18-125">-ResourceGroupName</span></span>
<span data-ttu-id="80c18-126">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="80c18-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="80c18-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="80c18-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="80c18-128">Målprogram-ID för mål</span><span class="sxs-lookup"><span data-stu-id="80c18-128">The target VM Id</span></span>

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

### <span data-ttu-id="80c18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c18-129">CommonParameters</span></span>
<span data-ttu-id="80c18-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c18-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80c18-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c18-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80c18-132">INPUTS</span></span>

### <span data-ttu-id="80c18-133">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="80c18-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="80c18-134">System. String</span><span class="sxs-lookup"><span data-stu-id="80c18-134">System.String</span></span>

## <span data-ttu-id="80c18-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80c18-135">OUTPUTS</span></span>

### <span data-ttu-id="80c18-136">Microsoft. Azure. commands. Networks. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="80c18-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="80c18-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80c18-137">NOTES</span></span>
<span data-ttu-id="80c18-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="80c18-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="80c18-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80c18-139">RELATED LINKS</span></span>

[<span data-ttu-id="80c18-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="80c18-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="80c18-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="80c18-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="80c18-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="80c18-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="80c18-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="80c18-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="80c18-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="80c18-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="80c18-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="80c18-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="80c18-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="80c18-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="80c18-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="80c18-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="80c18-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="80c18-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="80c18-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="80c18-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="80c18-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="80c18-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="80c18-151">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="80c18-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="80c18-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="80c18-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="80c18-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="80c18-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="80c18-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="80c18-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="80c18-155">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="80c18-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="80c18-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="80c18-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="80c18-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="80c18-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="80c18-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="80c18-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="80c18-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="80c18-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="80c18-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="80c18-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="80c18-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="80c18-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="80c18-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="80c18-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="80c18-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="80c18-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="80c18-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="80c18-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="80c18-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="80c18-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="80c18-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="80c18-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)