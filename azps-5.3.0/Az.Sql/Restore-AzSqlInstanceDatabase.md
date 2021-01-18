---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: 9b87539335752b07b6c03852f30959b13de4c06e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520499"
---
# <span data-ttu-id="a633b-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a633b-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="a633b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a633b-102">SYNOPSIS</span></span>
<span data-ttu-id="a633b-103">Återställer en Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="a633b-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="a633b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a633b-104">SYNTAX</span></span>

### <span data-ttu-id="a633b-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="a633b-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a633b-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="a633b-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a633b-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a633b-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a633b-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="a633b-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a633b-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="a633b-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a633b-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a633b-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a633b-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="a633b-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a633b-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="a633b-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a633b-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a633b-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a633b-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a633b-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a633b-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="a633b-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-Name] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a633b-116">LongTermRetentionBackupRestoreParameter</span><span class="sxs-lookup"><span data-stu-id="a633b-116">LongTermRetentionBackupRestoreParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromLongTermRetentionBackup] [-SubscriptionId <String>] [-ResourceId] <String>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a633b-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a633b-117">DESCRIPTION</span></span>
<span data-ttu-id="a633b-118">Cmdleten **restore-AzSqlInstanceDatabase** återställer en instans databas från en Geo-redundant säkerhets kopiering, en tidpunkt i en Live-databas eller en långsiktig säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="a633b-118">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup, a point in time in a live database, or a long term retention backup.</span></span>
<span data-ttu-id="a633b-119">Den återställda databasen skapas som en ny instans databas.</span><span class="sxs-lookup"><span data-stu-id="a633b-119">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="a633b-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a633b-120">EXAMPLES</span></span>

### <span data-ttu-id="a633b-121">Exempel 1: Återställ en instans databas från en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="a633b-121">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="a633b-122">Kommandot återställer instans databasens Database01 från den angivna säkerhets kopian under tiden till instans databasen med namnet Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="a633b-122">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="a633b-123">Exempel 2: återställa en instans databas från en tidpunkt till en annan instans i en annan resurs grupp</span><span class="sxs-lookup"><span data-stu-id="a633b-123">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="a633b-124">Kommandot återställer instans databasen Database01 på instans managedInstance1 i resurs grupp ResourceGroup01 från den angivna säkerhets kopian under tiden till instans databasen med namnet Database01_restored på instans managedInstance2 på resurs grupp ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="a633b-124">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="a633b-125">Exempel 3: Geo-Restore en instans databas</span><span class="sxs-lookup"><span data-stu-id="a633b-125">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="a633b-126">Det första kommandot får den geo-redundanta säkerhets kopieringen för databasen som heter Database01 och lagrar den sedan i $GeoBackup variabel.</span><span class="sxs-lookup"><span data-stu-id="a633b-126">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="a633b-127">Det andra kommandot återställer säkerhets kopian i $GeoBackup till instans databasen med namnet Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="a633b-127">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="a633b-128">Exempel 4: återställa en borttagen instans databas från en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="a633b-128">Example 4: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -FromPointInTimeBackup -Name $deletedDatabase.Name -InstanceName $deletedDatabase.ManagedInstanceName -ResourceGroupName $deletedDatabase.ResourceGroupName -DeletionDate $deletedDatabase.DeletionDate -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="a633b-129">Det första kommandot får de borttagna instans databaserna "DB1" på instansen "managedInstance1".</span><span class="sxs-lookup"><span data-stu-id="a633b-129">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="a633b-130">Det andra kommandot återställer den hämtade databasen, från den angivna säkerhets kopian under tiden till instans databasen med namnet Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="a633b-130">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="a633b-131">Exempel 5: återställa en borttagen instans databas från en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="a633b-131">Example 5: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -FromPointInTimeBackup -InputObject $deletedDatabase[0] -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="a633b-132">Det första kommandot får de borttagna instans databaserna "DB1" på instansen "managedInstance1".</span><span class="sxs-lookup"><span data-stu-id="a633b-132">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="a633b-133">Det andra kommandot återställer den hämtade databasen, från den angivna säkerhets kopian under tiden till instans databasen med namnet Database01_restored med hjälp av indata.</span><span class="sxs-lookup"><span data-stu-id="a633b-133">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored using input object.</span></span>

### <span data-ttu-id="a633b-134">Exempel 6: återställa en databas från vä-hö-säkerhetskopiering.</span><span class="sxs-lookup"><span data-stu-id="a633b-134">Example 6: Restore a database from LTR backup.</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -FromLongTermRetentionBackup -ResourceId /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManagedInstances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000 -TargetInstanceDatabaseName restoreTarget -TargetInstanceName testInstance -TargetResourceGroupName testResourceGroup


Location                          : southeastasia
Tags                              :
Collation                         : SQL_Latin1_General_CP1_CI_AS
Status                            : Online
RestorePointInTime                :
DefaultSecondaryLocation          : northeurope
CatalogCollation                  :
CreateMode                        :
StorageContainerUri               :
StorageContainerSasToken          :
SourceDatabaseId                  :
FailoverGroupId                   :
RecoverableDatabaseId             :
RestorableDroppedDatabaseId       :
LongTermRetentionBackupResourceId :
ResourceGroupName                 : testResourceGroup
ManagedInstanceName               : testInstance
Name                              : restoreTarget
CreationDate                      : 3/4/2020 8:12:56 AM
EarliestRestorePoint              : 3/4/2020 8:14:29 AM
Id                                : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/managedInstances/testInstance/databases/restoreTarget
```

<span data-ttu-id="a633b-135">Återställer vä-hö-säkerhetskopiering med angivet resurs-ID (som du kan hitta genom att köra Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span><span class="sxs-lookup"><span data-stu-id="a633b-135">Restores LTR backup with the given resource ID (which can be found by running Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span></span>

## <span data-ttu-id="a633b-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a633b-136">PARAMETERS</span></span>

### <span data-ttu-id="a633b-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a633b-137">-AsJob</span></span>
<span data-ttu-id="a633b-138">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a633b-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a633b-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a633b-139">-DefaultProfile</span></span>
<span data-ttu-id="a633b-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a633b-140">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="a633b-141">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="a633b-141">-DeletionDate</span></span>
<span data-ttu-id="a633b-142">Borttagnings datumet för den borttagna databasen.</span><span class="sxs-lookup"><span data-stu-id="a633b-142">The deletion date of deleted database.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-143">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a633b-143">-FromGeoBackup</span></span>
<span data-ttu-id="a633b-144">Återställ från en geo-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="a633b-144">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-145">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a633b-145">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="a633b-146">Återställ från en långsiktig säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="a633b-146">Restore from a Long Term Retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-147">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="a633b-147">-FromPointInTimeBackup</span></span>
<span data-ttu-id="a633b-148">Återställ från en säkerhets kopia under tiden.</span><span class="sxs-lookup"><span data-stu-id="a633b-148">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-149">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="a633b-149">-GeoBackupObject</span></span>
<span data-ttu-id="a633b-150">Det återställnings bara instans databas objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="a633b-150">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-151">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a633b-151">-InputObject</span></span>
<span data-ttu-id="a633b-152">Instans databas objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="a633b-152">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-153">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a633b-153">-InstanceName</span></span>
<span data-ttu-id="a633b-154">Instans namnet.</span><span class="sxs-lookup"><span data-stu-id="a633b-154">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-155">-Namn</span><span class="sxs-lookup"><span data-stu-id="a633b-155">-Name</span></span>
<span data-ttu-id="a633b-156">Instans databas namn som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="a633b-156">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName, SourceInstanceDatabaseName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-157">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="a633b-157">-PointInTime</span></span>
<span data-ttu-id="a633b-158">Tidpunkten då databasen återställs till.</span><span class="sxs-lookup"><span data-stu-id="a633b-158">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a633b-159">-ResourceGroupName</span></span>
<span data-ttu-id="a633b-160">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a633b-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a633b-161">-ResourceId</span></span>
<span data-ttu-id="a633b-162">Resurs-ID för instans databas objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="a633b-162">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a633b-163">-SubscriptionId</span></span>
<span data-ttu-id="a633b-164">ID för käll prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a633b-164">Source subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, LongTermRetentionBackupRestoreParameter
Aliases: SourceSubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-165">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a633b-165">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="a633b-166">Namnet på mål instans databasen som ska återställas till.</span><span class="sxs-lookup"><span data-stu-id="a633b-166">The name of the target instance database to restore to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-167">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="a633b-167">-TargetInstanceName</span></span>
<span data-ttu-id="a633b-168">Namnet på mål instansen som ska återställas till.</span><span class="sxs-lookup"><span data-stu-id="a633b-168">The name of the target instance to restore to.</span></span>
<span data-ttu-id="a633b-169">Om det inte anges är mål förekomsten samma som käll instansen.</span><span class="sxs-lookup"><span data-stu-id="a633b-169">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-170">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a633b-170">-TargetResourceGroupName</span></span>
<span data-ttu-id="a633b-171">Namnet på mål resurs gruppen som du vill återställa till.</span><span class="sxs-lookup"><span data-stu-id="a633b-171">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="a633b-172">Om det inte anges är mål resurs gruppen samma som käll resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a633b-172">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a633b-173">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a633b-173">-Confirm</span></span>
<span data-ttu-id="a633b-174">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a633b-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a633b-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a633b-175">-WhatIf</span></span>
<span data-ttu-id="a633b-176">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a633b-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a633b-177">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a633b-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a633b-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a633b-178">CommonParameters</span></span>
<span data-ttu-id="a633b-179">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a633b-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a633b-180">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a633b-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a633b-181">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a633b-181">INPUTS</span></span>

### <span data-ttu-id="a633b-182">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a633b-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="a633b-183">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a633b-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="a633b-184">System. String</span><span class="sxs-lookup"><span data-stu-id="a633b-184">System.String</span></span>

## <span data-ttu-id="a633b-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a633b-185">OUTPUTS</span></span>

### <span data-ttu-id="a633b-186">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a633b-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a633b-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a633b-187">NOTES</span></span>

## <span data-ttu-id="a633b-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a633b-188">RELATED LINKS</span></span>
