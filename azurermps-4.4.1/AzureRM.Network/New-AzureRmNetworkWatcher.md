---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: 10cc869bf6e0ac194ce5e2e77c69885a8e0a0d25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576000"
---
# <span data-ttu-id="5e47e-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e47e-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="5e47e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e47e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e47e-103">Skapar en ny resurs för nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="5e47e-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e47e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e47e-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e47e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e47e-105">DESCRIPTION</span></span>
<span data-ttu-id="5e47e-106">New-AzureRmNetworkWatcher-cmdleten skapar en ny nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="5e47e-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="5e47e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e47e-107">EXAMPLES</span></span>

### <span data-ttu-id="5e47e-108">Exempel 1: skapa en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="5e47e-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="5e47e-109">I det här exemplet skapas en ny nätverks bevakning i en nyligen skapad resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5e47e-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="5e47e-110">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5e47e-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="5e47e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e47e-111">PARAMETERS</span></span>

### <span data-ttu-id="5e47e-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="5e47e-112">-Location</span></span>
<span data-ttu-id="5e47e-113">Plats.</span><span class="sxs-lookup"><span data-stu-id="5e47e-113">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e47e-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e47e-114">-Name</span></span>
<span data-ttu-id="5e47e-115">Namnet på nät övervakaren.</span><span class="sxs-lookup"><span data-stu-id="5e47e-115">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e47e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e47e-116">-ResourceGroupName</span></span>
<span data-ttu-id="5e47e-117">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5e47e-117">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e47e-118">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5e47e-118">-Tag</span></span>
<span data-ttu-id="5e47e-119">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5e47e-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5e47e-120">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="5e47e-120">For example:</span></span>

<span data-ttu-id="5e47e-121">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="5e47e-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e47e-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e47e-122">-Confirm</span></span>
<span data-ttu-id="5e47e-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e47e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e47e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e47e-124">-WhatIf</span></span>
<span data-ttu-id="5e47e-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e47e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e47e-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e47e-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e47e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e47e-127">-DefaultProfile</span></span>
<span data-ttu-id="5e47e-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e47e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e47e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e47e-129">CommonParameters</span></span>
<span data-ttu-id="5e47e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e47e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e47e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e47e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e47e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e47e-132">INPUTS</span></span>

### <span data-ttu-id="5e47e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5e47e-133">System.String</span></span>
<span data-ttu-id="5e47e-134">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5e47e-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5e47e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e47e-135">OUTPUTS</span></span>

### <span data-ttu-id="5e47e-136">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e47e-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="5e47e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e47e-137">NOTES</span></span>
<span data-ttu-id="5e47e-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="5e47e-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="5e47e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e47e-139">RELATED LINKS</span></span>

[<span data-ttu-id="5e47e-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e47e-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e47e-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e47e-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e47e-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e47e-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e47e-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5e47e-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5e47e-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e47e-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e47e-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e47e-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e47e-146">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e47e-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e47e-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5e47e-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5e47e-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5e47e-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5e47e-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5e47e-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5e47e-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5e47e-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5e47e-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5e47e-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
