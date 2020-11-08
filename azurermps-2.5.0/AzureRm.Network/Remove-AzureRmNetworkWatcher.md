---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 84b92468f4945cbe25404b81f4c6403254a23ad3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930142"
---
# <span data-ttu-id="360c9-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="360c9-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="360c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="360c9-102">SYNOPSIS</span></span>
<span data-ttu-id="360c9-103">Tar bort en nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="360c9-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="360c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="360c9-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="360c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="360c9-105">DESCRIPTION</span></span>
<span data-ttu-id="360c9-106">Remove-AzureRmNetworkWatcher cmdlet tar bort en nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="360c9-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="360c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="360c9-107">EXAMPLES</span></span>

### <span data-ttu-id="360c9-108">--------------------------Exempel 1: skapa och ta bort en nätverks bevakning--------------------------</span><span class="sxs-lookup"><span data-stu-id="360c9-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="360c9-109">I det här exemplet skapas en nätverks bevakning i en resurs grupp och sedan tas den omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="360c9-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="360c9-110">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="360c9-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="360c9-111">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="360c9-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="360c9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="360c9-112">PARAMETERS</span></span>

### <span data-ttu-id="360c9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="360c9-113">-AsJob</span></span>
<span data-ttu-id="360c9-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="360c9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="360c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360c9-115">-DefaultProfile</span></span>
<span data-ttu-id="360c9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="360c9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="360c9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="360c9-117">-Name</span></span>
<span data-ttu-id="360c9-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="360c9-118">The resource name.</span></span>

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

### <span data-ttu-id="360c9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="360c9-119">-PassThru</span></span>
<span data-ttu-id="360c9-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="360c9-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="360c9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="360c9-121">-ResourceGroupName</span></span>
<span data-ttu-id="360c9-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="360c9-122">The resource group name.</span></span>

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

### <span data-ttu-id="360c9-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="360c9-123">-Confirm</span></span>
<span data-ttu-id="360c9-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="360c9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="360c9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="360c9-125">-WhatIf</span></span>
<span data-ttu-id="360c9-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="360c9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="360c9-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="360c9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="360c9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360c9-128">CommonParameters</span></span>
<span data-ttu-id="360c9-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="360c9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360c9-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="360c9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360c9-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="360c9-131">INPUTS</span></span>

### <span data-ttu-id="360c9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="360c9-132">System.String</span></span>

## <span data-ttu-id="360c9-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="360c9-133">OUTPUTS</span></span>

### <span data-ttu-id="360c9-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="360c9-134">System.Object</span></span>

## <span data-ttu-id="360c9-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="360c9-135">NOTES</span></span>
<span data-ttu-id="360c9-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="360c9-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="360c9-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="360c9-137">RELATED LINKS</span></span>

[<span data-ttu-id="360c9-138">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="360c9-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="360c9-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="360c9-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="360c9-140">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="360c9-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="360c9-141">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="360c9-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="360c9-142">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="360c9-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="360c9-143">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="360c9-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="360c9-144">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="360c9-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="360c9-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="360c9-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="360c9-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="360c9-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="360c9-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="360c9-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="360c9-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="360c9-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="360c9-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="360c9-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)