---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093149"
---
# <span data-ttu-id="eb668-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="eb668-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="eb668-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb668-102">SYNOPSIS</span></span>
<span data-ttu-id="eb668-103">Initierar en återställnings förfrågan för en databas.</span><span class="sxs-lookup"><span data-stu-id="eb668-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="eb668-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb668-104">SYNTAX</span></span>

### <span data-ttu-id="eb668-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb668-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="eb668-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="eb668-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eb668-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb668-107">DESCRIPTION</span></span>
<span data-ttu-id="eb668-108">Cmdleten **Start-AzureSqlDatabaseRecovery** initierar en återställnings förfrågan för en Live eller avbruten databas.</span><span class="sxs-lookup"><span data-stu-id="eb668-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="eb668-109">Denna cmdlet stöder grundläggande återställning med den senaste tillgängliga säkerhets kopian av databasen.</span><span class="sxs-lookup"><span data-stu-id="eb668-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="eb668-110">Återställnings åtgärden skapar en ny databas.</span><span class="sxs-lookup"><span data-stu-id="eb668-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="eb668-111">Om du återställer en Live-databas på samma server måste du ange ett annat namn för den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="eb668-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="eb668-112">Om du vill göra en tidpunkt för återställning av en databas kan du använda cmdleten **Start-AzureSqlDatabaseRestore** istället.</span><span class="sxs-lookup"><span data-stu-id="eb668-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="eb668-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb668-113">EXAMPLES</span></span>

### <span data-ttu-id="eb668-114">Exempel 1: Återställ en databas som har angetts som ett objekt</span><span class="sxs-lookup"><span data-stu-id="eb668-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="eb668-115">Det första kommandot får ett databas objekt med cmdleten **Get-AzureSqlRecoverableDatabase** .</span><span class="sxs-lookup"><span data-stu-id="eb668-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="eb668-116">Kommandot lagrar objektet i $Database variabel.</span><span class="sxs-lookup"><span data-stu-id="eb668-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="eb668-117">Det andra kommandot återställer databasen som är lagrad i $Database.</span><span class="sxs-lookup"><span data-stu-id="eb668-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="eb668-118">Exempel 2: Återställ en databas som anges efter namn</span><span class="sxs-lookup"><span data-stu-id="eb668-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="eb668-119">Det här kommandot återställer en databas med hjälp av databas namnet.</span><span class="sxs-lookup"><span data-stu-id="eb668-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="eb668-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb668-120">PARAMETERS</span></span>

### <span data-ttu-id="eb668-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="eb668-121">-Profile</span></span>
<span data-ttu-id="eb668-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="eb668-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb668-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="eb668-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb668-124">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="eb668-124">-SourceDatabase</span></span>
<span data-ttu-id="eb668-125">Anger det databas objekt som representerar databasen som denna cmdlet återställer.</span><span class="sxs-lookup"><span data-stu-id="eb668-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb668-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb668-126">-SourceDatabaseName</span></span>
<span data-ttu-id="eb668-127">Anger namnet på den databas som denna cmdlet återställer.</span><span class="sxs-lookup"><span data-stu-id="eb668-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb668-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="eb668-128">-SourceServerName</span></span>
<span data-ttu-id="eb668-129">Anger namnet på den server där käll databasen körs, eller som käll databasen kördes innan den togs bort.</span><span class="sxs-lookup"><span data-stu-id="eb668-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb668-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb668-130">-TargetDatabaseName</span></span>
<span data-ttu-id="eb668-131">Anger namnet på den återställda databasen.</span><span class="sxs-lookup"><span data-stu-id="eb668-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="eb668-132">Om käll databasen fortfarande är aktiv, för att återställa den till samma server, måste du ange ett namn som skiljer sig från käll databasens namn.</span><span class="sxs-lookup"><span data-stu-id="eb668-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

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

### <span data-ttu-id="eb668-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="eb668-133">-TargetServerName</span></span>
<span data-ttu-id="eb668-134">Anger namnet på den server som du vill återställa en databas till.</span><span class="sxs-lookup"><span data-stu-id="eb668-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="eb668-135">Du kan återställa en databas till samma server eller till en annan server.</span><span class="sxs-lookup"><span data-stu-id="eb668-135">You can restore a database to the same server or to a different server.</span></span>

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

### <span data-ttu-id="eb668-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb668-136">CommonParameters</span></span>
<span data-ttu-id="eb668-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb668-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb668-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb668-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb668-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb668-139">INPUTS</span></span>

### <span data-ttu-id="eb668-140">Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="eb668-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="eb668-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb668-141">OUTPUTS</span></span>

### <span data-ttu-id="eb668-142">Microsoft. WindowsAzure. Management. SQL. Models. RecoverDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="eb668-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="eb668-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb668-143">NOTES</span></span>
* <span data-ttu-id="eb668-144">Du måste använda certifikatbaserad inloggningsautentisering för att köra denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb668-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="eb668-145">Kör följande kommandon på den dator där du kör denna cmdlet:</span><span class="sxs-lookup"><span data-stu-id="eb668-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="eb668-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb668-146">RELATED LINKS</span></span>

[<span data-ttu-id="eb668-147">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="eb668-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="eb668-148">Skapa begäran om databas återställning</span><span class="sxs-lookup"><span data-stu-id="eb668-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="eb668-149">Geo-replikering i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="eb668-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="eb668-150">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="eb668-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="eb668-151">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="eb668-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="eb668-152">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="eb668-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)


