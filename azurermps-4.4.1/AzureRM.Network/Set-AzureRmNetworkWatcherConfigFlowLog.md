---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: e8ce107453a447ef2da4cb8528b2f3e1f24a3ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575964"
---
# <span data-ttu-id="4e6f2-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e6f2-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="4e6f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6f2-103">Konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e6f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e6f2-104">SYNTAX</span></span>

### <span data-ttu-id="4e6f2-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="4e6f2-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e6f2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4e6f2-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e6f2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e6f2-107">DESCRIPTION</span></span>
<span data-ttu-id="4e6f2-108">Set-AzureRmNetworkWatcherConfigFlowLog konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="4e6f2-109">Konfigurera med egenskaper: om flödes loggning är aktiverat för den angivna resursen, det konfigurerade lagrings kontot för att skicka loggar och bevarande princip för loggar.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="4e6f2-110">För närvarande stöds nätverks säkerhets grupper för flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="4e6f2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e6f2-111">EXAMPLES</span></span>

### <span data-ttu-id="4e6f2-112">---Exempel 1: Konfigurera flödes loggning för en angiven NSG---</span><span class="sxs-lookup"><span data-stu-id="4e6f2-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
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

<span data-ttu-id="4e6f2-113">I det här exemplet konfigurerar vi loggnings status för flödet för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="4e6f2-114">I svaret ser vi att NSG har Aktiver ATS för flödes loggning och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="4e6f2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e6f2-115">PARAMETERS</span></span>

### <span data-ttu-id="4e6f2-116">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e6f2-116">-EnableFlowLog</span></span>
<span data-ttu-id="4e6f2-117">Flagga för att aktivera/inaktivera flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-117">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6f2-118">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="4e6f2-118">-EnableRetention</span></span>
<span data-ttu-id="4e6f2-119">Flagga för att aktivera/inaktivera bevarande.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-119">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6f2-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e6f2-120">-NetworkWatcher</span></span>
<span data-ttu-id="4e6f2-121">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="4e6f2-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4e6f2-122">-NetworkWatcherName</span></span>
<span data-ttu-id="4e6f2-123">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="4e6f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e6f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e6f2-125">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4e6f2-126">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4e6f2-126">-RetentionInDays</span></span>
<span data-ttu-id="4e6f2-127">Antalet dagar som flödes logg poster ska bevaras.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-127">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6f2-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4e6f2-128">-StorageAccountId</span></span>
<span data-ttu-id="4e6f2-129">ID för det lagrings konto som används för att lagra flödes loggen.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-129">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="4e6f2-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4e6f2-130">-TargetResourceId</span></span>
<span data-ttu-id="4e6f2-131">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-131">The target resource ID.</span></span>

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

### <span data-ttu-id="4e6f2-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e6f2-132">-Confirm</span></span>
<span data-ttu-id="4e6f2-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6f2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e6f2-134">-WhatIf</span></span>
<span data-ttu-id="4e6f2-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e6f2-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6f2-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6f2-137">-DefaultProfile</span></span>
<span data-ttu-id="4e6f2-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e6f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6f2-139">CommonParameters</span></span>
<span data-ttu-id="4e6f2-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e6f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6f2-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e6f2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6f2-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e6f2-142">INPUTS</span></span>

### <span data-ttu-id="4e6f2-143">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e6f2-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4e6f2-144">System. String system. Boolean system. Int32</span><span class="sxs-lookup"><span data-stu-id="4e6f2-144">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="4e6f2-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e6f2-145">OUTPUTS</span></span>

### <span data-ttu-id="4e6f2-146">Microsoft. Azure. commands. Networks. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e6f2-146">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="4e6f2-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e6f2-147">NOTES</span></span>
<span data-ttu-id="4e6f2-148">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, flöde, loggar, flowlog, loggning</span><span class="sxs-lookup"><span data-stu-id="4e6f2-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="4e6f2-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e6f2-149">RELATED LINKS</span></span>

[<span data-ttu-id="4e6f2-150">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4e6f2-150">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4e6f2-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e6f2-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4e6f2-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e6f2-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4e6f2-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e6f2-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4e6f2-154">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e6f2-154">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e6f2-155">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4e6f2-155">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4e6f2-156">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e6f2-156">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e6f2-157">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e6f2-157">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e6f2-158">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e6f2-158">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e6f2-159">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4e6f2-159">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4e6f2-160">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4e6f2-160">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4e6f2-161">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4e6f2-161">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4e6f2-162">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4e6f2-162">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4e6f2-163">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4e6f2-163">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4e6f2-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4e6f2-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
