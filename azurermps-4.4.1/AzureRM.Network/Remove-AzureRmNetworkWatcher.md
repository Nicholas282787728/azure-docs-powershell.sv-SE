---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: ee92fd78d3a69b38620b2af543e01db7569d3b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573618"
---
# <span data-ttu-id="84778-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84778-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="84778-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84778-102">SYNOPSIS</span></span>
<span data-ttu-id="84778-103">Tar bort en nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="84778-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84778-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84778-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84778-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84778-105">DESCRIPTION</span></span>
<span data-ttu-id="84778-106">Remove-AzureRmNetworkWatcher cmdlet tar bort en nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="84778-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="84778-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84778-107">EXAMPLES</span></span>

### <span data-ttu-id="84778-108">--------------------------Exempel 1: skapa och ta bort en nätverks bevakning--------------------------</span><span class="sxs-lookup"><span data-stu-id="84778-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="84778-109">I det här exemplet skapas en nätverks bevakning i en resurs grupp och sedan tas den omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="84778-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="84778-110">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="84778-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="84778-111">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="84778-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="84778-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84778-112">PARAMETERS</span></span>

### <span data-ttu-id="84778-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="84778-113">-Name</span></span>
<span data-ttu-id="84778-114">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="84778-114">The resource name.</span></span>

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

### <span data-ttu-id="84778-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84778-115">-PassThru</span></span>
<span data-ttu-id="84778-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="84778-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84778-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84778-117">-ResourceGroupName</span></span>
<span data-ttu-id="84778-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="84778-118">The resource group name.</span></span>

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

### <span data-ttu-id="84778-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84778-119">-Confirm</span></span>
<span data-ttu-id="84778-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84778-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84778-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84778-121">-WhatIf</span></span>
<span data-ttu-id="84778-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="84778-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84778-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="84778-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84778-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84778-124">-DefaultProfile</span></span>
<span data-ttu-id="84778-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84778-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84778-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84778-126">CommonParameters</span></span>
<span data-ttu-id="84778-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84778-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84778-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84778-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84778-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84778-129">INPUTS</span></span>

### <span data-ttu-id="84778-130">System. String</span><span class="sxs-lookup"><span data-stu-id="84778-130">System.String</span></span>

## <span data-ttu-id="84778-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84778-131">OUTPUTS</span></span>

### <span data-ttu-id="84778-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="84778-132">System.Object</span></span>

## <span data-ttu-id="84778-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84778-133">NOTES</span></span>
<span data-ttu-id="84778-134">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="84778-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="84778-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84778-135">RELATED LINKS</span></span>

[<span data-ttu-id="84778-136">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84778-136">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="84778-137">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84778-137">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="84778-138">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84778-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84778-139">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="84778-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="84778-140">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84778-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84778-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84778-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84778-142">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84778-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84778-143">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="84778-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="84778-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="84778-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="84778-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="84778-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="84778-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="84778-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="84778-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="84778-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
