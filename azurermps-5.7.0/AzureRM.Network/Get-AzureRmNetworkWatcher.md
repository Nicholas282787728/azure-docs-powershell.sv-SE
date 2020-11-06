---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: 9df0d0855ca22e9ea7141a99c69c8b44f16f489d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586040"
---
# <span data-ttu-id="26b1c-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26b1c-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="26b1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="26b1c-103">Hämtar egenskaperna för en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="26b1c-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26b1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26b1c-104">SYNTAX</span></span>

### <span data-ttu-id="26b1c-105">Lära</span><span class="sxs-lookup"><span data-stu-id="26b1c-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26b1c-106">Förteckning</span><span class="sxs-lookup"><span data-stu-id="26b1c-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26b1c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26b1c-107">DESCRIPTION</span></span>
<span data-ttu-id="26b1c-108">Med den Get-AzureRmNetworkWatcher cmdleten får du en eller flera Azure Network Watchrs-resurser.</span><span class="sxs-lookup"><span data-stu-id="26b1c-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="26b1c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26b1c-109">EXAMPLES</span></span>

### <span data-ttu-id="26b1c-110">--------------------------Exempel 1: skaffa en nätverks bevakning--------------------------</span><span class="sxs-lookup"><span data-stu-id="26b1c-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="26b1c-111">Hämtar nätverks övervakaren med namnet NetworkWatcher_westcentralus i NetworkWatcherRG för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="26b1c-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="26b1c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26b1c-112">PARAMETERS</span></span>

### <span data-ttu-id="26b1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b1c-113">-DefaultProfile</span></span>
<span data-ttu-id="26b1c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26b1c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26b1c-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="26b1c-115">-Name</span></span>
<span data-ttu-id="26b1c-116">Namnet på nät övervakaren.</span><span class="sxs-lookup"><span data-stu-id="26b1c-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="26b1c-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="26b1c-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b1c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b1c-119">CommonParameters</span></span>
<span data-ttu-id="26b1c-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b1c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b1c-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b1c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b1c-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26b1c-122">INPUTS</span></span>

### <span data-ttu-id="26b1c-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="26b1c-123">None</span></span>

## <span data-ttu-id="26b1c-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26b1c-124">OUTPUTS</span></span>

### <span data-ttu-id="26b1c-125">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26b1c-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="26b1c-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26b1c-126">NOTES</span></span>
<span data-ttu-id="26b1c-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="26b1c-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="26b1c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26b1c-128">RELATED LINKS</span></span>

[<span data-ttu-id="26b1c-129">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26b1c-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="26b1c-130">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="26b1c-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="26b1c-131">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26b1c-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26b1c-132">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="26b1c-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="26b1c-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26b1c-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26b1c-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26b1c-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26b1c-135">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="26b1c-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="26b1c-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="26b1c-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="26b1c-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="26b1c-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="26b1c-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="26b1c-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="26b1c-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="26b1c-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="26b1c-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="26b1c-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
