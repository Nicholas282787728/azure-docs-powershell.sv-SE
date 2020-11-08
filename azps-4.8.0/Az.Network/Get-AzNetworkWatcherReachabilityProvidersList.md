---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a4e9c9a928d3a6c3ddeb7afa754cc957089a2283
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258798"
---
# <span data-ttu-id="04bbc-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="04bbc-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="04bbc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="04bbc-103">Här listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="04bbc-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="04bbc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04bbc-104">SYNTAX</span></span>

### <span data-ttu-id="04bbc-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="04bbc-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04bbc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="04bbc-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04bbc-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="04bbc-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04bbc-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="04bbc-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04bbc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04bbc-109">DESCRIPTION</span></span>
<span data-ttu-id="04bbc-110">I Get-AzNetworkWatcherReachabilityProvidersList listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="04bbc-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="04bbc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04bbc-111">EXAMPLES</span></span>

### <span data-ttu-id="04bbc-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="04bbc-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="04bbc-113">Här listas alla tillgängliga providrar i Seattle, WA för Azure Data Center i västra USA.</span><span class="sxs-lookup"><span data-stu-id="04bbc-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="04bbc-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="04bbc-114">Example 2</span></span>

<span data-ttu-id="04bbc-115">Här listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="04bbc-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="04bbc-116">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="04bbc-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="04bbc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04bbc-117">PARAMETERS</span></span>

### <span data-ttu-id="04bbc-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04bbc-118">-AsJob</span></span>
<span data-ttu-id="04bbc-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="04bbc-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04bbc-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="04bbc-120">-City</span></span>
<span data-ttu-id="04bbc-121">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="04bbc-121">The name of the city.</span></span>

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

### <span data-ttu-id="04bbc-122">-Country</span><span class="sxs-lookup"><span data-stu-id="04bbc-122">-Country</span></span>
<span data-ttu-id="04bbc-123">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="04bbc-123">The name of the country.</span></span>

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

### <span data-ttu-id="04bbc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04bbc-124">-DefaultProfile</span></span>
<span data-ttu-id="04bbc-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04bbc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04bbc-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="04bbc-126">-Location</span></span>
<span data-ttu-id="04bbc-127">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="04bbc-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="04bbc-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04bbc-128">-NetworkWatcher</span></span>
<span data-ttu-id="04bbc-129">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="04bbc-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="04bbc-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="04bbc-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="04bbc-131">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="04bbc-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="04bbc-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="04bbc-132">-NetworkWatcherName</span></span>
<span data-ttu-id="04bbc-133">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="04bbc-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="04bbc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04bbc-134">-ResourceGroupName</span></span>
<span data-ttu-id="04bbc-135">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="04bbc-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="04bbc-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04bbc-136">-ResourceId</span></span>
<span data-ttu-id="04bbc-137">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="04bbc-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="04bbc-138">-State</span><span class="sxs-lookup"><span data-stu-id="04bbc-138">-State</span></span>
<span data-ttu-id="04bbc-139">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="04bbc-139">The name of the state.</span></span>

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

### <span data-ttu-id="04bbc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04bbc-140">CommonParameters</span></span>
<span data-ttu-id="04bbc-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04bbc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04bbc-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04bbc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04bbc-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04bbc-143">INPUTS</span></span>

### <span data-ttu-id="04bbc-144">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04bbc-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="04bbc-145">System. String</span><span class="sxs-lookup"><span data-stu-id="04bbc-145">System.String</span></span>

## <span data-ttu-id="04bbc-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04bbc-146">OUTPUTS</span></span>

### <span data-ttu-id="04bbc-147">Microsoft. Azure. commands. Networks. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="04bbc-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="04bbc-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04bbc-148">NOTES</span></span>
<span data-ttu-id="04bbc-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="04bbc-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="04bbc-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04bbc-150">RELATED LINKS</span></span>

[<span data-ttu-id="04bbc-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04bbc-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="04bbc-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04bbc-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="04bbc-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="04bbc-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="04bbc-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="04bbc-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="04bbc-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="04bbc-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="04bbc-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="04bbc-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="04bbc-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="04bbc-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="04bbc-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="04bbc-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="04bbc-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="04bbc-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="04bbc-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="04bbc-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="04bbc-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="04bbc-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="04bbc-162">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="04bbc-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="04bbc-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="04bbc-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="04bbc-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="04bbc-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="04bbc-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="04bbc-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="04bbc-166">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04bbc-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04bbc-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04bbc-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04bbc-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04bbc-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04bbc-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="04bbc-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="04bbc-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04bbc-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04bbc-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04bbc-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="04bbc-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="04bbc-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="04bbc-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="04bbc-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="04bbc-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="04bbc-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="04bbc-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="04bbc-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="04bbc-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="04bbc-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="04bbc-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="04bbc-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
