---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922241"
---
# <span data-ttu-id="40df0-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="40df0-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="40df0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40df0-102">SYNOPSIS</span></span>
<span data-ttu-id="40df0-103">Här listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="40df0-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="40df0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40df0-104">SYNTAX</span></span>

### <span data-ttu-id="40df0-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="40df0-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40df0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="40df0-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40df0-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="40df0-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40df0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40df0-108">DESCRIPTION</span></span>
<span data-ttu-id="40df0-109">I Get-AzNetworkWatcherReachabilityProvidersList listas alla tillgängliga Internet leverantörer för ett angivet Azure-område.</span><span class="sxs-lookup"><span data-stu-id="40df0-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="40df0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40df0-110">EXAMPLES</span></span>

### <span data-ttu-id="40df0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40df0-111">Example 1</span></span>
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

<span data-ttu-id="40df0-112">Här listas alla tillgängliga providrar i Seattle, WA för Azure Data Center i västra USA.</span><span class="sxs-lookup"><span data-stu-id="40df0-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="40df0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40df0-113">PARAMETERS</span></span>

### <span data-ttu-id="40df0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40df0-114">-AsJob</span></span>
<span data-ttu-id="40df0-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="40df0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40df0-116">-Ort</span><span class="sxs-lookup"><span data-stu-id="40df0-116">-City</span></span>
<span data-ttu-id="40df0-117">Namnet på staden.</span><span class="sxs-lookup"><span data-stu-id="40df0-117">The name of the city.</span></span>

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

### <span data-ttu-id="40df0-118">-Country</span><span class="sxs-lookup"><span data-stu-id="40df0-118">-Country</span></span>
<span data-ttu-id="40df0-119">Landets namn.</span><span class="sxs-lookup"><span data-stu-id="40df0-119">The name of the country.</span></span>

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

### <span data-ttu-id="40df0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40df0-120">-DefaultProfile</span></span>
<span data-ttu-id="40df0-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40df0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40df0-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="40df0-122">-Location</span></span>
<span data-ttu-id="40df0-123">Valfria Azure-regioner som frågan ska beställas till.</span><span class="sxs-lookup"><span data-stu-id="40df0-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="40df0-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40df0-124">-NetworkWatcher</span></span>
<span data-ttu-id="40df0-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="40df0-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="40df0-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="40df0-126">-NetworkWatcherName</span></span>
<span data-ttu-id="40df0-127">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="40df0-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="40df0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40df0-128">-ResourceGroupName</span></span>
<span data-ttu-id="40df0-129">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="40df0-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="40df0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40df0-130">-ResourceId</span></span>
<span data-ttu-id="40df0-131">ID för nätverks Watch-resursen.</span><span class="sxs-lookup"><span data-stu-id="40df0-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="40df0-132">-State</span><span class="sxs-lookup"><span data-stu-id="40df0-132">-State</span></span>
<span data-ttu-id="40df0-133">Namnet på tillståndet.</span><span class="sxs-lookup"><span data-stu-id="40df0-133">The name of the state.</span></span>

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

### <span data-ttu-id="40df0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40df0-134">CommonParameters</span></span>
<span data-ttu-id="40df0-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40df0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40df0-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40df0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40df0-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40df0-137">INPUTS</span></span>

### <span data-ttu-id="40df0-138">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40df0-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="40df0-139">System. String system. Collections. Genered. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="40df0-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="40df0-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40df0-140">OUTPUTS</span></span>

### <span data-ttu-id="40df0-141">Microsoft. Azure. commands. Networks. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="40df0-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="40df0-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40df0-142">NOTES</span></span>
<span data-ttu-id="40df0-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, nästa, hopp</span><span class="sxs-lookup"><span data-stu-id="40df0-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="40df0-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40df0-144">RELATED LINKS</span></span>

[<span data-ttu-id="40df0-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40df0-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="40df0-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40df0-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="40df0-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40df0-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="40df0-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="40df0-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="40df0-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="40df0-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="40df0-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="40df0-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="40df0-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="40df0-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="40df0-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40df0-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40df0-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="40df0-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="40df0-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40df0-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40df0-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40df0-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40df0-156">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40df0-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
