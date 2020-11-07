---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a2c66f9e93a26c433c245f87c8506b71ad01c5e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926490"
---
# <span data-ttu-id="a7bcc-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a7bcc-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="a7bcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bcc-103">Här listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="a7bcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7bcc-104">SYNTAX</span></span>

### <span data-ttu-id="a7bcc-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a7bcc-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7bcc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a7bcc-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7bcc-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a7bcc-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7bcc-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7bcc-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7bcc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7bcc-109">DESCRIPTION</span></span>
<span data-ttu-id="a7bcc-110">I Get-AzNetworkWatcherReachabilityProvidersList listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="a7bcc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7bcc-111">EXAMPLES</span></span>

### <span data-ttu-id="a7bcc-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a7bcc-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="a7bcc-113">Här listas alla tillgängliga providrar i Seattle, WA för Azure Data Center i västra USA.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="a7bcc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7bcc-114">PARAMETERS</span></span>

### <span data-ttu-id="a7bcc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7bcc-115">-AsJob</span></span>
<span data-ttu-id="a7bcc-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a7bcc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7bcc-117">-Ort</span><span class="sxs-lookup"><span data-stu-id="a7bcc-117">-City</span></span>
<span data-ttu-id="a7bcc-118">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-118">The name of the city.</span></span>

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

### <span data-ttu-id="a7bcc-119">-Country</span><span class="sxs-lookup"><span data-stu-id="a7bcc-119">-Country</span></span>
<span data-ttu-id="a7bcc-120">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-120">The name of the country.</span></span>

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

### <span data-ttu-id="a7bcc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7bcc-121">-DefaultProfile</span></span>
<span data-ttu-id="a7bcc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7bcc-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="a7bcc-123">-Location</span></span>
<span data-ttu-id="a7bcc-124">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-124">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7bcc-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7bcc-125">-NetworkWatcher</span></span>
<span data-ttu-id="a7bcc-126">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="a7bcc-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="a7bcc-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="a7bcc-128">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a7bcc-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a7bcc-129">-NetworkWatcherName</span></span>
<span data-ttu-id="a7bcc-130">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7bcc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7bcc-131">-ResourceGroupName</span></span>
<span data-ttu-id="a7bcc-132">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a7bcc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7bcc-133">-ResourceId</span></span>
<span data-ttu-id="a7bcc-134">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="a7bcc-135">-State</span><span class="sxs-lookup"><span data-stu-id="a7bcc-135">-State</span></span>
<span data-ttu-id="a7bcc-136">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-136">The name of the state.</span></span>

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

### <span data-ttu-id="a7bcc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bcc-137">CommonParameters</span></span>
<span data-ttu-id="a7bcc-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7bcc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bcc-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7bcc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bcc-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7bcc-140">INPUTS</span></span>

### <span data-ttu-id="a7bcc-141">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7bcc-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a7bcc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a7bcc-142">System.String</span></span>

## <span data-ttu-id="a7bcc-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7bcc-143">OUTPUTS</span></span>

### <span data-ttu-id="a7bcc-144">Microsoft. Azure. commands. Networks. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="a7bcc-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="a7bcc-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7bcc-145">NOTES</span></span>
<span data-ttu-id="a7bcc-146">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="a7bcc-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="a7bcc-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7bcc-147">RELATED LINKS</span></span>

[<span data-ttu-id="a7bcc-148">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7bcc-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a7bcc-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7bcc-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a7bcc-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7bcc-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a7bcc-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a7bcc-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a7bcc-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a7bcc-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a7bcc-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a7bcc-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a7bcc-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a7bcc-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a7bcc-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7bcc-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7bcc-156">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a7bcc-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a7bcc-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7bcc-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7bcc-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7bcc-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7bcc-159">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7bcc-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7bcc-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7bcc-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a7bcc-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a7bcc-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a7bcc-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a7bcc-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a7bcc-163">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7bcc-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7bcc-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7bcc-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7bcc-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7bcc-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7bcc-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a7bcc-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a7bcc-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7bcc-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7bcc-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7bcc-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a7bcc-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a7bcc-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a7bcc-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a7bcc-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a7bcc-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a7bcc-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a7bcc-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a7bcc-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a7bcc-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a7bcc-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="a7bcc-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a7bcc-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
