---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: 5a1500554c1026b591faea63074ca9c12fef1b10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417552"
---
# <span data-ttu-id="dfce2-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dfce2-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="dfce2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfce2-102">SYNOPSIS</span></span>
<span data-ttu-id="dfce2-103">Starta diagnostiksessionen för nätverks konfiguration för angivna nätverks profiler på mål resursen.</span><span class="sxs-lookup"><span data-stu-id="dfce2-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="dfce2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfce2-104">SYNTAX</span></span>

### <span data-ttu-id="dfce2-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="dfce2-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfce2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dfce2-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfce2-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="dfce2-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfce2-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dfce2-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfce2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfce2-109">DESCRIPTION</span></span>
<span data-ttu-id="dfce2-110">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet anropar diagnostiksessionen för nätverks konfiguration för angivna nätverks profiler på mål resursen.</span><span class="sxs-lookup"><span data-stu-id="dfce2-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="dfce2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfce2-111">EXAMPLES</span></span>

### <span data-ttu-id="dfce2-112">Exempel 1: starta Nätverksdiagnostik för virtuell dator och angiven nätverks profil</span><span class="sxs-lookup"><span data-stu-id="dfce2-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="dfce2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfce2-113">PARAMETERS</span></span>

### <span data-ttu-id="dfce2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfce2-114">-AsJob</span></span>
<span data-ttu-id="dfce2-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dfce2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfce2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfce2-116">-DefaultProfile</span></span>
<span data-ttu-id="dfce2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfce2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfce2-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="dfce2-118">-Location</span></span>
<span data-ttu-id="dfce2-119">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="dfce2-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="dfce2-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dfce2-120">-NetworkWatcher</span></span>
<span data-ttu-id="dfce2-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="dfce2-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="dfce2-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dfce2-122">-NetworkWatcherName</span></span>
<span data-ttu-id="dfce2-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="dfce2-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfce2-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="dfce2-124">-Profile</span></span>
<span data-ttu-id="dfce2-125">Lista över profiler för nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dfce2-125">List of network configuration diagnostic profiles.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfce2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfce2-126">-ResourceGroupName</span></span>
<span data-ttu-id="dfce2-127">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dfce2-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dfce2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfce2-128">-ResourceId</span></span>
<span data-ttu-id="dfce2-129">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="dfce2-129">Resource ID.</span></span>

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

### <span data-ttu-id="dfce2-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dfce2-130">-TargetResourceId</span></span>
<span data-ttu-id="dfce2-131">ID: t för mål resursen för att utföra Nätverksdiagnostik för nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dfce2-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="dfce2-132">Giltiga alternativ är VM, NetworkInterface, VMSS/NetworkInterface och Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dfce2-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="dfce2-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="dfce2-133">-VerbosityLevel</span></span>
<span data-ttu-id="dfce2-134">Utförlig nivå.</span><span class="sxs-lookup"><span data-stu-id="dfce2-134">Verbosity level.</span></span>
<span data-ttu-id="dfce2-135">Godkända värden är "normal", "minimum", "full".</span><span class="sxs-lookup"><span data-stu-id="dfce2-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfce2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfce2-136">CommonParameters</span></span>
<span data-ttu-id="dfce2-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfce2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfce2-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfce2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfce2-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfce2-139">INPUTS</span></span>

### <span data-ttu-id="dfce2-140">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dfce2-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="dfce2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dfce2-141">System.String</span></span>

## <span data-ttu-id="dfce2-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfce2-142">OUTPUTS</span></span>

### <span data-ttu-id="dfce2-143">Microsoft. Azure. commands. Networks. Models. PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="dfce2-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="dfce2-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfce2-144">NOTES</span></span>
<span data-ttu-id="dfce2-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, diagnostik, profil</span><span class="sxs-lookup"><span data-stu-id="dfce2-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="dfce2-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfce2-146">RELATED LINKS</span></span>

[<span data-ttu-id="dfce2-147">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dfce2-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="dfce2-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dfce2-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="dfce2-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dfce2-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="dfce2-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dfce2-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="dfce2-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dfce2-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dfce2-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dfce2-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="dfce2-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dfce2-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dfce2-154">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dfce2-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dfce2-155">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dfce2-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="dfce2-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dfce2-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dfce2-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dfce2-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dfce2-158">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dfce2-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dfce2-159">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfce2-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="dfce2-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dfce2-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="dfce2-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="dfce2-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="dfce2-162">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dfce2-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dfce2-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dfce2-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dfce2-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dfce2-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dfce2-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="dfce2-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="dfce2-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dfce2-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dfce2-167">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dfce2-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dfce2-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="dfce2-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="dfce2-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="dfce2-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="dfce2-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="dfce2-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="dfce2-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="dfce2-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="dfce2-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="dfce2-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="dfce2-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dfce2-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
