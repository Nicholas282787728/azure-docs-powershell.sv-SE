---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: e1e0714c070c47d4be2cff0893a4428bdf0949c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757666"
---
# <span data-ttu-id="ba5b1-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba5b1-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="ba5b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5b1-103">Skapar en ny resurs för nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba5b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba5b1-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba5b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba5b1-105">DESCRIPTION</span></span>
<span data-ttu-id="ba5b1-106">New-AzureRmNetworkWatcher-cmdleten skapar en ny nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="ba5b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba5b1-107">EXAMPLES</span></span>

### <span data-ttu-id="ba5b1-108">Exempel 1: skapa en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="ba5b1-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="ba5b1-109">I det här exemplet skapas en ny nätverks bevakning i en nyligen skapad resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="ba5b1-110">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="ba5b1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba5b1-111">PARAMETERS</span></span>

### <span data-ttu-id="ba5b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5b1-112">-DefaultProfile</span></span>
<span data-ttu-id="ba5b1-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba5b1-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="ba5b1-114">-Location</span></span>
<span data-ttu-id="ba5b1-115">Plats.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-115">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5b1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba5b1-116">-Name</span></span>
<span data-ttu-id="ba5b1-117">Namnet på nät övervakaren.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-117">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5b1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba5b1-118">-ResourceGroupName</span></span>
<span data-ttu-id="ba5b1-119">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5b1-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ba5b1-120">-Tag</span></span>
<span data-ttu-id="ba5b1-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ba5b1-122">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="ba5b1-122">For example:</span></span>

<span data-ttu-id="ba5b1-123">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="ba5b1-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5b1-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ba5b1-124">-Confirm</span></span>
<span data-ttu-id="ba5b1-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5b1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba5b1-126">-WhatIf</span></span>
<span data-ttu-id="ba5b1-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba5b1-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5b1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5b1-129">CommonParameters</span></span>
<span data-ttu-id="ba5b1-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba5b1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5b1-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5b1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5b1-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba5b1-132">INPUTS</span></span>

### <span data-ttu-id="ba5b1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ba5b1-133">System.String</span></span>
<span data-ttu-id="ba5b1-134">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ba5b1-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ba5b1-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba5b1-135">OUTPUTS</span></span>

### <span data-ttu-id="ba5b1-136">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba5b1-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="ba5b1-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba5b1-137">NOTES</span></span>
<span data-ttu-id="ba5b1-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="ba5b1-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="ba5b1-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba5b1-139">RELATED LINKS</span></span>

[<span data-ttu-id="ba5b1-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba5b1-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ba5b1-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba5b1-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ba5b1-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba5b1-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba5b1-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ba5b1-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ba5b1-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba5b1-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba5b1-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba5b1-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba5b1-146">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba5b1-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba5b1-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ba5b1-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ba5b1-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ba5b1-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ba5b1-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ba5b1-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ba5b1-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ba5b1-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ba5b1-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ba5b1-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
