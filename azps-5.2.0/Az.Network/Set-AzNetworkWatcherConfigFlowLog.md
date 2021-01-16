---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 6d4dca8cdaa9e80fd1417fd65a9200eb5e3ecf7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400584"
---
# <span data-ttu-id="75b5e-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="75b5e-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="75b5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="75b5e-103">Konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="75b5e-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="75b5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75b5e-104">SYNTAX</span></span>

### <span data-ttu-id="75b5e-105">SetFlowlogByResourceWithoutTA (standard)</span><span class="sxs-lookup"><span data-stu-id="75b5e-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b5e-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="75b5e-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b5e-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="75b5e-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75b5e-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="75b5e-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b5e-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="75b5e-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75b5e-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="75b5e-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b5e-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="75b5e-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75b5e-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="75b5e-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b5e-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="75b5e-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75b5e-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75b5e-114">DESCRIPTION</span></span>
<span data-ttu-id="75b5e-115">Set-AzNetworkWatcherConfigFlowLog konfigurerar flödes loggning för en mål resurs.</span><span class="sxs-lookup"><span data-stu-id="75b5e-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="75b5e-116">Konfigurera med egenskaper: om flödes loggning är aktiverat för den angivna resursen, det konfigurerade lagrings kontot för att skicka loggar, flödes loggnings format och bevarande princip för loggarna.</span><span class="sxs-lookup"><span data-stu-id="75b5e-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="75b5e-117">För närvarande stöds nätverks säkerhets grupper för flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="75b5e-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="75b5e-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75b5e-118">EXAMPLES</span></span>

### <span data-ttu-id="75b5e-119">Exempel 1: Konfigurera flödes loggning för en angiven NSG</span><span class="sxs-lookup"><span data-stu-id="75b5e-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="75b5e-120">I det här exemplet konfigurerar vi loggnings status för flödet för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="75b5e-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="75b5e-121">I svaret ser vi att den angivna NSG har flödes loggning aktive rad, standardinställningar och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="75b5e-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="75b5e-122">Exempel 2: Konfigurera flödes loggning för en angiven NSG och ange versionen för flödes loggning till 2.</span><span class="sxs-lookup"><span data-stu-id="75b5e-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="75b5e-123">I det här exemplet konfigurerar vi flödes loggning på en nätverks säkerhets grupp (NSG) med version 2-loggar angiven.</span><span class="sxs-lookup"><span data-stu-id="75b5e-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="75b5e-124">I svaret ser vi att den angivna NSG har flödes loggning aktive rad, att formatet är angivet och att ingen bevarande princip har kon figurer ATS.</span><span class="sxs-lookup"><span data-stu-id="75b5e-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="75b5e-125">Om regionen inte har stöd för den version som du har angett skrivs den standard version som stöds i regionen.</span><span class="sxs-lookup"><span data-stu-id="75b5e-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="75b5e-126">Exempel 3: Konfigurera flödes loggning och trafik analys för en viss NSG</span><span class="sxs-lookup"><span data-stu-id="75b5e-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="75b5e-127">I det här exemplet konfigurerar vi status för flödes loggning och trafik analys för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="75b5e-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="75b5e-128">I svaret ser vi att den angivna NSG har flödes loggning och Traffic Analytics aktive rad, standard format och ingen bevarande princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="75b5e-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="75b5e-129">Exempel 4: inaktivera trafikanalys för angivna NSG med flödes loggning och trafikanalys konfigurerade</span><span class="sxs-lookup"><span data-stu-id="75b5e-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg
PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics:$false -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": false,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
          "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="75b5e-130">I det här exemplet inaktiverar vi trafik analys för en nätverks säkerhets grupp som har flödes loggning och konfigurerat trafik analyser.</span><span class="sxs-lookup"><span data-stu-id="75b5e-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="75b5e-131">I svaret ser vi att NSG har Aktiver ATS för flödes loggning men att trafikanalys är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="75b5e-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="75b5e-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75b5e-132">PARAMETERS</span></span>

### <span data-ttu-id="75b5e-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75b5e-133">-AsJob</span></span>
<span data-ttu-id="75b5e-134">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="75b5e-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75b5e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b5e-135">-DefaultProfile</span></span>
<span data-ttu-id="75b5e-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75b5e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b5e-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="75b5e-137">-EnableFlowLog</span></span>
<span data-ttu-id="75b5e-138">Flagga för att aktivera/inaktivera flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="75b5e-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="75b5e-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="75b5e-139">-EnableRetention</span></span>
<span data-ttu-id="75b5e-140">Flagga för att aktivera/inaktivera bevarande.</span><span class="sxs-lookup"><span data-stu-id="75b5e-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="75b5e-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="75b5e-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="75b5e-142">Flagga för att aktivera/inaktivera bevarande.</span><span class="sxs-lookup"><span data-stu-id="75b5e-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="75b5e-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="75b5e-143">-FormatType</span></span>
<span data-ttu-id="75b5e-144">Typ av flödes logg format.</span><span class="sxs-lookup"><span data-stu-id="75b5e-144">Type of flow log format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b5e-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="75b5e-145">-FormatVersion</span></span>
<span data-ttu-id="75b5e-146">Version av flödes logg format.</span><span class="sxs-lookup"><span data-stu-id="75b5e-146">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b5e-147">-Plats</span><span class="sxs-lookup"><span data-stu-id="75b5e-147">-Location</span></span>
<span data-ttu-id="75b5e-148">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="75b5e-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="75b5e-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75b5e-149">-NetworkWatcher</span></span>
<span data-ttu-id="75b5e-150">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="75b5e-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="75b5e-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="75b5e-151">-NetworkWatcherName</span></span>
<span data-ttu-id="75b5e-152">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="75b5e-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="75b5e-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b5e-153">-ResourceGroupName</span></span>
<span data-ttu-id="75b5e-154">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="75b5e-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="75b5e-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="75b5e-155">-RetentionInDays</span></span>
<span data-ttu-id="75b5e-156">Antalet dagar som flödes logg poster ska bevaras.</span><span class="sxs-lookup"><span data-stu-id="75b5e-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="75b5e-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="75b5e-157">-StorageAccountId</span></span>
<span data-ttu-id="75b5e-158">ID för det lagrings konto som används för att lagra flödes loggen.</span><span class="sxs-lookup"><span data-stu-id="75b5e-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="75b5e-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="75b5e-159">-TargetResourceId</span></span>
<span data-ttu-id="75b5e-160">Mål resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="75b5e-160">The target resource ID.</span></span>

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

### <span data-ttu-id="75b5e-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="75b5e-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="75b5e-162">Hämtar eller anger intervallet (i minuter) som bestämmer hur ofta du ska TA till tjänst ska utföra flödes analys.</span><span class="sxs-lookup"><span data-stu-id="75b5e-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span> <span data-ttu-id="75b5e-163">Tillåtna värden är 10 till 60 minuter.</span><span class="sxs-lookup"><span data-stu-id="75b5e-163">Supported values are 10 and 60 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b5e-164">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="75b5e-164">-Workspace</span></span>
<span data-ttu-id="75b5e-165">Det WS-objekt som används för att lagra trafikanalys data.</span><span class="sxs-lookup"><span data-stu-id="75b5e-165">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="75b5e-166">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="75b5e-166">-WorkspaceGUID</span></span>
<span data-ttu-id="75b5e-167">GUID för WS som används för att lagra trafikanalys data.</span><span class="sxs-lookup"><span data-stu-id="75b5e-167">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="75b5e-168">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="75b5e-168">-WorkspaceLocation</span></span>
<span data-ttu-id="75b5e-169">Azure-regionen i WS som används för att lagra trafikanalys data.</span><span class="sxs-lookup"><span data-stu-id="75b5e-169">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="75b5e-170">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="75b5e-170">-WorkspaceResourceId</span></span>
<span data-ttu-id="75b5e-171">Abonnemang på WS som används för att lagra trafikanalys data.</span><span class="sxs-lookup"><span data-stu-id="75b5e-171">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="75b5e-172">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75b5e-172">-Confirm</span></span>
<span data-ttu-id="75b5e-173">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75b5e-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b5e-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b5e-174">-WhatIf</span></span>
<span data-ttu-id="75b5e-175">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75b5e-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75b5e-176">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75b5e-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b5e-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b5e-177">CommonParameters</span></span>
<span data-ttu-id="75b5e-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b5e-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b5e-179">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b5e-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b5e-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75b5e-180">INPUTS</span></span>

### <span data-ttu-id="75b5e-181">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75b5e-181">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="75b5e-182">System. String</span><span class="sxs-lookup"><span data-stu-id="75b5e-182">System.String</span></span>

### <span data-ttu-id="75b5e-183">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75b5e-183">System.Boolean</span></span>

### <span data-ttu-id="75b5e-184">System. Int32</span><span class="sxs-lookup"><span data-stu-id="75b5e-184">System.Int32</span></span>

### <span data-ttu-id="75b5e-185">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="75b5e-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="75b5e-186">Microsoft. Azure. Management. Internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="75b5e-186">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="75b5e-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75b5e-187">OUTPUTS</span></span>

### <span data-ttu-id="75b5e-188">Microsoft. Azure. commands. Networks. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="75b5e-188">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="75b5e-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75b5e-189">NOTES</span></span>
<span data-ttu-id="75b5e-190">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, Watcher, flöde, loggar, flowlog, loggning</span><span class="sxs-lookup"><span data-stu-id="75b5e-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="75b5e-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75b5e-191">RELATED LINKS</span></span>

[<span data-ttu-id="75b5e-192">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75b5e-192">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="75b5e-193">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75b5e-193">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="75b5e-194">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="75b5e-194">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="75b5e-195">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="75b5e-195">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="75b5e-196">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="75b5e-196">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="75b5e-197">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="75b5e-197">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="75b5e-198">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="75b5e-198">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="75b5e-199">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75b5e-199">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75b5e-200">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="75b5e-200">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="75b5e-201">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75b5e-201">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75b5e-202">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75b5e-202">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75b5e-203">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="75b5e-203">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="75b5e-204">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="75b5e-204">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="75b5e-205">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="75b5e-205">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="75b5e-206">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="75b5e-206">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="75b5e-207">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75b5e-207">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75b5e-208">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75b5e-208">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75b5e-209">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75b5e-209">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75b5e-210">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="75b5e-210">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="75b5e-211">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75b5e-211">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75b5e-212">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75b5e-212">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="75b5e-213">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="75b5e-213">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="75b5e-214">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="75b5e-214">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="75b5e-215">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="75b5e-215">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="75b5e-216">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="75b5e-216">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="75b5e-217">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="75b5e-217">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="75b5e-218">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="75b5e-218">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
