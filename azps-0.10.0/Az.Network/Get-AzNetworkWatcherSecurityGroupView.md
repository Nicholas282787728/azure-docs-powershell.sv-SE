---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: fe315ac4b6c29b8ffd1c82c8045ba9b7a7aab4a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922238"
---
# <span data-ttu-id="31627-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="31627-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="31627-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31627-102">SYNOPSIS</span></span>
<span data-ttu-id="31627-103">Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="31627-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="31627-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31627-104">SYNTAX</span></span>

### <span data-ttu-id="31627-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="31627-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31627-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="31627-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31627-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31627-107">DESCRIPTION</span></span>
<span data-ttu-id="31627-108">Med Get-AzNetworkWatcherSecurityGroupView kan du Visa de konfigurerade och effektiva nätverks säkerhets grup regler som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="31627-108">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="31627-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31627-109">EXAMPLES</span></span>

### <span data-ttu-id="31627-110">---Exempel 1: skapa ett samtal för en säkerhets grupp på en virtuell dator---</span><span class="sxs-lookup"><span data-stu-id="31627-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="31627-111">I exemplet ovan skaffa vi först den regionala nätverks Watchheten och sedan en VM i regionen.</span><span class="sxs-lookup"><span data-stu-id="31627-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="31627-112">Då ringer vi ett samtal på den angivna virtuella datorns säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="31627-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="31627-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31627-113">PARAMETERS</span></span>

### <span data-ttu-id="31627-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31627-114">-AsJob</span></span>
<span data-ttu-id="31627-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="31627-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31627-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31627-116">-DefaultProfile</span></span>
<span data-ttu-id="31627-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31627-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31627-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31627-118">-NetworkWatcher</span></span>
<span data-ttu-id="31627-119">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="31627-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="31627-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="31627-120">-NetworkWatcherName</span></span>
<span data-ttu-id="31627-121">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="31627-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="31627-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31627-122">-ResourceGroupName</span></span>
<span data-ttu-id="31627-123">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="31627-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="31627-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="31627-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="31627-125">Målprogram-ID för mål</span><span class="sxs-lookup"><span data-stu-id="31627-125">The target VM Id</span></span>

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

### <span data-ttu-id="31627-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31627-126">CommonParameters</span></span>
<span data-ttu-id="31627-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31627-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31627-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31627-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31627-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31627-129">INPUTS</span></span>

### <span data-ttu-id="31627-130">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31627-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="31627-131">System. String</span><span class="sxs-lookup"><span data-stu-id="31627-131">System.String</span></span>

## <span data-ttu-id="31627-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31627-132">OUTPUTS</span></span>

### <span data-ttu-id="31627-133">Microsoft. Azure. commands. Networks. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="31627-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="31627-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31627-134">NOTES</span></span>
<span data-ttu-id="31627-135">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, flöde, IP</span><span class="sxs-lookup"><span data-stu-id="31627-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="31627-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31627-136">RELATED LINKS</span></span>

[<span data-ttu-id="31627-137">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31627-137">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="31627-138">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31627-138">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="31627-139">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="31627-139">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="31627-140">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="31627-140">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="31627-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="31627-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="31627-142">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="31627-142">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="31627-143">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="31627-143">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="31627-144">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31627-144">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31627-145">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="31627-145">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="31627-146">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31627-146">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31627-147">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31627-147">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="31627-148">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="31627-148">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

