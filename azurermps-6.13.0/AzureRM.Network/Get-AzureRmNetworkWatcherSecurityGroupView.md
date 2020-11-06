---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 9fe23ea5fa9bef544feae6112879cb1be6eeae7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574802"
---
# <span data-ttu-id="5e776-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5e776-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="5e776-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e776-102">SYNOPSIS</span></span>
<span data-ttu-id="5e776-103">Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5e776-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e776-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e776-104">SYNTAX</span></span>

### <span data-ttu-id="5e776-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="5e776-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e776-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5e776-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e776-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5e776-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e776-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e776-108">DESCRIPTION</span></span>
<span data-ttu-id="5e776-109">Med Get-AzureRmNetworkWatcherSecurityGroupView kan du Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5e776-109">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="5e776-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e776-110">EXAMPLES</span></span>

### <span data-ttu-id="5e776-111">Exempel 1: skapa ett samtal för en säkerhets grupp på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="5e776-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="5e776-112">I exemplet ovan skaffa vi först den regionala nätverks Watchheten och sedan en VM i regionen.</span><span class="sxs-lookup"><span data-stu-id="5e776-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="5e776-113">Då ringer vi ett samtal på den angivna virtuella datorns säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="5e776-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="5e776-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e776-114">PARAMETERS</span></span>

### <span data-ttu-id="5e776-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e776-115">-AsJob</span></span>
<span data-ttu-id="5e776-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5e776-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e776-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e776-117">-DefaultProfile</span></span>
<span data-ttu-id="5e776-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e776-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e776-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="5e776-119">-Location</span></span>
<span data-ttu-id="5e776-120">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="5e776-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5e776-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e776-121">-NetworkWatcher</span></span>
<span data-ttu-id="5e776-122">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="5e776-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="5e776-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5e776-123">-NetworkWatcherName</span></span>
<span data-ttu-id="5e776-124">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="5e776-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="5e776-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e776-125">-ResourceGroupName</span></span>
<span data-ttu-id="5e776-126">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5e776-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5e776-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5e776-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="5e776-128">Målprogram-ID för mål</span><span class="sxs-lookup"><span data-stu-id="5e776-128">The target VM Id</span></span>

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

### <span data-ttu-id="5e776-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e776-129">CommonParameters</span></span>
<span data-ttu-id="5e776-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e776-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e776-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e776-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e776-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e776-132">INPUTS</span></span>

### <span data-ttu-id="5e776-133">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e776-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5e776-134">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e776-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="5e776-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5e776-135">System.String</span></span>
<span data-ttu-id="5e776-136">Parametrar: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e776-136">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="5e776-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e776-137">OUTPUTS</span></span>

### <span data-ttu-id="5e776-138">Microsoft. Azure. commands. Networks. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="5e776-138">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="5e776-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e776-139">NOTES</span></span>
<span data-ttu-id="5e776-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="5e776-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="5e776-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e776-141">RELATED LINKS</span></span>

[<span data-ttu-id="5e776-142">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e776-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e776-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e776-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e776-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e776-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e776-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5e776-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5e776-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5e776-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5e776-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5e776-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5e776-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5e776-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5e776-149">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e776-149">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e776-150">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5e776-150">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5e776-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e776-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e776-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e776-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e776-153">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e776-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e776-154">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e776-154">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5e776-155">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5e776-155">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5e776-156">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5e776-156">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="5e776-157">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e776-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e776-158">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e776-158">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e776-159">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e776-159">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e776-160">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5e776-160">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5e776-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e776-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e776-162">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e776-162">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e776-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5e776-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5e776-164">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5e776-164">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5e776-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5e776-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5e776-166">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5e776-166">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5e776-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5e776-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="5e776-168">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e776-168">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
