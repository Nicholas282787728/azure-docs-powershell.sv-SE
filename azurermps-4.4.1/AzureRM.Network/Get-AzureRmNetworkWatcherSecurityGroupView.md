---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 44bba48f1d066c4a9006595092bd84c68252bbd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580544"
---
# <span data-ttu-id="236bd-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="236bd-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="236bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="236bd-102">SYNOPSIS</span></span>
<span data-ttu-id="236bd-103">Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="236bd-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="236bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="236bd-104">SYNTAX</span></span>

### <span data-ttu-id="236bd-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="236bd-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="236bd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="236bd-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="236bd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="236bd-107">DESCRIPTION</span></span>
<span data-ttu-id="236bd-108">Med Get-AzureRmNetworkWatcherSecurityGroupView kan du Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="236bd-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="236bd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="236bd-109">EXAMPLES</span></span>

### <span data-ttu-id="236bd-110">---Exempel 1: skapa ett samtal för en säkerhets grupp på en virtuell dator---</span><span class="sxs-lookup"><span data-stu-id="236bd-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="236bd-111">I exemplet ovan skaffa vi först den regionala nätverks Watchheten och sedan en VM i regionen.</span><span class="sxs-lookup"><span data-stu-id="236bd-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="236bd-112">Då ringer vi ett samtal på den angivna virtuella datorns säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="236bd-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="236bd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="236bd-113">PARAMETERS</span></span>

### <span data-ttu-id="236bd-114">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="236bd-114">-NetworkWatcher</span></span>
<span data-ttu-id="236bd-115">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="236bd-115">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="236bd-116">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="236bd-116">-NetworkWatcherName</span></span>
<span data-ttu-id="236bd-117">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="236bd-117">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="236bd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="236bd-118">-ResourceGroupName</span></span>
<span data-ttu-id="236bd-119">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="236bd-119">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="236bd-120">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="236bd-120">-TargetVirtualMachineId</span></span>
<span data-ttu-id="236bd-121">Målprogram-ID för mål</span><span class="sxs-lookup"><span data-stu-id="236bd-121">The target VM Id</span></span>

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

### <span data-ttu-id="236bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236bd-122">-DefaultProfile</span></span>
<span data-ttu-id="236bd-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="236bd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="236bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236bd-124">CommonParameters</span></span>
<span data-ttu-id="236bd-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="236bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236bd-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="236bd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236bd-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="236bd-127">INPUTS</span></span>

### <span data-ttu-id="236bd-128">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="236bd-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="236bd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="236bd-129">System.String</span></span>

## <span data-ttu-id="236bd-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="236bd-130">OUTPUTS</span></span>

### <span data-ttu-id="236bd-131">Microsoft. Azure. commands. Networks. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="236bd-131">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="236bd-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="236bd-132">NOTES</span></span>
<span data-ttu-id="236bd-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="236bd-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="236bd-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="236bd-134">RELATED LINKS</span></span>

[<span data-ttu-id="236bd-135">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="236bd-135">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="236bd-136">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="236bd-136">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="236bd-137">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="236bd-137">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="236bd-138">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="236bd-138">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="236bd-139">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="236bd-139">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="236bd-140">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="236bd-140">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="236bd-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="236bd-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="236bd-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="236bd-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="236bd-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="236bd-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="236bd-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="236bd-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="236bd-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="236bd-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="236bd-146">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="236bd-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

