---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269048"
---
# <span data-ttu-id="62e42-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62e42-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="62e42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62e42-102">SYNOPSIS</span></span>
<span data-ttu-id="62e42-103">Återställer en SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="62e42-103">Restores a SQL database.</span></span>

## <span data-ttu-id="62e42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62e42-104">SYNTAX</span></span>

### <span data-ttu-id="62e42-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62e42-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="62e42-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e42-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e42-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="62e42-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62e42-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e42-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="62e42-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e42-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e42-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="62e42-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e42-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62e42-113">DESCRIPTION</span></span>
<span data-ttu-id="62e42-114">Med cmdleten **restore-AzSqlDatabase** återställs en SQL-databas från en Geo-redundant säkerhets kopiering, en säkerhets kopia av en borttagen databas, en långsiktig säkerhets kopiering eller en tidpunkt i en Live-databas.</span><span class="sxs-lookup"><span data-stu-id="62e42-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="62e42-115">Den återställda databasen skapas som en ny databas.</span><span class="sxs-lookup"><span data-stu-id="62e42-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="62e42-116">Du kan skapa en elastisk SQL-databas genom att ange parametern *ElasticPoolName* till en befintlig elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="62e42-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="62e42-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62e42-117">EXAMPLES</span></span>

### <span data-ttu-id="62e42-118">Exempel 1: återställa en databas från en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="62e42-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="62e42-119">Det första kommandot får den SQL-databas som heter Database01 och lagrar den sedan i $Database variabel.</span><span class="sxs-lookup"><span data-stu-id="62e42-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="62e42-120">Det andra kommandot återställer databasen i $Database från den angivna säkerhets kopian under tiden till den databas som heter RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="62e42-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="62e42-121">Exempel 2: återställa en databas från en tidpunkt till en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="62e42-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="62e42-122">Det första kommandot får den SQL-databas som heter Database01 och lagrar den sedan i $Database variabel.</span><span class="sxs-lookup"><span data-stu-id="62e42-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="62e42-123">Det andra kommandot återställer databasen i $Database från den angivna säkerhets kopian under tiden till den SQL-databas som heter RestoredDatabase i den elastiska poolen med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="62e42-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="62e42-124">Exempel 3: återställa en borttagen databas</span><span class="sxs-lookup"><span data-stu-id="62e42-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="62e42-125">Det första kommandot får den borttagna databas säkerhets kopia som du vill återställa med [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="62e42-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="62e42-126">Det andra kommandot startar återställning från den borttagna databas säkerhets kopian med hjälp av cmdleten [restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="62e42-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="62e42-127">Om parametern-PointInTime inte anges kommer databasen att återställas till borttagnings tid.</span><span class="sxs-lookup"><span data-stu-id="62e42-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="62e42-128">Exempel 4: återställa en borttagen databas till en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="62e42-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="62e42-129">Det första kommandot får den borttagna databas säkerhets kopia som du vill återställa med [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="62e42-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="62e42-130">Det andra kommandot startar återställning från den borttagna databas säkerhets kopian med hjälp av [restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="62e42-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="62e42-131">Om parametern-PointInTime inte anges kommer databasen att återställas till borttagnings tid.</span><span class="sxs-lookup"><span data-stu-id="62e42-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="62e42-132">Exempel 5: Geo-Restore en databas</span><span class="sxs-lookup"><span data-stu-id="62e42-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="62e42-133">Det första kommandot får den geo-redundanta säkerhets kopieringen för databasen som heter Database01 och lagrar den sedan i $GeoBackup variabel.</span><span class="sxs-lookup"><span data-stu-id="62e42-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="62e42-134">Det andra kommandot återställer säkerhets kopian i $GeoBackup till SQL-databasen med namnet RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="62e42-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="62e42-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62e42-135">PARAMETERS</span></span>

### <span data-ttu-id="62e42-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62e42-136">-AsJob</span></span>
<span data-ttu-id="62e42-137">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="62e42-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62e42-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="62e42-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="62e42-139">Säkerhets kopians lagrings utrymme som används för att lagra säkerhets kopior för SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="62e42-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="62e42-140">Alternativen är: lokal, zon och geo.</span><span class="sxs-lookup"><span data-stu-id="62e42-140">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="62e42-141">-ComputeGeneration</span></span>
<span data-ttu-id="62e42-142">Den beräknade genereringen som ska kopplas till den återställda databasen</span><span class="sxs-lookup"><span data-stu-id="62e42-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e42-143">-DefaultProfile</span></span>
<span data-ttu-id="62e42-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="62e42-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62e42-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="62e42-145">-DeletionDate</span></span>
<span data-ttu-id="62e42-146">Anger borttagnings datumet som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="62e42-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="62e42-147">Använd Get-Date cmdlet för att få ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="62e42-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-148">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="62e42-148">-Edition</span></span>
<span data-ttu-id="62e42-149">Anger versionen av SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="62e42-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="62e42-150">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="62e42-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62e42-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="62e42-151">None</span></span>
- <span data-ttu-id="62e42-152">Basisk</span><span class="sxs-lookup"><span data-stu-id="62e42-152">Basic</span></span>
- <span data-ttu-id="62e42-153">Standar</span><span class="sxs-lookup"><span data-stu-id="62e42-153">Standard</span></span>
- <span data-ttu-id="62e42-154">Beta</span><span class="sxs-lookup"><span data-stu-id="62e42-154">Premium</span></span>
- <span data-ttu-id="62e42-155">Warehouse</span><span class="sxs-lookup"><span data-stu-id="62e42-155">DataWarehouse</span></span>
- <span data-ttu-id="62e42-156">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="62e42-156">Free</span></span>
- <span data-ttu-id="62e42-157">Sträckning</span><span class="sxs-lookup"><span data-stu-id="62e42-157">Stretch</span></span>
- <span data-ttu-id="62e42-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="62e42-158">GeneralPurpose</span></span>
- <span data-ttu-id="62e42-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="62e42-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="62e42-160">-ElasticPoolName</span></span>
<span data-ttu-id="62e42-161">Anger namnet på den elastiska pool där SQL-databasen ska placeras.</span><span class="sxs-lookup"><span data-stu-id="62e42-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="62e42-163">Anger att denna cmdlet återställer en databas från en säkerhets kopia av en borttagen SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="62e42-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="62e42-164">Du kan använda Get-AzSqlDeletedDatabaseBackup cmdlet för att hämta säkerhets kopian av en borttagen SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="62e42-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-165">-FromGeoBackup</span></span>
<span data-ttu-id="62e42-166">Anger att denna cmdlet återställer en SQL-databas från en Geo-redundant säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="62e42-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="62e42-167">Du kan använda Get-AzSqlDatabaseGeoBackup cmdlet för att få en Geo-redundant säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="62e42-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="62e42-169">Anger att den här cmdleten återställer en SQL-databas från en säkerhets kopia av en lång tids period.</span><span class="sxs-lookup"><span data-stu-id="62e42-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="62e42-171">Anger att den här cmdleten återställer en SQL-databas från en tidpunkt för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="62e42-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="62e42-172">-LicenseType</span></span>
<span data-ttu-id="62e42-173">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="62e42-173">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="62e42-174">-PointInTime</span></span>
<span data-ttu-id="62e42-175">Anger den tidpunkt som du vill återställa SQL-databasen till som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="62e42-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="62e42-176">Använd cmdleten **Get-date** för att få ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="62e42-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="62e42-177">Använd den här parametern tillsammans med parametern *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="62e42-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e42-178">-ResourceGroupName</span></span>
<span data-ttu-id="62e42-179">Anger namnet på den resurs grupp som den här cmdleten tilldelar SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="62e42-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62e42-180">-ResourceId</span></span>
<span data-ttu-id="62e42-181">Anger ID för den resurs som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="62e42-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62e42-182">-ServerName</span></span>
<span data-ttu-id="62e42-183">Anger namnet på SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="62e42-183">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="62e42-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="62e42-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="62e42-185">Anger namnet på tjänst målet.</span><span class="sxs-lookup"><span data-stu-id="62e42-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="62e42-186">-TargetDatabaseName</span></span>
<span data-ttu-id="62e42-187">Anger namnet på den databas som du vill återställa till.</span><span class="sxs-lookup"><span data-stu-id="62e42-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="62e42-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="62e42-188">-VCore</span></span>
<span data-ttu-id="62e42-189">VCore nummer för den återställda Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="62e42-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e42-190">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62e42-190">-Confirm</span></span>
<span data-ttu-id="62e42-191">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62e42-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e42-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e42-192">-WhatIf</span></span>
<span data-ttu-id="62e42-193">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62e42-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62e42-194">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62e42-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e42-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e42-195">CommonParameters</span></span>
<span data-ttu-id="62e42-196">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e42-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e42-197">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62e42-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e42-198">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62e42-198">INPUTS</span></span>

### <span data-ttu-id="62e42-199">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="62e42-199">System.DateTime</span></span>

### <span data-ttu-id="62e42-200">System. String</span><span class="sxs-lookup"><span data-stu-id="62e42-200">System.String</span></span>

## <span data-ttu-id="62e42-201">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62e42-201">OUTPUTS</span></span>

### <span data-ttu-id="62e42-202">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="62e42-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="62e42-203">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62e42-203">NOTES</span></span>

## <span data-ttu-id="62e42-204">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62e42-204">RELATED LINKS</span></span>

[<span data-ttu-id="62e42-205">Återställa en Azure SQL-databas från ett avbrott</span><span class="sxs-lookup"><span data-stu-id="62e42-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="62e42-206">Återställa en Azure SQL-databas från ett användar fel</span><span class="sxs-lookup"><span data-stu-id="62e42-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="62e42-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62e42-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="62e42-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="62e42-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="62e42-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="62e42-210">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="62e42-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

