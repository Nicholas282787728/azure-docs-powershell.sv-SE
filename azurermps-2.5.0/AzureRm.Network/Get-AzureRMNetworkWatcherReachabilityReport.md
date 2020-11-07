---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
ms.openlocfilehash: 75335fb09bb8f4187879ab69ab138952cc873993
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931349"
---
# <span data-ttu-id="2f90c-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2f90c-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="2f90c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f90c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f90c-103">Hämtar den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="2f90c-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f90c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f90c-104">SYNTAX</span></span>

### <span data-ttu-id="2f90c-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="2f90c-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f90c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2f90c-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f90c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f90c-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f90c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f90c-108">DESCRIPTION</span></span>
<span data-ttu-id="2f90c-109">Get-AzureRmNetworkWatcherReachabilityReport får den relativa fördröjnings poängen för Internet leverantör från en angiven plats till Azure-regioner.</span><span class="sxs-lookup"><span data-stu-id="2f90c-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="2f90c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f90c-110">EXAMPLES</span></span>

### <span data-ttu-id="2f90c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2f90c-111">Example 1</span></span>
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

<span data-ttu-id="2f90c-112">Hämtar relativa fördröjningar till Azure Data Center i väster från 2017-10-10 till 2017-10-12 i USA.</span><span class="sxs-lookup"><span data-stu-id="2f90c-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="2f90c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f90c-113">PARAMETERS</span></span>

### <span data-ttu-id="2f90c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f90c-114">-AsJob</span></span>
<span data-ttu-id="2f90c-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2f90c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f90c-116">-Ort</span><span class="sxs-lookup"><span data-stu-id="2f90c-116">-City</span></span>
<span data-ttu-id="2f90c-117">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="2f90c-117">The name of the city.</span></span>

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

### <span data-ttu-id="2f90c-118">-Country</span><span class="sxs-lookup"><span data-stu-id="2f90c-118">-Country</span></span>
<span data-ttu-id="2f90c-119">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="2f90c-119">The name of the country.</span></span>

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

### <span data-ttu-id="2f90c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f90c-120">-DefaultProfile</span></span>
<span data-ttu-id="2f90c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f90c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f90c-122">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="2f90c-122">-EndTime</span></span>
<span data-ttu-id="2f90c-123">Slut tiden för Azure REACH-rapporten.</span><span class="sxs-lookup"><span data-stu-id="2f90c-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="2f90c-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="2f90c-124">-Location</span></span>
<span data-ttu-id="2f90c-125">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="2f90c-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="2f90c-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f90c-126">-NetworkWatcher</span></span>
<span data-ttu-id="2f90c-127">Nätverks Watcher-resursen</span><span class="sxs-lookup"><span data-stu-id="2f90c-127">The network watcher resource</span></span>

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

### <span data-ttu-id="2f90c-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2f90c-128">-NetworkWatcherName</span></span>
<span data-ttu-id="2f90c-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="2f90c-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="2f90c-130">-Leverantör</span><span class="sxs-lookup"><span data-stu-id="2f90c-130">-Provider</span></span>
<span data-ttu-id="2f90c-131">Lista över Internet leverantörer.</span><span class="sxs-lookup"><span data-stu-id="2f90c-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="2f90c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f90c-132">-ResourceGroupName</span></span>
<span data-ttu-id="2f90c-133">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2f90c-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2f90c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f90c-134">-ResourceId</span></span>
<span data-ttu-id="2f90c-135">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="2f90c-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="2f90c-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2f90c-136">-StartTime</span></span>
<span data-ttu-id="2f90c-137">Start tiden för rapporten för Azure-tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="2f90c-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="2f90c-138">-State</span><span class="sxs-lookup"><span data-stu-id="2f90c-138">-State</span></span>
<span data-ttu-id="2f90c-139">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="2f90c-139">The name of the state.</span></span>

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

### <span data-ttu-id="2f90c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f90c-140">CommonParameters</span></span>
<span data-ttu-id="2f90c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f90c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f90c-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f90c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f90c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f90c-143">INPUTS</span></span>

### <span data-ttu-id="2f90c-144">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f90c-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2f90c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2f90c-145">System.String</span></span>

## <span data-ttu-id="2f90c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f90c-146">OUTPUTS</span></span>

### <span data-ttu-id="2f90c-147">Microsoft. Azure. commands. Networks. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2f90c-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="2f90c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f90c-148">NOTES</span></span>
<span data-ttu-id="2f90c-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, tillgänglighet, rapport</span><span class="sxs-lookup"><span data-stu-id="2f90c-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="2f90c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f90c-150">RELATED LINKS</span></span>

[<span data-ttu-id="2f90c-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f90c-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2f90c-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f90c-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2f90c-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f90c-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2f90c-154">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2f90c-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2f90c-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2f90c-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2f90c-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2f90c-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2f90c-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2f90c-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2f90c-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f90c-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f90c-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2f90c-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2f90c-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f90c-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f90c-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f90c-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f90c-162">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f90c-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
