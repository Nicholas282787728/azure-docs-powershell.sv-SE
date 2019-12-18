---
title: Migreringsguide för Az 3.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 3.0 av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.openlocfilehash: e88752e0c997efc4f49161e358072803cb63450a
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182170"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="c1349-103">Migreringsguide för Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="c1349-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="c1349-104">I det här dokumentet beskrivs ändringarna mellan Az-versionerna 2.0.0 och 3.0.0</span><span class="sxs-lookup"><span data-stu-id="c1349-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="c1349-105">Migreringsguide för Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="c1349-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="c1349-106">Batch</span><span class="sxs-lookup"><span data-stu-id="c1349-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="c1349-107">Inkompatibilitet med tidigare versioner av `Az.Resources`</span><span class="sxs-lookup"><span data-stu-id="c1349-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="c1349-108">Compute</span><span class="sxs-lookup"><span data-stu-id="c1349-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="c1349-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1349-109">HDInsight</span></span>](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [<span data-ttu-id="c1349-110">IotHub</span><span class="sxs-lookup"><span data-stu-id="c1349-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="c1349-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1349-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="c1349-112">Resurser</span><span class="sxs-lookup"><span data-stu-id="c1349-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="c1349-113">Inkompatibilitet med tidigare versioner av `Az.Batch`</span><span class="sxs-lookup"><span data-stu-id="c1349-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="c1349-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1349-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="c1349-115">SQL</span><span class="sxs-lookup"><span data-stu-id="c1349-115">Sql</span></span>](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a><span data-ttu-id="c1349-116">Batch</span><span class="sxs-lookup"><span data-stu-id="c1349-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="c1349-117">`Get-AzBatchNodeAgentSku` har tagits bort och ersatts med `Get-AzBatchSupportedImage`.</span><span class="sxs-lookup"><span data-stu-id="c1349-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="c1349-118">`Get-AzBatchSupportedImage` returnerar samma data som `Get-AzBatchNodeAgentSku` men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="c1349-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="c1349-119">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="c1349-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="c1349-120">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="c1349-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-121">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="c1349-122">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="c1349-123">Tidigare version är inkompatibel med Az.Resources-modulen</span><span class="sxs-lookup"><span data-stu-id="c1349-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="c1349-124">Version 2.0.1 av modulen Az.Batch är inkompatibel med tidigare versioner (version 1.7.0 eller tidigare) av modulen Az.Resources.</span><span class="sxs-lookup"><span data-stu-id="c1349-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="c1349-125">På grund av detta går det inte att importera version 1.7.0 av modulen Az.Resources när version 2.0.1 av modulen Az.Batch har importerats.</span><span class="sxs-lookup"><span data-stu-id="c1349-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="c1349-126">Du kan åtgärda problemet genom att uppdatera modulen Az.Resources till version 1.7.1 eller senare, eller installera den senaste versionen av Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="c1349-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="c1349-127">Compute</span><span class="sxs-lookup"><span data-stu-id="c1349-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="c1349-128">Parametern `UploadSizeInBytes` används i stället för `DiskSizeGB` för `New-AzDiskConfig` när CreateOption är Upload</span><span class="sxs-lookup"><span data-stu-id="c1349-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-129">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="c1349-130">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="c1349-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1349-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="c1349-132">Uppdaterade cmdleten `Get-AzHDInsightJobOutput` för att ge stöd för detaljerad rollbaserad åtkomst till lagringsnyckeln.</span><span class="sxs-lookup"><span data-stu-id="c1349-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="c1349-133">Användare med rollerna	HDInsight-klusteroperator, Deltagare och Ägare påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="c1349-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="c1349-134">Användare med skrivskyddad åtkomst behöver ange parametern `DefaultStorageAccountKey` uttryckligen.</span><span class="sxs-lookup"><span data-stu-id="c1349-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-135">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="c1349-136">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="c1349-137">Cmdleten `Add-AzHDInsightConfigValue` tog bort alias till `Add-AzHDInsightConfigValues`.</span><span class="sxs-lookup"><span data-stu-id="c1349-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-138">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-138">Before</span></span>
<span data-ttu-id="c1349-139">Använda inaktuellt alias</span><span class="sxs-lookup"><span data-stu-id="c1349-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="c1349-140">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="c1349-141">Lade till ny `Disable-AzHDInsightMonitoring`-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1349-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="c1349-142">Använd denna cmdlet för att inaktivera övervakning i ett HDInsight-kluster (ersätter `Disable-AzHDInsightOperationsManagementSuite` och `Disable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="c1349-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-143">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="c1349-144">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="c1349-145">Lade till en ny `Enable-AzHDInsightMonitoring`-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1349-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="c1349-146">Använd denna cmdlet för att aktivera övervakning i ett HDInsight-kluster (ersätter `Enable-AzHDInsightOperationsManagementSuite` och `Enable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="c1349-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-147">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="c1349-148">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="c1349-149">Lade till en ny `Get-AzHDInsightMonitoring`-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1349-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="c1349-150">Använd denna cmdlet för att hämta status för övervakning av installation i ett Azure HDInsight-kluster (ersätter `Get-AzHDInsightOperationsManagementSuite` och `Get-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="c1349-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-151">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="c1349-152">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="c1349-153">Cmdleten `Get-HDInsightProperty` tog bort alias till `Get-AzHDInsightProperties`.</span><span class="sxs-lookup"><span data-stu-id="c1349-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-154">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-154">Before</span></span>
<span data-ttu-id="c1349-155">Använda inaktuellt alias</span><span class="sxs-lookup"><span data-stu-id="c1349-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="c1349-156">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="c1349-157">Tog bort cmdletarna `Grant-AzHDInsightRdpServicesAccess` och `Revoke-AzHDInsightRdpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="c1349-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="c1349-158">De behövs inte längre eftersom kluster som använder Windows OS-typen inte stöds.</span><span class="sxs-lookup"><span data-stu-id="c1349-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="c1349-159">Skapa ett kluster med en Linux OS-typ i stället.</span><span class="sxs-lookup"><span data-stu-id="c1349-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="c1349-160">Utdatatypen för `Remove-AzHDInsightCluster` ändrades från `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` till `bool`.</span><span class="sxs-lookup"><span data-stu-id="c1349-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-161">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="c1349-162">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="c1349-163">Cmdleten är föråldrad.</span><span class="sxs-lookup"><span data-stu-id="c1349-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="c1349-164">Det finns ingen ersättning för den.</span><span class="sxs-lookup"><span data-stu-id="c1349-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="c1349-165">Utdatatypen för `Set-AzHDInsightGatewayCredential` ändrades från `HttpConnectivitySettings` till `AzureHDInsightGatewaySettings`.</span><span class="sxs-lookup"><span data-stu-id="c1349-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="c1349-166">IotHub</span><span class="sxs-lookup"><span data-stu-id="c1349-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="c1349-167">Det här aliaset har tagits bort. Använd `New-AzIotHubImportDevice` i stället.</span><span class="sxs-lookup"><span data-stu-id="c1349-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-168">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="c1349-169">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="c1349-170">Det här aliaset har tagits bort. Använd `New-AzIotHubExportDevice` i stället.</span><span class="sxs-lookup"><span data-stu-id="c1349-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-171">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="c1349-172">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="c1349-173">Parametern `EventHubEndPointName` är föråldrad och har inte ersatts eftersom IotHub endast innehåller en inbyggd slutpunkt ("händelser") som kan hantera system- och enhetsmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="c1349-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-174">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="c1349-175">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="c1349-176">Parametern `EventHubEndPointName` är föråldrad och har inte ersatts eftersom IotHub endast innehåller en inbyggd slutpunkt ("händelser") som kan hantera system- och enhetsmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="c1349-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-177">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="c1349-178">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="c1349-179">Parametern `EventHubEndPointName` är föråldrad och har inte ersatts eftersom IotHub endast innehåller en inbyggd slutpunkt ("händelser") som kan hantera system- och enhetsmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="c1349-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-180">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="c1349-181">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="c1349-182">Parametern `OperationsMonitoringProperties` är föråldrad utan att ha ersatts eftersom IotHub inte längre använder inbyggda slutpunkter ("operationsMonitoringEvents").</span><span class="sxs-lookup"><span data-stu-id="c1349-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="c1349-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c1349-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="c1349-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` och `ASRRecoveryPlanGroup.EndGroupActions` har tagits bort från utdata.</span><span class="sxs-lookup"><span data-stu-id="c1349-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="c1349-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` och `ASRRecoveryPlanGroup.EndGroupActions` har tagits bort från utdata.</span><span class="sxs-lookup"><span data-stu-id="c1349-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="c1349-186">Parametern IncludeDiskId har ändrats för att stödja direkt skrivning till en hanterad disk i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c1349-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-187">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="c1349-188">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="c1349-189">Resurser</span><span class="sxs-lookup"><span data-stu-id="c1349-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="c1349-190">Tidigare version är inkompatibel med Az.Batch-modulen</span><span class="sxs-lookup"><span data-stu-id="c1349-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="c1349-191">Version 1.7.1 av modulen Az.Resources är inkompatibel med tidigare versioner (version 1.1.2 eller tidigare) av modulen Az.Batch.</span><span class="sxs-lookup"><span data-stu-id="c1349-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="c1349-192">På grund av detta går det inte att importera version 1.1.2 av modulen Az.Batch när version 1.7.1 av modulen Az.Resources har importerats.</span><span class="sxs-lookup"><span data-stu-id="c1349-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="c1349-193">Du kan åtgärda problemet genom att uppdatera modulen Az.Batch till version 2.0.1 eller senare, eller installera den senaste versionen av Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="c1349-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="c1349-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c1349-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="c1349-195">Tog bort `Add-ServiceFabricApplicationCertificate` eftersom det här scenariot omfattas av `Add-AzVmssSecret`.</span><span class="sxs-lookup"><span data-stu-id="c1349-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-196">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="c1349-197">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="c1349-198">SQL</span><span class="sxs-lookup"><span data-stu-id="c1349-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="c1349-199">Observera att säker anslutning är inaktuell och att kommandot därför har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="c1349-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="c1349-200">Använd bladet SQL Database i Azure-portalen för att visa anslutningssträngarna</span><span class="sxs-lookup"><span data-stu-id="c1349-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="c1349-201">Aliaset `Get-AzSqlDatabaseIndexRecommendations` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="c1349-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="c1349-202">Använd `Get-AzSqlDatabaseIndexRecommendation` i stället.</span><span class="sxs-lookup"><span data-stu-id="c1349-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="c1349-203">Aliaset `Get-AzSqlDatabaseRestorePoints` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="c1349-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="c1349-204">Använd `Get-AzSqlDatabaseRestorePoint` i stället.</span><span class="sxs-lookup"><span data-stu-id="c1349-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="c1349-205">Cmdleten `Get-AzSqlDatabaseAudit` ersätter denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1349-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="c1349-206">Utdatatypen ändras från den befintliga typen :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' till den nya typen :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', och egenskaperna `AuditState` och `StorageAccountName` tas bort.</span><span class="sxs-lookup"><span data-stu-id="c1349-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="c1349-207">och `StorageAccountSubscriptionId`.</span><span class="sxs-lookup"><span data-stu-id="c1349-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="c1349-208">Skript kan hämta lagringskontoinformation från den nya egenskapen `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="c1349-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-209">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-209">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="c1349-210">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-210">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- <span data-ttu-id="c1349-211">Cmdleten `Set-AzSqlDatabaseAudit` ersätter denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1349-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="c1349-212">Utdatatypen ändras från den befintliga typen :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' till den nya typen :'bool'</span><span class="sxs-lookup"><span data-stu-id="c1349-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-213">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-214">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="c1349-215">Cmdleten `Get-AzSqlServerAudit` ersätter denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1349-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="c1349-216">Utdatatypen ändras från den befintliga typen :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' till den nya typen :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span><span class="sxs-lookup"><span data-stu-id="c1349-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="c1349-217">Egenskaperna `AuditState`, `StorageAccountName`och `StorageAccountSubscriptionId` tas bort.</span><span class="sxs-lookup"><span data-stu-id="c1349-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="c1349-218">Skript som använder egenskaperna `StorageAccountName` och `StorageAccountSubscriptionId` kan hämta den här informationen från den nya egenskapen `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="c1349-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-219">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-219">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="c1349-220">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-220">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- <span data-ttu-id="c1349-221">Cmdleten `Set-AzSqlServerAudit` ersätter denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1349-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="c1349-222">Utdatatypen ändras från den befintliga typen :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' till den nya typen :'bool'</span><span class="sxs-lookup"><span data-stu-id="c1349-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-223">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="c1349-224">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="c1349-225">Cmdleten `Get-AzSqlServerAdvancedThreatProtectionSettings` ersätts av `Get-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-226">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="c1349-227">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="c1349-228">Cmdleten `Clear-AzSqlServerAdvancedThreatProtectionSettings` ersätts av `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-229">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="c1349-230">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="c1349-231">Cmdleten `Update-AzSqlServerAdvancedThreatProtectionSettings` ersätts av `Update-AzSqlServerAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-232">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="c1349-233">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="c1349-234">Cmdleten `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` ersätts av `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-235">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-236">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="c1349-237">Cmdleten `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` ersätts av `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-238">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="c1349-239">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="c1349-240">Cmdleten `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` ersätts av `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-241">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-242">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-243">Cmdleten `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` ersätts av `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-244">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-244">Before</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="c1349-245">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-245">After</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-246">Cmdleten `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` ersätts av `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-247">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-248">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-249">Cmdleten `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` ersätts av `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-250">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-251">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-252">Cmdleten `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` ersätts av `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-253">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-253">Before</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="c1349-254">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-254">After</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-255">Cmdleten `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` ersätts av `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-256">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-257">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-258">Cmdleten `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` ersätts av `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-259">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-260">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-261">Cmdleten `Update-AzSqlInstanceVulnerabilityAssessmentSettings` ersätts av `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-262">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-262">Before</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="c1349-263">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-263">After</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-264">Cmdleten `Get-AzSqlInstanceVulnerabilityAssessmentSettings` ersätts av `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-265">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-266">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-267">Cmdleten `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` ersätts av `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-268">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-269">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-270">Cmdleten `Update-AzSqlServerVulnerabilityAssessmentSettings` ersätts av `Update-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-271">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-271">Before</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="c1349-272">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-272">After</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-273">Cmdleten `Get-AzSqlServerVulnerabilityAssessmentSettings` ersätts av `Get-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-274">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-275">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="c1349-276">Cmdleten `Clear-AzSqlServerVulnerabilityAssessmentSettings` ersätts av `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-277">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-278">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="c1349-279">Cmdleten `Get-AzSqlServerAdvancedThreatProtectionPolicy` tas bort och ingen cmdlet ersätter den</span><span class="sxs-lookup"><span data-stu-id="c1349-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="c1349-280">Cmdleten `Get-AzSqlServerThreatDetectionPolicy` ersätts av `Get-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-281">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-281">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="c1349-282">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-282">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="c1349-283">Cmdleten `Remove-AzSqlServerThreatDetectionPolicy` ersätts av `Clear-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-284">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="c1349-285">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="c1349-286">Cmdleten `Set-AzSqlServerThreatDetectionPolicy` ersätts av `Update-AzSqlServerThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-287">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="c1349-288">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="c1349-289">Cmdleten `Get-AzSqlDatabaseThreatDetectionPolicy` ersätts av `Get-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-290">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-290">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="c1349-291">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-291">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="c1349-292">Cmdleten `Set-AzSqlDatabaseThreatDetectionPolicy` ersätts av `Update-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-293">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="c1349-294">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="c1349-295">Cmdleten `Remove-AzSqlDatabaseThreatDetectionPolicy` ersätts av `Clear-AzSqlDatabaseThreatDetectionSetting`</span><span class="sxs-lookup"><span data-stu-id="c1349-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="c1349-296">Före</span><span class="sxs-lookup"><span data-stu-id="c1349-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="c1349-297">Efter</span><span class="sxs-lookup"><span data-stu-id="c1349-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```