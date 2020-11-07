---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 276cd57a51b6b457f2f4d205932cdbfabd7613b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924378"
---
# <span data-ttu-id="557fc-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="557fc-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="557fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="557fc-102">SYNOPSIS</span></span>
<span data-ttu-id="557fc-103">Tar bort en nätverks bevakning.</span><span class="sxs-lookup"><span data-stu-id="557fc-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="557fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="557fc-104">SYNTAX</span></span>

```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="557fc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="557fc-105">DESCRIPTION</span></span>
<span data-ttu-id="557fc-106">Remove-AzNetworkWatcher cmdlet tar bort en nätverks bevaknings resurs.</span><span class="sxs-lookup"><span data-stu-id="557fc-106">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="557fc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="557fc-107">EXAMPLES</span></span>

### <span data-ttu-id="557fc-108">--------------------------Exempel 1: skapa och ta bort en nätverks bevakning--------------------------</span><span class="sxs-lookup"><span data-stu-id="557fc-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="557fc-109">I det här exemplet skapas en nätverks bevakning i en resurs grupp och sedan tas den omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="557fc-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="557fc-110">Observera att endast en nätverks bevakning kan skapas per region per prenumeration.</span><span class="sxs-lookup"><span data-stu-id="557fc-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="557fc-111">Om du inte vill att meddelandet ska visas när det virtuella nätverket tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="557fc-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="557fc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="557fc-112">PARAMETERS</span></span>

### <span data-ttu-id="557fc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="557fc-113">-AsJob</span></span>
<span data-ttu-id="557fc-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="557fc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="557fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557fc-115">-DefaultProfile</span></span>
<span data-ttu-id="557fc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="557fc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="557fc-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="557fc-117">-Name</span></span>
<span data-ttu-id="557fc-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="557fc-118">The resource name.</span></span>

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

### <span data-ttu-id="557fc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="557fc-119">-PassThru</span></span>
<span data-ttu-id="557fc-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="557fc-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="557fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="557fc-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="557fc-122">The resource group name.</span></span>

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

### <span data-ttu-id="557fc-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="557fc-123">-Confirm</span></span>
<span data-ttu-id="557fc-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="557fc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="557fc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="557fc-125">-WhatIf</span></span>
<span data-ttu-id="557fc-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="557fc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="557fc-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="557fc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="557fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557fc-128">CommonParameters</span></span>
<span data-ttu-id="557fc-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="557fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557fc-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="557fc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557fc-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="557fc-131">INPUTS</span></span>

### <span data-ttu-id="557fc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="557fc-132">System.String</span></span>

## <span data-ttu-id="557fc-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="557fc-133">OUTPUTS</span></span>

### <span data-ttu-id="557fc-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="557fc-134">System.Object</span></span>

## <span data-ttu-id="557fc-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="557fc-135">NOTES</span></span>
<span data-ttu-id="557fc-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="557fc-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="557fc-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="557fc-137">RELATED LINKS</span></span>

[<span data-ttu-id="557fc-138">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="557fc-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="557fc-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="557fc-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="557fc-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="557fc-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="557fc-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="557fc-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="557fc-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="557fc-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="557fc-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="557fc-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="557fc-144">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="557fc-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="557fc-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="557fc-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="557fc-146">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="557fc-146">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="557fc-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="557fc-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="557fc-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="557fc-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="557fc-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="557fc-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
