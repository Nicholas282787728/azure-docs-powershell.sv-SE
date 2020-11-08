---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093152"
---
# <span data-ttu-id="c22e5-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="c22e5-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="c22e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c22e5-102">SYNOPSIS</span></span>
<span data-ttu-id="c22e5-103">Utför en tidpunkt för återställning av en databas.</span><span class="sxs-lookup"><span data-stu-id="c22e5-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="c22e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c22e5-104">SYNTAX</span></span>

### <span data-ttu-id="c22e5-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c22e5-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c22e5-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c22e5-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c22e5-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c22e5-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c22e5-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c22e5-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c22e5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c22e5-109">DESCRIPTION</span></span>
<span data-ttu-id="c22e5-110">Cmdleten **Start-AzureSqlDatabaseRestore** utför en tidpunkt för återställning av en bas-, standard-eller Premium-databas.</span><span class="sxs-lookup"><span data-stu-id="c22e5-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="c22e5-111">Azure SQL Database behåller grundläggande säkerhets kopiering av databaser 7 dagar, standard i 14 dagar och Premium för 35 dagar.</span><span class="sxs-lookup"><span data-stu-id="c22e5-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="c22e5-112">Återställnings åtgärden skapar en ny databas.</span><span class="sxs-lookup"><span data-stu-id="c22e5-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="c22e5-113">Om käll databasen inte tas bort måste *SourceDatabaseName* -och *TargetDatabaseName* -parametern ha olika värden.</span><span class="sxs-lookup"><span data-stu-id="c22e5-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="c22e5-114">Azure SQL Database stöder för närvarande inte återställning mellan servrar.</span><span class="sxs-lookup"><span data-stu-id="c22e5-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="c22e5-115">Namnet på käll-och mål servern måste vara samma.</span><span class="sxs-lookup"><span data-stu-id="c22e5-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="c22e5-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c22e5-116">EXAMPLES</span></span>

### <span data-ttu-id="c22e5-117">Exempel 1: återställa en databas som angetts som ett objekt till en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="c22e5-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="c22e5-118">Det första kommandot får ett databas objekt för databasen som heter Database17 på servern Server01 och lagrar det sedan i $Database variabel.</span><span class="sxs-lookup"><span data-stu-id="c22e5-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="c22e5-119">Det andra kommandot återställer databasen till en viss tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="c22e5-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="c22e5-120">Kommandot anger namnet på den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="c22e5-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="c22e5-121">Exempel 2: återställa en databas som anges efter namn till en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="c22e5-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="c22e5-122">Det här kommandot återställer databasen med namnet Database17 till en viss tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="c22e5-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="c22e5-123">Kommandot anger namnet på den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="c22e5-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="c22e5-124">Exempel 3: återställa en borttagen databas som angetts som ett objekt till en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="c22e5-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="c22e5-125">Det första kommandot får ett databas objekt för databasen som heter Database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="c22e5-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="c22e5-126">Kommandot anger parametern *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="c22e5-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="c22e5-127">Därför får cmdleten restorable tappad databas den angivna återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="c22e5-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="c22e5-128">Kommandot lagrar databasobjektet i $Database variabel.</span><span class="sxs-lookup"><span data-stu-id="c22e5-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="c22e5-129">Det andra kommandot återställer den avbrutna databasen som anges av $Database.</span><span class="sxs-lookup"><span data-stu-id="c22e5-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="c22e5-130">Kommandot anger namnet på den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="c22e5-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="c22e5-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c22e5-131">PARAMETERS</span></span>

### <span data-ttu-id="c22e5-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="c22e5-132">-PointInTime</span></span>
<span data-ttu-id="c22e5-133">Anger återställnings punkten som databasen ska återställas till.</span><span class="sxs-lookup"><span data-stu-id="c22e5-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="c22e5-134">När återställningen är slutförd återställs databasen till den status den hade vid det datum och den tid som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c22e5-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="c22e5-135">För en Live-databas som används som standard till den aktuella tiden och för en borttagen databas använder denna cmdlet den tid då databasen släpptes.</span><span class="sxs-lookup"><span data-stu-id="c22e5-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e5-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="c22e5-136">-Profile</span></span>
<span data-ttu-id="c22e5-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c22e5-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c22e5-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c22e5-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e5-139">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="c22e5-139">-RestorableDropped</span></span>
<span data-ttu-id="c22e5-140">Anger att den här cmdleten återställer en restorable tappad databas.</span><span class="sxs-lookup"><span data-stu-id="c22e5-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e5-141">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="c22e5-141">-SourceDatabase</span></span>
<span data-ttu-id="c22e5-142">Anger namnet på den databas som denna cmdlet återställer.</span><span class="sxs-lookup"><span data-stu-id="c22e5-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c22e5-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="c22e5-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="c22e5-144">Anger datum och tid när databasen togs bort.</span><span class="sxs-lookup"><span data-stu-id="c22e5-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="c22e5-145">Du måste inkludera millisekunder om du anger tiden för att matcha den faktiska borttagnings tiden för databasen.</span><span class="sxs-lookup"><span data-stu-id="c22e5-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e5-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c22e5-146">-SourceDatabaseName</span></span>
<span data-ttu-id="c22e5-147">Anger namnet på den Live-databas som denna cmdlet återställer.</span><span class="sxs-lookup"><span data-stu-id="c22e5-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e5-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="c22e5-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="c22e5-149">Anger ett objekt som representerar den restorable-släppta databasen som lagras i den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c22e5-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="c22e5-150">För att få ett **RestorableDroppedDatabase** -objekt, Använd cmdleten Get-AzureSqlDatabase och ange parametern *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="c22e5-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c22e5-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="c22e5-151">-SourceServerName</span></span>
<span data-ttu-id="c22e5-152">Anger namnet på den server där käll databasen körs, eller som käll databasen kördes innan den togs bort.</span><span class="sxs-lookup"><span data-stu-id="c22e5-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e5-153">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c22e5-153">-TargetDatabaseName</span></span>
<span data-ttu-id="c22e5-154">Anger namnet på den nya databasen som återställnings åtgärden skapar.</span><span class="sxs-lookup"><span data-stu-id="c22e5-154">Specifies the name of the new database that the restore operation creates.</span></span>

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

### <span data-ttu-id="c22e5-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="c22e5-155">-TargetServerName</span></span>
<span data-ttu-id="c22e5-156">Anger namnet på den server där denna cmdlet återställer databasen.</span><span class="sxs-lookup"><span data-stu-id="c22e5-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="c22e5-157">Azure SQL Database stöder för närvarande inte återställning mellan servrar.</span><span class="sxs-lookup"><span data-stu-id="c22e5-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="c22e5-158">Namnet på käll-och mål servern måste vara samma.</span><span class="sxs-lookup"><span data-stu-id="c22e5-158">The source and target server names must be the same.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e5-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22e5-159">CommonParameters</span></span>
<span data-ttu-id="c22e5-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c22e5-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22e5-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c22e5-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22e5-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c22e5-162">INPUTS</span></span>

### <span data-ttu-id="c22e5-163">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="c22e5-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="c22e5-164">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="c22e5-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="c22e5-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c22e5-165">OUTPUTS</span></span>

### <span data-ttu-id="c22e5-166">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. RestoreDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="c22e5-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="c22e5-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c22e5-167">NOTES</span></span>
* <span data-ttu-id="c22e5-168">Du måste använda certifikatbaserad inloggningsautentisering för att köra denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c22e5-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="c22e5-169">Kör följande kommandon på den dator där kör denna cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c22e5-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="c22e5-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c22e5-170">RELATED LINKS</span></span>

[<span data-ttu-id="c22e5-171">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="c22e5-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c22e5-172">Skapa en begäran om databas återställning</span><span class="sxs-lookup"><span data-stu-id="c22e5-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="c22e5-173">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="c22e5-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c22e5-174">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c22e5-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


