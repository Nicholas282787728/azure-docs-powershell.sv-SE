---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: e7110511840542b8efed22b1267b76074434b94a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755573"
---
# <span data-ttu-id="30d4f-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="30d4f-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="30d4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="30d4f-103">Återställer en SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="30d4f-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30d4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30d4f-104">SYNTAX</span></span>

### <span data-ttu-id="30d4f-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30d4f-106">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30d4f-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30d4f-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30d4f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30d4f-109">DESCRIPTION</span></span>
<span data-ttu-id="30d4f-110">Med cmdleten **restore-AzureRmSqlDatabase** återställs en SQL-databas från en Geo-redundant säkerhets kopiering, en säkerhets kopia av en borttagen databas, en långsiktig säkerhets kopiering eller en tidpunkt i en Live-databas.</span><span class="sxs-lookup"><span data-stu-id="30d4f-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="30d4f-111">Den återställda databasen skapas som en ny databas.</span><span class="sxs-lookup"><span data-stu-id="30d4f-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="30d4f-112">Du kan skapa en elastisk SQL-databas genom att ange parametern *ElasticPoolName* till en befintlig elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="30d4f-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="30d4f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30d4f-113">EXAMPLES</span></span>

### <span data-ttu-id="30d4f-114">Exempel 1: återställa en databas från en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="30d4f-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="30d4f-115">Det första kommandot får den SQL-databas som heter Database01 och lagrar den sedan i $Database variabel.</span><span class="sxs-lookup"><span data-stu-id="30d4f-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="30d4f-116">Det andra kommandot återställer databasen i $Database från den angivna säkerhets kopian under tiden till den databas som heter RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="30d4f-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="30d4f-117">Exempel 2: återställa en databas från en tidpunkt till en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="30d4f-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="30d4f-118">Det första kommandot får den SQL-databas som heter Database01 och lagrar den sedan i $Database variabel.</span><span class="sxs-lookup"><span data-stu-id="30d4f-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="30d4f-119">Det andra kommandot återställer databasen i $Database från den angivna säkerhets kopian under tiden till den SQL-databas som heter RestoredDatabase i den elastiska poolen med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="30d4f-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="30d4f-120">Exempel 3: återställa en borttagen databas</span><span class="sxs-lookup"><span data-stu-id="30d4f-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="30d4f-121">Det första kommandot får den borttagna databas säkerhets kopia som du vill återställa med [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="30d4f-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="30d4f-122">Det andra kommandot startar återställning från den borttagna databas säkerhets kopian med hjälp av cmdleten [restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="30d4f-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="30d4f-123">Om parametern-PointInTime inte anges kommer databasen att återställas till borttagnings tid.</span><span class="sxs-lookup"><span data-stu-id="30d4f-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="30d4f-124">Exempel 4: återställa en borttagen databas till en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="30d4f-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="30d4f-125">Det första kommandot får den borttagna databas säkerhets kopia som du vill återställa med [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="30d4f-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="30d4f-126">Det andra kommandot startar återställning från den borttagna databas säkerhets kopian med hjälp av [restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="30d4f-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="30d4f-127">Om parametern-PointInTime inte anges kommer databasen att återställas till borttagnings tid.</span><span class="sxs-lookup"><span data-stu-id="30d4f-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="30d4f-128">Exempel 5: Geo-Restore en databas</span><span class="sxs-lookup"><span data-stu-id="30d4f-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="30d4f-129">Det första kommandot får den geo-redundanta säkerhets kopieringen för databasen som heter Database01 och lagrar den sedan i $GeoBackup variabel.</span><span class="sxs-lookup"><span data-stu-id="30d4f-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="30d4f-130">Det andra kommandot återställer säkerhets kopian i $GeoBackup till SQL-databasen med namnet RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="30d4f-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="30d4f-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30d4f-131">PARAMETERS</span></span>

### <span data-ttu-id="30d4f-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30d4f-132">-AsJob</span></span>
<span data-ttu-id="30d4f-133">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="30d4f-133">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="30d4f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d4f-134">-DefaultProfile</span></span>
<span data-ttu-id="30d4f-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="30d4f-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30d4f-136">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="30d4f-136">-DeletionDate</span></span>
<span data-ttu-id="30d4f-137">Anger borttagnings datumet som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="30d4f-137">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="30d4f-138">Använd Get-Date cmdlet för att få ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="30d4f-138">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-139">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="30d4f-139">-Edition</span></span>
<span data-ttu-id="30d4f-140">Anger versionen av SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="30d4f-140">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="30d4f-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="30d4f-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30d4f-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="30d4f-142">None</span></span>
- <span data-ttu-id="30d4f-143">Beta</span><span class="sxs-lookup"><span data-stu-id="30d4f-143">Premium</span></span>
- <span data-ttu-id="30d4f-144">Basisk</span><span class="sxs-lookup"><span data-stu-id="30d4f-144">Basic</span></span>
- <span data-ttu-id="30d4f-145">Standar</span><span class="sxs-lookup"><span data-stu-id="30d4f-145">Standard</span></span>
- <span data-ttu-id="30d4f-146">Warehouse</span><span class="sxs-lookup"><span data-stu-id="30d4f-146">DataWarehouse</span></span>
- <span data-ttu-id="30d4f-147">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="30d4f-147">Free</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-148">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="30d4f-148">-ElasticPoolName</span></span>
<span data-ttu-id="30d4f-149">Anger namnet på den elastiska pool där SQL-databasen ska placeras.</span><span class="sxs-lookup"><span data-stu-id="30d4f-149">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-150">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-150">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="30d4f-151">Anger att denna cmdlet återställer en databas från en säkerhets kopia av en borttagen SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="30d4f-151">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="30d4f-152">Du kan använda Get-AzureRMSqlDeletedDatabaseBackup cmdlet för att hämta säkerhets kopian av en borttagen SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="30d4f-152">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-153">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-153">-FromGeoBackup</span></span>
<span data-ttu-id="30d4f-154">Anger att denna cmdlet återställer en SQL-databas från en Geo-redundant säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="30d4f-154">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="30d4f-155">Du kan använda Get-AzureRMSqlDatabaseGeoBackup cmdlet för att få en Geo-redundant säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="30d4f-155">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromGeoBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-156">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-156">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="30d4f-157">Anger att den här cmdleten återställer en SQL-databas från en säkerhets kopia av en lång tids period.</span><span class="sxs-lookup"><span data-stu-id="30d4f-157">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-158">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-158">-FromPointInTimeBackup</span></span>
<span data-ttu-id="30d4f-159">Anger att den här cmdleten återställer en SQL-databas från en tidpunkt för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="30d4f-159">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-160">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="30d4f-160">-PointInTime</span></span>
<span data-ttu-id="30d4f-161">Anger den tidpunkt som du vill återställa SQL-databasen till som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="30d4f-161">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="30d4f-162">Använd cmdleten **Get-date** för att få ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="30d4f-162">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="30d4f-163">Använd den här parametern tillsammans med parametern *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="30d4f-163">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d4f-164">-ResourceGroupName</span></span>
<span data-ttu-id="30d4f-165">Anger namnet på den resurs grupp som den här cmdleten tilldelar SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="30d4f-165">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30d4f-166">-ResourceId</span></span>
<span data-ttu-id="30d4f-167">Anger ID för den resurs som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="30d4f-167">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30d4f-168">-ServerName</span></span>
<span data-ttu-id="30d4f-169">Anger namnet på SQL-serverdatabasen.</span><span class="sxs-lookup"><span data-stu-id="30d4f-169">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="30d4f-170">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="30d4f-170">-ServiceObjectiveName</span></span>
<span data-ttu-id="30d4f-171">Anger namnet på tjänst målet.</span><span class="sxs-lookup"><span data-stu-id="30d4f-171">Specifies the name of the service objective.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-172">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="30d4f-172">-TargetDatabaseName</span></span>
<span data-ttu-id="30d4f-173">Anger namnet på den databas som du vill återställa till.</span><span class="sxs-lookup"><span data-stu-id="30d4f-173">Specifies the name of the database to restore to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d4f-174">CommonParameters</span></span>
<span data-ttu-id="30d4f-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30d4f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d4f-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d4f-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d4f-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30d4f-177">INPUTS</span></span>

### <span data-ttu-id="30d4f-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="30d4f-178">None</span></span>
<span data-ttu-id="30d4f-179">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="30d4f-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30d4f-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30d4f-180">OUTPUTS</span></span>

### <span data-ttu-id="30d4f-181">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="30d4f-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="30d4f-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30d4f-182">NOTES</span></span>

## <span data-ttu-id="30d4f-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30d4f-183">RELATED LINKS</span></span>

[<span data-ttu-id="30d4f-184">Återställa en Azure SQL-databas från ett avbrott</span><span class="sxs-lookup"><span data-stu-id="30d4f-184">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="30d4f-185">Återställa en Azure SQL-databas från ett användar fel</span><span class="sxs-lookup"><span data-stu-id="30d4f-185">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="30d4f-186">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="30d4f-186">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="30d4f-187">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-187">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="30d4f-188">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="30d4f-188">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="30d4f-189">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="30d4f-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

