---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
ms.openlocfilehash: fad852ff589b2929df83775a2fa955e72663cfa2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929030"
---
# <span data-ttu-id="0104d-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0104d-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="0104d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0104d-102">SYNOPSIS</span></span>
<span data-ttu-id="0104d-103">Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0104d-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0104d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0104d-104">SYNTAX</span></span>

### <span data-ttu-id="0104d-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="0104d-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0104d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0104d-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0104d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0104d-107">DESCRIPTION</span></span>
<span data-ttu-id="0104d-108">Med Get-AzureRmNetworkWatcherSecurityGroupView kan du Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0104d-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="0104d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0104d-109">EXAMPLES</span></span>

### <span data-ttu-id="0104d-110">---Exempel 1: skapa ett samtal för en säkerhets grupp på en virtuell dator---</span><span class="sxs-lookup"><span data-stu-id="0104d-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="0104d-111">I exemplet ovan skaffa vi först den regionala nätverks Watchheten och sedan en VM i regionen.</span><span class="sxs-lookup"><span data-stu-id="0104d-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="0104d-112">Då ringer vi ett samtal på den angivna virtuella datorns säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="0104d-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="0104d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0104d-113">PARAMETERS</span></span>

### <span data-ttu-id="0104d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0104d-114">-AsJob</span></span>
<span data-ttu-id="0104d-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0104d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0104d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0104d-116">-DefaultProfile</span></span>
<span data-ttu-id="0104d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0104d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0104d-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0104d-118">-NetworkWatcher</span></span>
<span data-ttu-id="0104d-119">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="0104d-119">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0104d-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0104d-120">-NetworkWatcherName</span></span>
<span data-ttu-id="0104d-121">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="0104d-121">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0104d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0104d-122">-ResourceGroupName</span></span>
<span data-ttu-id="0104d-123">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0104d-123">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0104d-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0104d-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0104d-125">Målprogram-ID för mål</span><span class="sxs-lookup"><span data-stu-id="0104d-125">The target VM Id</span></span>

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

### <span data-ttu-id="0104d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0104d-126">CommonParameters</span></span>
<span data-ttu-id="0104d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0104d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0104d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0104d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0104d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0104d-129">INPUTS</span></span>

### <span data-ttu-id="0104d-130">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0104d-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0104d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0104d-131">System.String</span></span>

## <span data-ttu-id="0104d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0104d-132">OUTPUTS</span></span>

### <span data-ttu-id="0104d-133">Microsoft. Azure. commands. Networks. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="0104d-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="0104d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0104d-134">NOTES</span></span>
<span data-ttu-id="0104d-135">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="0104d-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="0104d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0104d-136">RELATED LINKS</span></span>

[<span data-ttu-id="0104d-137">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0104d-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0104d-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0104d-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0104d-139">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0104d-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0104d-140">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0104d-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0104d-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0104d-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="0104d-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0104d-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0104d-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0104d-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0104d-144">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0104d-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0104d-145">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0104d-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0104d-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0104d-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0104d-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0104d-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0104d-148">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0104d-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

