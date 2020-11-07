---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: cf35292be5005a957e245370a5b15b78bb7d4fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918461"
---
# <span data-ttu-id="3fd7c-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3fd7c-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="3fd7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd7c-103">Här listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="3fd7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fd7c-104">SYNTAX</span></span>

### <span data-ttu-id="3fd7c-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="3fd7c-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fd7c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3fd7c-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3fd7c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3fd7c-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3fd7c-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3fd7c-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fd7c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fd7c-109">DESCRIPTION</span></span>
<span data-ttu-id="3fd7c-110">I Get-AzNetworkWatcherReachabilityProvidersList listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="3fd7c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fd7c-111">EXAMPLES</span></span>

### <span data-ttu-id="3fd7c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3fd7c-112">Example 1</span></span>
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

<span data-ttu-id="3fd7c-113">Här listas alla tillgängliga providrar i Seattle, WA för Azure Data Center i västra USA.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="3fd7c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fd7c-114">PARAMETERS</span></span>

### <span data-ttu-id="3fd7c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fd7c-115">-AsJob</span></span>
<span data-ttu-id="3fd7c-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3fd7c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fd7c-117">-Ort</span><span class="sxs-lookup"><span data-stu-id="3fd7c-117">-City</span></span>
<span data-ttu-id="3fd7c-118">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-118">The name of the city.</span></span>

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

### <span data-ttu-id="3fd7c-119">-Country</span><span class="sxs-lookup"><span data-stu-id="3fd7c-119">-Country</span></span>
<span data-ttu-id="3fd7c-120">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-120">The name of the country.</span></span>

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

### <span data-ttu-id="3fd7c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd7c-121">-DefaultProfile</span></span>
<span data-ttu-id="3fd7c-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fd7c-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="3fd7c-123">-Location</span></span>
<span data-ttu-id="3fd7c-124">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="3fd7c-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fd7c-125">-NetworkWatcher</span></span>
<span data-ttu-id="3fd7c-126">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="3fd7c-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="3fd7c-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="3fd7c-128">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3fd7c-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3fd7c-129">-NetworkWatcherName</span></span>
<span data-ttu-id="3fd7c-130">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="3fd7c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd7c-131">-ResourceGroupName</span></span>
<span data-ttu-id="3fd7c-132">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3fd7c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fd7c-133">-ResourceId</span></span>
<span data-ttu-id="3fd7c-134">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="3fd7c-135">-State</span><span class="sxs-lookup"><span data-stu-id="3fd7c-135">-State</span></span>
<span data-ttu-id="3fd7c-136">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-136">The name of the state.</span></span>

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

### <span data-ttu-id="3fd7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd7c-137">CommonParameters</span></span>
<span data-ttu-id="3fd7c-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd7c-139">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fd7c-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd7c-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fd7c-140">INPUTS</span></span>

### <span data-ttu-id="3fd7c-141">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fd7c-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3fd7c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3fd7c-142">System.String</span></span>

## <span data-ttu-id="3fd7c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fd7c-143">OUTPUTS</span></span>

### <span data-ttu-id="3fd7c-144">Microsoft. Azure. commands. Networks. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="3fd7c-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="3fd7c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fd7c-145">NOTES</span></span>
<span data-ttu-id="3fd7c-146">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="3fd7c-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="3fd7c-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fd7c-147">RELATED LINKS</span></span>

[<span data-ttu-id="3fd7c-148">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fd7c-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3fd7c-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fd7c-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3fd7c-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3fd7c-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3fd7c-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3fd7c-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3fd7c-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3fd7c-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3fd7c-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3fd7c-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3fd7c-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3fd7c-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3fd7c-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fd7c-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fd7c-156">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3fd7c-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3fd7c-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fd7c-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fd7c-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fd7c-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fd7c-159">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3fd7c-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3fd7c-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fd7c-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3fd7c-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3fd7c-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3fd7c-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3fd7c-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3fd7c-163">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fd7c-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fd7c-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fd7c-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fd7c-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fd7c-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fd7c-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3fd7c-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3fd7c-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fd7c-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fd7c-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fd7c-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3fd7c-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3fd7c-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3fd7c-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3fd7c-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3fd7c-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3fd7c-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3fd7c-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3fd7c-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3fd7c-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3fd7c-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="3fd7c-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3fd7c-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
