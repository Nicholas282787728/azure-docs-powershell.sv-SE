---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924178"
---
# <span data-ttu-id="bb7f1-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bb7f1-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="bb7f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7f1-103">Konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="bb7f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb7f1-104">SYNTAX</span></span>

### <span data-ttu-id="bb7f1-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="bb7f1-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb7f1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bb7f1-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb7f1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb7f1-107">DESCRIPTION</span></span>
<span data-ttu-id="bb7f1-108">Set-AzNetworkWatcherConfigFlowLog konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="bb7f1-109">Konfigurera med egenskaper: om flödes loggning är aktiverat för den angivna resursen, det konfigurerade lagrings kontot för att skicka loggar och bevarande princip för loggar.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="bb7f1-110">För närvarande stöds nätverks säkerhets grupper för flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="bb7f1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb7f1-111">EXAMPLES</span></span>

### <span data-ttu-id="bb7f1-112">---Exempel 1: Konfigurera flödes loggning för en angiven NSG---</span><span class="sxs-lookup"><span data-stu-id="bb7f1-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="bb7f1-113">I det här exemplet konfigurerar vi loggnings status för flödet för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="bb7f1-114">I svaret ser vi att NSG har Aktiver ATS för flödes loggning och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="bb7f1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb7f1-115">PARAMETERS</span></span>

### <span data-ttu-id="bb7f1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb7f1-116">-AsJob</span></span>
<span data-ttu-id="bb7f1-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bb7f1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb7f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb7f1-118">-DefaultProfile</span></span>
<span data-ttu-id="bb7f1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb7f1-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="bb7f1-120">-EnableFlowLog</span></span>
<span data-ttu-id="bb7f1-121">Flagga för att aktivera/inaktivera flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7f1-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="bb7f1-122">-EnableRetention</span></span>
<span data-ttu-id="bb7f1-123">Flagga för att aktivera/inaktivera bevarande.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7f1-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb7f1-124">-NetworkWatcher</span></span>
<span data-ttu-id="bb7f1-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="bb7f1-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bb7f1-126">-NetworkWatcherName</span></span>
<span data-ttu-id="bb7f1-127">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="bb7f1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb7f1-128">-ResourceGroupName</span></span>
<span data-ttu-id="bb7f1-129">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bb7f1-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bb7f1-130">-RetentionInDays</span></span>
<span data-ttu-id="bb7f1-131">Antalet dagar som flödes logg poster ska bevaras.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-131">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7f1-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bb7f1-132">-StorageAccountId</span></span>
<span data-ttu-id="bb7f1-133">ID för det lagrings konto som används för att lagra flödes loggen.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="bb7f1-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="bb7f1-134">-TargetResourceId</span></span>
<span data-ttu-id="bb7f1-135">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-135">The target resource ID.</span></span>

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

### <span data-ttu-id="bb7f1-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb7f1-136">-Confirm</span></span>
<span data-ttu-id="bb7f1-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7f1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb7f1-138">-WhatIf</span></span>
<span data-ttu-id="bb7f1-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb7f1-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7f1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb7f1-141">CommonParameters</span></span>
<span data-ttu-id="bb7f1-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb7f1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb7f1-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb7f1-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb7f1-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb7f1-144">INPUTS</span></span>

### <span data-ttu-id="bb7f1-145">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb7f1-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bb7f1-146">System. String system. Boolean system. Int32</span><span class="sxs-lookup"><span data-stu-id="bb7f1-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="bb7f1-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb7f1-147">OUTPUTS</span></span>

### <span data-ttu-id="bb7f1-148">Microsoft. Azure. commands. Networks. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="bb7f1-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="bb7f1-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb7f1-149">NOTES</span></span>
<span data-ttu-id="bb7f1-150">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, flöde, loggar, flowlog, loggning</span><span class="sxs-lookup"><span data-stu-id="bb7f1-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="bb7f1-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb7f1-151">RELATED LINKS</span></span>

[<span data-ttu-id="bb7f1-152">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bb7f1-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="bb7f1-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb7f1-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bb7f1-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb7f1-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bb7f1-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb7f1-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bb7f1-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb7f1-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb7f1-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bb7f1-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bb7f1-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb7f1-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb7f1-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb7f1-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb7f1-160">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb7f1-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb7f1-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bb7f1-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bb7f1-162">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bb7f1-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bb7f1-163">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bb7f1-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bb7f1-164">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bb7f1-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bb7f1-165">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bb7f1-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="bb7f1-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bb7f1-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
