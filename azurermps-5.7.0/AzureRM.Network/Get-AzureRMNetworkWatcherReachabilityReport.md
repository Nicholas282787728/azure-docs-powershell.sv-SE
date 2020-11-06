---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 7ec4ebbe9e1224e47605a35f7f21feb2dfbcf045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580363"
---
# <span data-ttu-id="97b4b-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="97b4b-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="97b4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="97b4b-103">Hämtar den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="97b4b-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97b4b-104">SYNTAX</span></span>

### <span data-ttu-id="97b4b-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="97b4b-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97b4b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="97b4b-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97b4b-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="97b4b-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97b4b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97b4b-108">DESCRIPTION</span></span>
<span data-ttu-id="97b4b-109">Get-AzureRmNetworkWatcherReachabilityReport får den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="97b4b-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="97b4b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97b4b-110">EXAMPLES</span></span>

### <span data-ttu-id="97b4b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="97b4b-111">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="97b4b-112">Hämtar relativa fördröjningar till Azure Data Center i väster från 2017-10-10 till 2017-10-12 i USA.</span><span class="sxs-lookup"><span data-stu-id="97b4b-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="97b4b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97b4b-113">PARAMETERS</span></span>

### <span data-ttu-id="97b4b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97b4b-114">-AsJob</span></span>
<span data-ttu-id="97b4b-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="97b4b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97b4b-116">-Ort</span><span class="sxs-lookup"><span data-stu-id="97b4b-116">-City</span></span>
<span data-ttu-id="97b4b-117">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="97b4b-117">The name of the city.</span></span>

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

### <span data-ttu-id="97b4b-118">-Country</span><span class="sxs-lookup"><span data-stu-id="97b4b-118">-Country</span></span>
<span data-ttu-id="97b4b-119">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="97b4b-119">The name of the country.</span></span>

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

### <span data-ttu-id="97b4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b4b-120">-DefaultProfile</span></span>
<span data-ttu-id="97b4b-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97b4b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97b4b-122">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="97b4b-122">-EndTime</span></span>
<span data-ttu-id="97b4b-123">Slut tiden för Azure REACH-rapporten.</span><span class="sxs-lookup"><span data-stu-id="97b4b-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="97b4b-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="97b4b-124">-Location</span></span>
<span data-ttu-id="97b4b-125">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="97b4b-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="97b4b-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97b4b-126">-NetworkWatcher</span></span>
<span data-ttu-id="97b4b-127">Nätverks Watcher-resursen</span><span class="sxs-lookup"><span data-stu-id="97b4b-127">The network watcher resource</span></span>

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

### <span data-ttu-id="97b4b-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="97b4b-128">-NetworkWatcherName</span></span>
<span data-ttu-id="97b4b-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="97b4b-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="97b4b-130">-Leverantör</span><span class="sxs-lookup"><span data-stu-id="97b4b-130">-Provider</span></span>
<span data-ttu-id="97b4b-131">Lista över Internet leverantörer.</span><span class="sxs-lookup"><span data-stu-id="97b4b-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="97b4b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b4b-132">-ResourceGroupName</span></span>
<span data-ttu-id="97b4b-133">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="97b4b-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="97b4b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97b4b-134">-ResourceId</span></span>
<span data-ttu-id="97b4b-135">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="97b4b-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="97b4b-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="97b4b-136">-StartTime</span></span>
<span data-ttu-id="97b4b-137">Start tiden för rapporten för Azure-tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="97b4b-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="97b4b-138">-State</span><span class="sxs-lookup"><span data-stu-id="97b4b-138">-State</span></span>
<span data-ttu-id="97b4b-139">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="97b4b-139">The name of the state.</span></span>

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

### <span data-ttu-id="97b4b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b4b-140">CommonParameters</span></span>
<span data-ttu-id="97b4b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b4b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b4b-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b4b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b4b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97b4b-143">INPUTS</span></span>

### <span data-ttu-id="97b4b-144">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97b4b-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="97b4b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="97b4b-145">System.String</span></span>

## <span data-ttu-id="97b4b-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97b4b-146">OUTPUTS</span></span>

### <span data-ttu-id="97b4b-147">Microsoft. Azure. commands. Networks. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="97b4b-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="97b4b-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97b4b-148">NOTES</span></span>
<span data-ttu-id="97b4b-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, tillgänglighet, rapport</span><span class="sxs-lookup"><span data-stu-id="97b4b-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="97b4b-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97b4b-150">RELATED LINKS</span></span>

[<span data-ttu-id="97b4b-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97b4b-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="97b4b-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97b4b-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="97b4b-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97b4b-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="97b4b-154">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="97b4b-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="97b4b-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="97b4b-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="97b4b-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="97b4b-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="97b4b-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="97b4b-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="97b4b-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="97b4b-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="97b4b-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="97b4b-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="97b4b-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="97b4b-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="97b4b-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="97b4b-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="97b4b-162">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="97b4b-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
