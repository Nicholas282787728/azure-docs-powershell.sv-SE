---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 97227c27e23c6283fd64e1660262bbec175cf0a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931278"
---
# <span data-ttu-id="86284-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86284-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="86284-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86284-102">SYNOPSIS</span></span>
<span data-ttu-id="86284-103">Hämtar egenskaperna för en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="86284-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86284-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86284-104">SYNTAX</span></span>

### <span data-ttu-id="86284-105">Lära</span><span class="sxs-lookup"><span data-stu-id="86284-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86284-106">Förteckning</span><span class="sxs-lookup"><span data-stu-id="86284-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86284-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86284-107">DESCRIPTION</span></span>
<span data-ttu-id="86284-108">Med den Get-AzureRmNetworkWatcher cmdleten får du en eller flera Azure Network Watchrs-resurser.</span><span class="sxs-lookup"><span data-stu-id="86284-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="86284-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86284-109">EXAMPLES</span></span>

### <span data-ttu-id="86284-110">--------------------------Exempel 1: skaffa en nätverks bevakning--------------------------</span><span class="sxs-lookup"><span data-stu-id="86284-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="86284-111">Hämtar nätverks övervakaren med namnet NetworkWatcher_westcentralus i NetworkWatcherRG för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="86284-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="86284-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86284-112">PARAMETERS</span></span>

### <span data-ttu-id="86284-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86284-113">-DefaultProfile</span></span>
<span data-ttu-id="86284-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86284-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86284-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="86284-115">-Name</span></span>
<span data-ttu-id="86284-116">Namnet på nät övervakaren.</span><span class="sxs-lookup"><span data-stu-id="86284-116">The network watcher name.</span></span>

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

### <span data-ttu-id="86284-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86284-117">-ResourceGroupName</span></span>
<span data-ttu-id="86284-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="86284-118">The resource group name.</span></span>

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

### <span data-ttu-id="86284-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86284-119">CommonParameters</span></span>
<span data-ttu-id="86284-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86284-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86284-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86284-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86284-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86284-122">INPUTS</span></span>

### <span data-ttu-id="86284-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="86284-123">None</span></span>

## <span data-ttu-id="86284-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86284-124">OUTPUTS</span></span>

### <span data-ttu-id="86284-125">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86284-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="86284-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86284-126">NOTES</span></span>
<span data-ttu-id="86284-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="86284-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="86284-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86284-128">RELATED LINKS</span></span>

[<span data-ttu-id="86284-129">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86284-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="86284-130">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86284-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="86284-131">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86284-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86284-132">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="86284-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="86284-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86284-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86284-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86284-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86284-135">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86284-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86284-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="86284-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="86284-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="86284-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="86284-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86284-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="86284-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="86284-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="86284-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="86284-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
