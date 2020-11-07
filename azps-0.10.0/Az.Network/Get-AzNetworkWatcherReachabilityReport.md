---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922239"
---
# <span data-ttu-id="9b516-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9b516-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="9b516-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b516-102">SYNOPSIS</span></span>
<span data-ttu-id="9b516-103">Hämtar den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="9b516-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="9b516-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b516-104">SYNTAX</span></span>

### <span data-ttu-id="9b516-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="9b516-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b516-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9b516-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b516-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b516-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b516-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b516-108">DESCRIPTION</span></span>
<span data-ttu-id="9b516-109">Get-AzNetworkWatcherReachabilityReport får den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="9b516-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="9b516-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b516-110">EXAMPLES</span></span>

### <span data-ttu-id="9b516-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b516-111">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="9b516-112">Hämtar relativa fördröjningar till Azure Data Center i väster från 2017-10-10 till 2017-10-12 i USA.</span><span class="sxs-lookup"><span data-stu-id="9b516-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="9b516-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b516-113">PARAMETERS</span></span>

### <span data-ttu-id="9b516-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b516-114">-AsJob</span></span>
<span data-ttu-id="9b516-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9b516-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-116">-Ort</span><span class="sxs-lookup"><span data-stu-id="9b516-116">-City</span></span>
<span data-ttu-id="9b516-117">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="9b516-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-118">-Country</span><span class="sxs-lookup"><span data-stu-id="9b516-118">-Country</span></span>
<span data-ttu-id="9b516-119">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="9b516-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b516-120">-DefaultProfile</span></span>
<span data-ttu-id="9b516-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b516-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-122">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="9b516-122">-EndTime</span></span>
<span data-ttu-id="9b516-123">Slut tiden för Azure REACH-rapporten.</span><span class="sxs-lookup"><span data-stu-id="9b516-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="9b516-124">-Location</span></span>
<span data-ttu-id="9b516-125">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="9b516-125">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b516-126">-NetworkWatcher</span></span>
<span data-ttu-id="9b516-127">Nätverks Watcher-resursen</span><span class="sxs-lookup"><span data-stu-id="9b516-127">The network watcher resource</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9b516-128">-NetworkWatcherName</span></span>
<span data-ttu-id="9b516-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="9b516-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-130">-Leverantör</span><span class="sxs-lookup"><span data-stu-id="9b516-130">-Provider</span></span>
<span data-ttu-id="9b516-131">Lista över Internet leverantörer.</span><span class="sxs-lookup"><span data-stu-id="9b516-131">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b516-132">-ResourceGroupName</span></span>
<span data-ttu-id="9b516-133">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9b516-133">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b516-134">-ResourceId</span></span>
<span data-ttu-id="9b516-135">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="9b516-135">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9b516-136">-StartTime</span></span>
<span data-ttu-id="9b516-137">Start tiden för rapporten för Azure-tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="9b516-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-138">-State</span><span class="sxs-lookup"><span data-stu-id="9b516-138">-State</span></span>
<span data-ttu-id="9b516-139">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="9b516-139">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b516-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b516-140">CommonParameters</span></span>
<span data-ttu-id="9b516-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b516-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b516-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b516-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b516-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b516-143">INPUTS</span></span>

### <span data-ttu-id="9b516-144">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b516-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9b516-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9b516-145">System.String</span></span>

## <span data-ttu-id="9b516-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b516-146">OUTPUTS</span></span>

### <span data-ttu-id="9b516-147">Microsoft. Azure. commands. Networks. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9b516-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="9b516-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b516-148">NOTES</span></span>
<span data-ttu-id="9b516-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, tillgänglighet, rapport</span><span class="sxs-lookup"><span data-stu-id="9b516-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="9b516-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b516-150">RELATED LINKS</span></span>

[<span data-ttu-id="9b516-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b516-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9b516-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b516-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9b516-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b516-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9b516-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9b516-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9b516-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9b516-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9b516-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9b516-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9b516-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9b516-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9b516-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b516-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b516-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9b516-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9b516-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b516-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b516-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b516-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b516-162">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b516-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
