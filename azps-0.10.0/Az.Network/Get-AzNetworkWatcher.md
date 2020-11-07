---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922255"
---
# <span data-ttu-id="8f2ea-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f2ea-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="8f2ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2ea-103">Hämtar egenskaperna för en nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="8f2ea-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="8f2ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f2ea-104">SYNTAX</span></span>

### <span data-ttu-id="8f2ea-105">Lära</span><span class="sxs-lookup"><span data-stu-id="8f2ea-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f2ea-106">Förteckning</span><span class="sxs-lookup"><span data-stu-id="8f2ea-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f2ea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f2ea-107">DESCRIPTION</span></span>
<span data-ttu-id="8f2ea-108">Med den Get-AzNetworkWatcher cmdleten får du en eller flera Azure Network Watchrs-resurser.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="8f2ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f2ea-109">EXAMPLES</span></span>

### <span data-ttu-id="8f2ea-110">--------------------------Exempel 1: skaffa en nätverks bevakning--------------------------</span><span class="sxs-lookup"><span data-stu-id="8f2ea-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="8f2ea-111">Hämtar nätverks övervakaren med namnet NetworkWatcher_westcentralus i NetworkWatcherRG för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="8f2ea-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f2ea-112">PARAMETERS</span></span>

### <span data-ttu-id="8f2ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2ea-113">-DefaultProfile</span></span>
<span data-ttu-id="8f2ea-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f2ea-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f2ea-115">-Name</span></span>
<span data-ttu-id="8f2ea-116">Namnet på nät övervakaren.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-116">The network watcher name.</span></span>

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

### <span data-ttu-id="8f2ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f2ea-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-118">The resource group name.</span></span>

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

### <span data-ttu-id="8f2ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2ea-119">CommonParameters</span></span>
<span data-ttu-id="8f2ea-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2ea-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f2ea-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2ea-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f2ea-122">INPUTS</span></span>

### <span data-ttu-id="8f2ea-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="8f2ea-123">None</span></span>

## <span data-ttu-id="8f2ea-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f2ea-124">OUTPUTS</span></span>

### <span data-ttu-id="8f2ea-125">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f2ea-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="8f2ea-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f2ea-126">NOTES</span></span>
<span data-ttu-id="8f2ea-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="8f2ea-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="8f2ea-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f2ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="8f2ea-129">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f2ea-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8f2ea-130">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f2ea-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8f2ea-131">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f2ea-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f2ea-132">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8f2ea-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8f2ea-133">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f2ea-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f2ea-134">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f2ea-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f2ea-135">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8f2ea-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8f2ea-136">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8f2ea-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8f2ea-137">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8f2ea-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8f2ea-138">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8f2ea-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8f2ea-139">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8f2ea-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8f2ea-140">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8f2ea-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
