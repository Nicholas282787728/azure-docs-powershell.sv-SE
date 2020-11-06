---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 20d59fb2a112b32c95b380c114ebc1b365569235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575188"
---
# <span data-ttu-id="c6023-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c6023-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="c6023-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6023-102">SYNOPSIS</span></span>
<span data-ttu-id="c6023-103">Konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="c6023-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6023-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6023-104">SYNTAX</span></span>

### <span data-ttu-id="c6023-105">SetFlowlogByResourceWithoutTA (standard)</span><span class="sxs-lookup"><span data-stu-id="c6023-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6023-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="c6023-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6023-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="c6023-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String>
 -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6023-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="c6023-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6023-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="c6023-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6023-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="c6023-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6023-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="c6023-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6023-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="c6023-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6023-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="c6023-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6023-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6023-114">DESCRIPTION</span></span>
<span data-ttu-id="c6023-115">Set-AzureRmNetworkWatcherConfigFlowLog konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="c6023-115">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="c6023-116">Konfigurera med egenskaper: om flödes loggning är aktiverat för den angivna resursen, det konfigurerade lagrings kontot för att skicka loggar och bevarande princip för loggar.</span><span class="sxs-lookup"><span data-stu-id="c6023-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="c6023-117">För närvarande stöds nätverks säkerhets grupper för flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="c6023-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="c6023-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6023-118">EXAMPLES</span></span>

### <span data-ttu-id="c6023-119">Exempel 1: Konfigurera flödes loggning för en angiven NSG</span><span class="sxs-lookup"><span data-stu-id="c6023-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="c6023-120">I det här exemplet konfigurerar vi loggnings status för flödet för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="c6023-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="c6023-121">I svaret ser vi att NSG har Aktiver ATS för flödes loggning och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="c6023-121">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

### <span data-ttu-id="c6023-122">Exempel 2: Konfigurera flödes loggning och trafik analys för en viss NSG</span><span class="sxs-lookup"><span data-stu-id="c6023-122">Example 2: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzureRmOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName"
            }
          }
```

<span data-ttu-id="c6023-123">I det här exemplet konfigurerar vi status för flödes loggning och trafik analys för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="c6023-123">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="c6023-124">I svaret ser vi att den angivna NSG har flödes loggning och trafik analys aktive rad, och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="c6023-124">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, and no retention policy set.</span></span>

## <span data-ttu-id="c6023-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6023-125">PARAMETERS</span></span>

### <span data-ttu-id="c6023-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6023-126">-AsJob</span></span>
<span data-ttu-id="c6023-127">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c6023-127">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6023-128">-DefaultProfile</span></span>
<span data-ttu-id="c6023-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6023-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6023-130">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="c6023-130">-EnableFlowLog</span></span>
<span data-ttu-id="c6023-131">Flagga för att aktivera/inaktivera flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="c6023-131">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="c6023-132">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="c6023-132">-EnableRetention</span></span>
<span data-ttu-id="c6023-133">Flagga för att aktivera/inaktivera bevarande.</span><span class="sxs-lookup"><span data-stu-id="c6023-133">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="c6023-134">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="c6023-134">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="c6023-135">Flagga för att aktivera/inaktivera bevarande.</span><span class="sxs-lookup"><span data-stu-id="c6023-135">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="c6023-136">-Location</span></span>
<span data-ttu-id="c6023-137">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="c6023-137">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-138">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6023-138">-NetworkWatcher</span></span>
<span data-ttu-id="c6023-139">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="c6023-139">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-140">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c6023-140">-NetworkWatcherName</span></span>
<span data-ttu-id="c6023-141">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="c6023-141">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6023-142">-ResourceGroupName</span></span>
<span data-ttu-id="c6023-143">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c6023-143">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c6023-144">-RetentionInDays</span></span>
<span data-ttu-id="c6023-145">Antalet dagar som flödes logg poster ska bevaras.</span><span class="sxs-lookup"><span data-stu-id="c6023-145">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="c6023-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c6023-146">-StorageAccountId</span></span>
<span data-ttu-id="c6023-147">ID för det lagrings konto som används för att lagra flödes loggen.</span><span class="sxs-lookup"><span data-stu-id="c6023-147">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="c6023-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c6023-148">-TargetResourceId</span></span>
<span data-ttu-id="c6023-149">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c6023-149">The target resource ID.</span></span>

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

### <span data-ttu-id="c6023-150">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="c6023-150">-Workspace</span></span>
<span data-ttu-id="c6023-151">Det WS-objekt som används för att lagra trafikanalys data.</span><span class="sxs-lookup"><span data-stu-id="c6023-151">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-152">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="c6023-152">-WorkspaceGUID</span></span>
<span data-ttu-id="c6023-153">GUID för WS som används för att lagra trafikanalys data.</span><span class="sxs-lookup"><span data-stu-id="c6023-153">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-154">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="c6023-154">-WorkspaceLocation</span></span>
<span data-ttu-id="c6023-155">Azure-regionen i WS som används för att lagra trafikanalys data.</span><span class="sxs-lookup"><span data-stu-id="c6023-155">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-156">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="c6023-156">-WorkspaceResourceId</span></span>
<span data-ttu-id="c6023-157">Abonnemang på WS som används för att lagra trafikanalys data.</span><span class="sxs-lookup"><span data-stu-id="c6023-157">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6023-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6023-158">-Confirm</span></span>
<span data-ttu-id="c6023-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6023-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6023-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6023-160">-WhatIf</span></span>
<span data-ttu-id="c6023-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6023-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6023-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6023-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6023-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6023-163">CommonParameters</span></span>
<span data-ttu-id="c6023-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6023-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6023-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6023-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6023-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6023-166">INPUTS</span></span>

### <span data-ttu-id="c6023-167">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6023-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c6023-168">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c6023-168">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="c6023-169">System. String</span><span class="sxs-lookup"><span data-stu-id="c6023-169">System.String</span></span>
<span data-ttu-id="c6023-170">Parametrar: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c6023-170">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="c6023-171">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6023-171">System.Boolean</span></span>

### <span data-ttu-id="c6023-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c6023-172">System.Int32</span></span>

### <span data-ttu-id="c6023-173">Microsoft. Azure. Management. Internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6023-173">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="c6023-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6023-174">OUTPUTS</span></span>

### <span data-ttu-id="c6023-175">Microsoft. Azure. commands. Networks. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="c6023-175">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="c6023-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6023-176">NOTES</span></span>
<span data-ttu-id="c6023-177">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, flöde, loggar, flowlog, loggning</span><span class="sxs-lookup"><span data-stu-id="c6023-177">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="c6023-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6023-178">RELATED LINKS</span></span>

[<span data-ttu-id="c6023-179">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6023-179">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c6023-180">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6023-180">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c6023-181">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6023-181">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c6023-182">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c6023-182">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c6023-183">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c6023-183">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c6023-184">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c6023-184">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c6023-185">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c6023-185">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c6023-186">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c6023-186">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c6023-187">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c6023-187">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c6023-188">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c6023-188">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c6023-189">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c6023-189">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c6023-190">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c6023-190">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c6023-191">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6023-191">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c6023-192">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c6023-192">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c6023-193">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c6023-193">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="c6023-194">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6023-194">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6023-195">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6023-195">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6023-196">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6023-196">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6023-197">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c6023-197">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c6023-198">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6023-198">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6023-199">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6023-199">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6023-200">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c6023-200">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c6023-201">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c6023-201">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c6023-202">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c6023-202">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c6023-203">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c6023-203">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c6023-204">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c6023-204">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c6023-205">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6023-205">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
