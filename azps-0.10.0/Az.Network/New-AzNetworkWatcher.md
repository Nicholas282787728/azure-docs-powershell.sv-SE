---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922107"
---
# <span data-ttu-id="b2e5b-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2e5b-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="b2e5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e5b-103">Skapar en ny resurs för nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="b2e5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2e5b-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e5b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2e5b-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e5b-106">New-AzNetworkWatcher-cmdleten skapar en ny nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="b2e5b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2e5b-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e5b-108">Exempel 1: skapa en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="b2e5b-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="b2e5b-109">I det här exemplet skapas en ny nätverks bevakning i en nyligen skapad resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="b2e5b-110">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="b2e5b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2e5b-111">PARAMETERS</span></span>

### <span data-ttu-id="b2e5b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e5b-112">-DefaultProfile</span></span>
<span data-ttu-id="b2e5b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2e5b-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="b2e5b-114">-Location</span></span>
<span data-ttu-id="b2e5b-115">Plats.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-115">Location.</span></span>

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

### <span data-ttu-id="b2e5b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2e5b-116">-Name</span></span>
<span data-ttu-id="b2e5b-117">Namnet på nät övervakaren.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-117">The network watcher name.</span></span>

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

### <span data-ttu-id="b2e5b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e5b-118">-ResourceGroupName</span></span>
<span data-ttu-id="b2e5b-119">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-119">The resource group name.</span></span>

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

### <span data-ttu-id="b2e5b-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b2e5b-120">-Tag</span></span>
<span data-ttu-id="b2e5b-121">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b2e5b-122">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="b2e5b-122">For example:</span></span>

<span data-ttu-id="b2e5b-123">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b2e5b-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b2e5b-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2e5b-124">-Confirm</span></span>
<span data-ttu-id="b2e5b-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e5b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e5b-126">-WhatIf</span></span>
<span data-ttu-id="b2e5b-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e5b-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e5b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e5b-129">CommonParameters</span></span>
<span data-ttu-id="b2e5b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e5b-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e5b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e5b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2e5b-132">INPUTS</span></span>

### <span data-ttu-id="b2e5b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e5b-133">System.String</span></span>
<span data-ttu-id="b2e5b-134">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b2e5b-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b2e5b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2e5b-135">OUTPUTS</span></span>

### <span data-ttu-id="b2e5b-136">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2e5b-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="b2e5b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2e5b-137">NOTES</span></span>
<span data-ttu-id="b2e5b-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="b2e5b-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="b2e5b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2e5b-139">RELATED LINKS</span></span>

[<span data-ttu-id="b2e5b-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2e5b-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b2e5b-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2e5b-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b2e5b-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2e5b-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2e5b-143">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b2e5b-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b2e5b-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2e5b-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2e5b-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2e5b-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2e5b-146">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2e5b-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2e5b-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b2e5b-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b2e5b-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b2e5b-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b2e5b-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b2e5b-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b2e5b-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b2e5b-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b2e5b-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b2e5b-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
