---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400579"
---
# <span data-ttu-id="7047d-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7047d-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="7047d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7047d-102">SYNOPSIS</span></span>
<span data-ttu-id="7047d-103">Uppdaterar flödes logg resurs.</span><span class="sxs-lookup"><span data-stu-id="7047d-103">Updates flow log resource.</span></span>

## <span data-ttu-id="7047d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7047d-104">SYNTAX</span></span>

### <span data-ttu-id="7047d-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="7047d-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7047d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7047d-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7047d-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="7047d-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7047d-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="7047d-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7047d-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7047d-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7047d-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="7047d-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7047d-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7047d-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7047d-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="7047d-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7047d-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="7047d-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7047d-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7047d-114">DESCRIPTION</span></span>
<span data-ttu-id="7047d-115">Uppdaterar flödes logg resurs.</span><span class="sxs-lookup"><span data-stu-id="7047d-115">Updates flow log resource.</span></span>

## <span data-ttu-id="7047d-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7047d-116">EXAMPLES</span></span>

### <span data-ttu-id="7047d-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7047d-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="7047d-118">Namn: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid inspirerar/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest etag: W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: lyckades: öster TargetResourceId:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/nonstorage Enabled: true RetentionPolicy: {"dagar": 0, "Enabled": false} format: {"Type": "JSON", "version": 2} FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="7047d-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="7047d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7047d-119">PARAMETERS</span></span>

### <span data-ttu-id="7047d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7047d-120">-DefaultProfile</span></span>
<span data-ttu-id="7047d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7047d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-122">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="7047d-122">-Enabled</span></span>
<span data-ttu-id="7047d-123">Flagga för att aktivera/inaktivera flödes loggning.</span><span class="sxs-lookup"><span data-stu-id="7047d-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="7047d-124">-EnableRetention</span></span>
<span data-ttu-id="7047d-125">Flagga för att aktivera/inaktivera bevarande.</span><span class="sxs-lookup"><span data-stu-id="7047d-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="7047d-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="7047d-127">Flagga för att aktivera/inaktivera TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="7047d-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-128">-Force</span><span class="sxs-lookup"><span data-stu-id="7047d-128">-Force</span></span>
<span data-ttu-id="7047d-129">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="7047d-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7047d-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="7047d-130">-FormatType</span></span>
<span data-ttu-id="7047d-131">Fil typen för flödes loggen.</span><span class="sxs-lookup"><span data-stu-id="7047d-131">The file type of flow log.</span></span>
<span data-ttu-id="7047d-132">Det enda värde som stöds är nu "JSON".</span><span class="sxs-lookup"><span data-stu-id="7047d-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="7047d-133">-FormatVersion</span></span>
<span data-ttu-id="7047d-134">Version (revision) av flödes loggen.</span><span class="sxs-lookup"><span data-stu-id="7047d-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7047d-135">-InputObject</span></span>
<span data-ttu-id="7047d-136">Flöda LOF-objekt.</span><span class="sxs-lookup"><span data-stu-id="7047d-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="7047d-137">-Location</span></span>
<span data-ttu-id="7047d-138">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="7047d-138">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="7047d-139">-Name</span></span>
<span data-ttu-id="7047d-140">Flödets logg namn.</span><span class="sxs-lookup"><span data-stu-id="7047d-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7047d-141">-NetworkWatcher</span></span>
<span data-ttu-id="7047d-142">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="7047d-142">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7047d-143">-NetworkWatcherName</span></span>
<span data-ttu-id="7047d-144">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="7047d-144">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7047d-145">-ResourceGroupName</span></span>
<span data-ttu-id="7047d-146">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7047d-146">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7047d-147">-ResourceId</span></span>
<span data-ttu-id="7047d-148">FlowLog resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7047d-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="7047d-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="7047d-150">Antalet dagar som flödes logg poster ska bevaras.</span><span class="sxs-lookup"><span data-stu-id="7047d-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="7047d-151">-StorageId</span></span>
<span data-ttu-id="7047d-152">ID för det lagrings konto som används för att lagra flödes loggen.</span><span class="sxs-lookup"><span data-stu-id="7047d-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-153">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7047d-153">-Tag</span></span>
<span data-ttu-id="7047d-154">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="7047d-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7047d-155">-TargetResourceId</span></span>
<span data-ttu-id="7047d-156">ID för nätverks säkerhets grupp som flödes logg ska användas för.</span><span class="sxs-lookup"><span data-stu-id="7047d-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="7047d-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="7047d-158">Det intervall i minuter som skulle avgöra hur ofta TA-tjänsten ska utföra flödes analys.</span><span class="sxs-lookup"><span data-stu-id="7047d-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7047d-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="7047d-160">Resurs-ID för den anslutna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="7047d-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7047d-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7047d-161">-Confirm</span></span>
<span data-ttu-id="7047d-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7047d-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7047d-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7047d-163">-WhatIf</span></span>
<span data-ttu-id="7047d-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7047d-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7047d-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7047d-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7047d-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7047d-166">CommonParameters</span></span>
<span data-ttu-id="7047d-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7047d-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7047d-168">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7047d-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7047d-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7047d-169">INPUTS</span></span>

### <span data-ttu-id="7047d-170">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7047d-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7047d-171">System. String</span><span class="sxs-lookup"><span data-stu-id="7047d-171">System.String</span></span>

### <span data-ttu-id="7047d-172">Microsoft. Azure. commands. Networks. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="7047d-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="7047d-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7047d-173">OUTPUTS</span></span>

### <span data-ttu-id="7047d-174">Microsoft. Azure. commands. Networks. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="7047d-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="7047d-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7047d-175">NOTES</span></span>

## <span data-ttu-id="7047d-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7047d-176">RELATED LINKS</span></span>

[<span data-ttu-id="7047d-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7047d-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7047d-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7047d-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7047d-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7047d-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7047d-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7047d-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7047d-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7047d-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7047d-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7047d-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7047d-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7047d-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7047d-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7047d-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7047d-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7047d-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7047d-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7047d-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7047d-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7047d-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7047d-188">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7047d-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7047d-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7047d-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7047d-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7047d-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7047d-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7047d-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7047d-192">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7047d-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7047d-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7047d-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7047d-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7047d-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7047d-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7047d-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7047d-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7047d-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7047d-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7047d-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7047d-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7047d-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7047d-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7047d-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7047d-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7047d-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7047d-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7047d-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7047d-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7047d-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7047d-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7047d-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="7047d-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7047d-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="7047d-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7047d-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="7047d-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7047d-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
