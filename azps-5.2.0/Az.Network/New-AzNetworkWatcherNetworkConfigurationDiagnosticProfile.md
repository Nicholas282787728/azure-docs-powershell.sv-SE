---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390792"
---
# <span data-ttu-id="ed438-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="ed438-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="ed438-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed438-102">SYNOPSIS</span></span>
<span data-ttu-id="ed438-103">Skapar ett nytt användar profil objekt för nätverks konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ed438-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="ed438-104">Det här objektet används för att begränsa nätverks konfigurationen under en diagnostisk session med de angivna villkoren.</span><span class="sxs-lookup"><span data-stu-id="ed438-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="ed438-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed438-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed438-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed438-106">DESCRIPTION</span></span>
<span data-ttu-id="ed438-107">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile-cmdleten skapar ett nytt diagnostiskt profil objekt.</span><span class="sxs-lookup"><span data-stu-id="ed438-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="ed438-108">Det här objektet används för att begränsa nätverks konfigurationen under en diagnostisk session med nätverks konfiguration med angivna villkor.</span><span class="sxs-lookup"><span data-stu-id="ed438-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="ed438-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed438-109">EXAMPLES</span></span>

### <span data-ttu-id="ed438-110">Exempel 1: starta Nätverksdiagnostik för virtuell dator och angiven nätverks profil</span><span class="sxs-lookup"><span data-stu-id="ed438-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="ed438-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed438-111">PARAMETERS</span></span>

### <span data-ttu-id="ed438-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed438-112">-DefaultProfile</span></span>
<span data-ttu-id="ed438-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed438-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed438-114">-Mål</span><span class="sxs-lookup"><span data-stu-id="ed438-114">-Destination</span></span>
<span data-ttu-id="ed438-115">Trafik destination.</span><span class="sxs-lookup"><span data-stu-id="ed438-115">Traffic destination.</span></span>
<span data-ttu-id="ed438-116">Godkända värden är: ' \* ', IP-adress/CIDR, service märke.</span><span class="sxs-lookup"><span data-stu-id="ed438-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="ed438-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ed438-117">-DestinationPort</span></span>
<span data-ttu-id="ed438-118">Målport för trafik.</span><span class="sxs-lookup"><span data-stu-id="ed438-118">Traffic destination port.</span></span>
<span data-ttu-id="ed438-119">Godkända värden är ' \* ', port (till exempel 3389) och port intervall (till exempel 80-100).</span><span class="sxs-lookup"><span data-stu-id="ed438-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="ed438-120">-Riktning</span><span class="sxs-lookup"><span data-stu-id="ed438-120">-Direction</span></span>
<span data-ttu-id="ed438-121">Riktningen för trafiken.</span><span class="sxs-lookup"><span data-stu-id="ed438-121">The direction of the traffic.</span></span>
<span data-ttu-id="ed438-122">Godkända värden är "inkommande" och "utgående"</span><span class="sxs-lookup"><span data-stu-id="ed438-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed438-123">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ed438-123">-Protocol</span></span>
<span data-ttu-id="ed438-124">Protokollet som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="ed438-124">Protocol to be verified on.</span></span>
<span data-ttu-id="ed438-125">Godkända värden är "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="ed438-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="ed438-126">-Källa</span><span class="sxs-lookup"><span data-stu-id="ed438-126">-Source</span></span>
<span data-ttu-id="ed438-127">Trafik källa.</span><span class="sxs-lookup"><span data-stu-id="ed438-127">Traffic source.</span></span>
<span data-ttu-id="ed438-128">Godkända värden är ' \* ', IP Address/CIDR, service tag.</span><span class="sxs-lookup"><span data-stu-id="ed438-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="ed438-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed438-129">CommonParameters</span></span>
<span data-ttu-id="ed438-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed438-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed438-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed438-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed438-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed438-132">INPUTS</span></span>

### <span data-ttu-id="ed438-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ed438-133">System.String</span></span>

## <span data-ttu-id="ed438-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed438-134">OUTPUTS</span></span>

### <span data-ttu-id="ed438-135">Microsoft. Azure. commands. Networks. Models. PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="ed438-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="ed438-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed438-136">NOTES</span></span>
<span data-ttu-id="ed438-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, diagnostik, profil</span><span class="sxs-lookup"><span data-stu-id="ed438-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="ed438-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed438-138">RELATED LINKS</span></span>

[<span data-ttu-id="ed438-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed438-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ed438-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed438-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ed438-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed438-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ed438-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ed438-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ed438-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ed438-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ed438-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ed438-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ed438-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ed438-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ed438-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed438-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed438-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ed438-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ed438-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed438-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed438-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed438-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed438-150">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed438-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed438-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed438-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ed438-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ed438-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ed438-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ed438-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ed438-154">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed438-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed438-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed438-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed438-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed438-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed438-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ed438-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ed438-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed438-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed438-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed438-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed438-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ed438-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ed438-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ed438-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ed438-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ed438-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ed438-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ed438-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ed438-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ed438-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ed438-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed438-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
