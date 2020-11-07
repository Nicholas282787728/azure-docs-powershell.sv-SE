---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 093a847154c75ee7c640bda522ebf16baa04560a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758215"
---
# <span data-ttu-id="4618e-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4618e-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="4618e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4618e-102">SYNOPSIS</span></span>
<span data-ttu-id="4618e-103">Här listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="4618e-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4618e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4618e-104">SYNTAX</span></span>

### <span data-ttu-id="4618e-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="4618e-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4618e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4618e-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4618e-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4618e-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4618e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4618e-108">DESCRIPTION</span></span>
<span data-ttu-id="4618e-109">I Get-AzureRmNetworkWatcherReachabilityProvidersList listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="4618e-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="4618e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4618e-110">EXAMPLES</span></span>

### <span data-ttu-id="4618e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4618e-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="4618e-112">Här listas alla tillgängliga providrar i Seattle, WA för Azure Data Center i västra USA.</span><span class="sxs-lookup"><span data-stu-id="4618e-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="4618e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4618e-113">PARAMETERS</span></span>

### <span data-ttu-id="4618e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4618e-114">-AsJob</span></span>
<span data-ttu-id="4618e-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4618e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4618e-116">-Ort</span><span class="sxs-lookup"><span data-stu-id="4618e-116">-City</span></span>
<span data-ttu-id="4618e-117">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="4618e-117">The name of the city.</span></span>

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

### <span data-ttu-id="4618e-118">-Country</span><span class="sxs-lookup"><span data-stu-id="4618e-118">-Country</span></span>
<span data-ttu-id="4618e-119">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="4618e-119">The name of the country.</span></span>

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

### <span data-ttu-id="4618e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4618e-120">-DefaultProfile</span></span>
<span data-ttu-id="4618e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4618e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4618e-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="4618e-122">-Location</span></span>
<span data-ttu-id="4618e-123">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="4618e-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="4618e-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4618e-124">-NetworkWatcher</span></span>
<span data-ttu-id="4618e-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="4618e-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="4618e-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4618e-126">-NetworkWatcherName</span></span>
<span data-ttu-id="4618e-127">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="4618e-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="4618e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4618e-128">-ResourceGroupName</span></span>
<span data-ttu-id="4618e-129">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4618e-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4618e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4618e-130">-ResourceId</span></span>
<span data-ttu-id="4618e-131">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="4618e-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="4618e-132">-State</span><span class="sxs-lookup"><span data-stu-id="4618e-132">-State</span></span>
<span data-ttu-id="4618e-133">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="4618e-133">The name of the state.</span></span>

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

### <span data-ttu-id="4618e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4618e-134">CommonParameters</span></span>
<span data-ttu-id="4618e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4618e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4618e-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4618e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4618e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4618e-137">INPUTS</span></span>

### <span data-ttu-id="4618e-138">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4618e-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4618e-139">System. String system. Collections. Genered. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4618e-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4618e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4618e-140">OUTPUTS</span></span>

### <span data-ttu-id="4618e-141">Microsoft. Azure. commands. Networks. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="4618e-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="4618e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4618e-142">NOTES</span></span>
<span data-ttu-id="4618e-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="4618e-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="4618e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4618e-144">RELATED LINKS</span></span>

[<span data-ttu-id="4618e-145">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4618e-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4618e-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4618e-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4618e-147">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4618e-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4618e-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4618e-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4618e-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4618e-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4618e-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4618e-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4618e-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4618e-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4618e-152">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4618e-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4618e-153">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4618e-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4618e-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4618e-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4618e-155">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4618e-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4618e-156">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4618e-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
