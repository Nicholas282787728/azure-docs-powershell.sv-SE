---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 3c918b36bf851d34f8f10541de5cbf0de1a595cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583635"
---
# <span data-ttu-id="da0bd-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="da0bd-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="da0bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="da0bd-103">Konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="da0bd-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da0bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da0bd-104">SYNTAX</span></span>

### <span data-ttu-id="da0bd-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="da0bd-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da0bd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="da0bd-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da0bd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da0bd-107">DESCRIPTION</span></span>
<span data-ttu-id="da0bd-108">Set-AzureRmNetworkWatcherConfigFlowLog konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="da0bd-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="da0bd-109">Konfigurera med egenskaper: om flödes loggning är aktiverat för den angivna resursen, det konfigurerade lagrings kontot för att skicka loggar och bevarande princip för loggar.</span><span class="sxs-lookup"><span data-stu-id="da0bd-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="da0bd-110">För närvarande stöds nätverks säkerhets grupper för flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="da0bd-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="da0bd-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da0bd-111">EXAMPLES</span></span>

### <span data-ttu-id="da0bd-112">---Exempel 1: Konfigurera flödes loggning för en angiven NSG---</span><span class="sxs-lookup"><span data-stu-id="da0bd-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="da0bd-113">I det här exemplet konfigurerar vi loggnings status för flödet för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="da0bd-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="da0bd-114">I svaret ser vi att NSG har Aktiver ATS för flödes loggning och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="da0bd-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="da0bd-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da0bd-115">PARAMETERS</span></span>

### <span data-ttu-id="da0bd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da0bd-116">-AsJob</span></span>
<span data-ttu-id="da0bd-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="da0bd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da0bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da0bd-118">-DefaultProfile</span></span>
<span data-ttu-id="da0bd-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da0bd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da0bd-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="da0bd-120">-EnableFlowLog</span></span>
<span data-ttu-id="da0bd-121">Flagga för att aktivera/inaktivera flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="da0bd-121">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="da0bd-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="da0bd-122">-EnableRetention</span></span>
<span data-ttu-id="da0bd-123">Flagga för att aktivera/inaktivera bevarande.</span><span class="sxs-lookup"><span data-stu-id="da0bd-123">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="da0bd-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da0bd-124">-NetworkWatcher</span></span>
<span data-ttu-id="da0bd-125">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="da0bd-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="da0bd-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="da0bd-126">-NetworkWatcherName</span></span>
<span data-ttu-id="da0bd-127">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="da0bd-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="da0bd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da0bd-128">-ResourceGroupName</span></span>
<span data-ttu-id="da0bd-129">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="da0bd-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="da0bd-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="da0bd-130">-RetentionInDays</span></span>
<span data-ttu-id="da0bd-131">Antalet dagar som flödes logg poster ska bevaras.</span><span class="sxs-lookup"><span data-stu-id="da0bd-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="da0bd-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="da0bd-132">-StorageAccountId</span></span>
<span data-ttu-id="da0bd-133">ID för det lagrings konto som används för att lagra flödes loggen.</span><span class="sxs-lookup"><span data-stu-id="da0bd-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="da0bd-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="da0bd-134">-TargetResourceId</span></span>
<span data-ttu-id="da0bd-135">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="da0bd-135">The target resource ID.</span></span>

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

### <span data-ttu-id="da0bd-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da0bd-136">-Confirm</span></span>
<span data-ttu-id="da0bd-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da0bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da0bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da0bd-138">-WhatIf</span></span>
<span data-ttu-id="da0bd-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da0bd-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da0bd-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da0bd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da0bd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0bd-141">CommonParameters</span></span>
<span data-ttu-id="da0bd-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da0bd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0bd-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da0bd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0bd-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da0bd-144">INPUTS</span></span>

### <span data-ttu-id="da0bd-145">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da0bd-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="da0bd-146">System. String system. Boolean system. Int32</span><span class="sxs-lookup"><span data-stu-id="da0bd-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="da0bd-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da0bd-147">OUTPUTS</span></span>

### <span data-ttu-id="da0bd-148">Microsoft. Azure. commands. Networks. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="da0bd-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="da0bd-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da0bd-149">NOTES</span></span>
<span data-ttu-id="da0bd-150">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, flöde, loggar, flowlog, loggning</span><span class="sxs-lookup"><span data-stu-id="da0bd-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="da0bd-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da0bd-151">RELATED LINKS</span></span>

[<span data-ttu-id="da0bd-152">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="da0bd-152">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="da0bd-153">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da0bd-153">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="da0bd-154">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da0bd-154">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="da0bd-155">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da0bd-155">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="da0bd-156">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da0bd-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da0bd-157">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="da0bd-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="da0bd-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da0bd-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da0bd-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da0bd-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da0bd-160">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da0bd-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da0bd-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="da0bd-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="da0bd-162">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="da0bd-162">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="da0bd-163">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="da0bd-163">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="da0bd-164">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="da0bd-164">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="da0bd-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="da0bd-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="da0bd-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="da0bd-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
