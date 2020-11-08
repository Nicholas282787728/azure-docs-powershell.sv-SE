---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099633"
---
# <span data-ttu-id="da03d-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="da03d-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="da03d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da03d-102">SYNOPSIS</span></span>
<span data-ttu-id="da03d-103">Avbryter en kontinuerlig kopierings relation.</span><span class="sxs-lookup"><span data-stu-id="da03d-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="da03d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da03d-104">SYNTAX</span></span>

### <span data-ttu-id="da03d-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="da03d-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da03d-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="da03d-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da03d-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="da03d-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da03d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da03d-108">DESCRIPTION</span></span>
<span data-ttu-id="da03d-109">Cmdleten **Stop-AzureSqlDatabaseCopy** avbryter en kontinuerlig kopierings relation.</span><span class="sxs-lookup"><span data-stu-id="da03d-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="da03d-110">Denna cmdlet stoppar data förflyttningen mellan käll databasen och den sekundära databasen eller måltypen och ändrar sedan den sekundära databasens status till en fristående databas.</span><span class="sxs-lookup"><span data-stu-id="da03d-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="da03d-111">Det finns två sätt att avsluta ett fort löp ande kopierings förhållande, uppsägning eller planerad uppsägning med möjlig data förlust.</span><span class="sxs-lookup"><span data-stu-id="da03d-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="da03d-112">På den server som är värd för käll databasen kan du köra denna cmdlet i uppsägning eller framtvingat avslutnings läge.</span><span class="sxs-lookup"><span data-stu-id="da03d-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="da03d-113">På den server som är värd för den sekundära databasen måste du använda framtvingat avslutnings läge.</span><span class="sxs-lookup"><span data-stu-id="da03d-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="da03d-114">En planerad uppsägning väntar tills alla genomförda transaktioner på käll databasen, när du kör cmdleten, har repliker ATS till den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="da03d-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="da03d-115">Framtvingad uppsägning väntar inte på replikering av utestående transaktioner och kan leda till förlust av data i den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="da03d-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="da03d-116">När replikeringsstatus är pågående kan endast tvingande uppsägning avsluta en kontinuerlig kopierings relation.</span><span class="sxs-lookup"><span data-stu-id="da03d-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="da03d-117">Om replikeringsstatus är avvaktat stöds inte uppsägning som inte framtvingas.</span><span class="sxs-lookup"><span data-stu-id="da03d-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="da03d-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da03d-118">EXAMPLES</span></span>

### <span data-ttu-id="da03d-119">Exempel 1: avsluta en kontinuerlig kopierings relation</span><span class="sxs-lookup"><span data-stu-id="da03d-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="da03d-120">Det här kommandot avbryter den kontinuerliga kopierings relationen för databasen order på den server som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="da03d-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="da03d-121">Servern med namnet bk0b8kf658 är värd för den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="da03d-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="da03d-122">Exempel 2: tvinga fram en kontinuerlig kopierings relation</span><span class="sxs-lookup"><span data-stu-id="da03d-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="da03d-123">Det första kommandot får databas kopierings relationen för databasen order på den server som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="da03d-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="da03d-124">Det andra kommandot avslutar en kontinuerlig kopierings relation från den server som är värd för den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="da03d-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="da03d-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da03d-125">PARAMETERS</span></span>

### <span data-ttu-id="da03d-126">-Databas</span><span class="sxs-lookup"><span data-stu-id="da03d-126">-Database</span></span>
<span data-ttu-id="da03d-127">Anger ett objekt som representerar käll-Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="da03d-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="da03d-128">Denna cmdlet avbryter den kontinuerliga kopierings relationen för databasen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="da03d-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da03d-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="da03d-129">-DatabaseCopy</span></span>
<span data-ttu-id="da03d-130">Anger ett objekt som representerar en databas.</span><span class="sxs-lookup"><span data-stu-id="da03d-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="da03d-131">Denna cmdlet avbryter den kontinuerliga kopierings relationen för databasen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="da03d-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="da03d-132">Den här parametern accepterar pipeline-inmatning.</span><span class="sxs-lookup"><span data-stu-id="da03d-132">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da03d-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da03d-133">-DatabaseName</span></span>
<span data-ttu-id="da03d-134">Anger namnet på en databas.</span><span class="sxs-lookup"><span data-stu-id="da03d-134">Specifies the name of a database.</span></span>
<span data-ttu-id="da03d-135">Denna cmdlet avbryter den kontinuerliga kopierings relationen för databasen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="da03d-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da03d-136">-Force</span><span class="sxs-lookup"><span data-stu-id="da03d-136">-Force</span></span>
<span data-ttu-id="da03d-137">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="da03d-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da03d-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="da03d-138">-ForcedTermination</span></span>
<span data-ttu-id="da03d-139">Anger att denna cmdlet orsakar tvingande uppsägning av den kontinuerliga kopierings relationen.</span><span class="sxs-lookup"><span data-stu-id="da03d-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="da03d-140">Det kan orsaka förlust av data.</span><span class="sxs-lookup"><span data-stu-id="da03d-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="da03d-141">Om du vill köra denna cmdlet på en server som är värd för mål databasen måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="da03d-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="da03d-142">Om du vill köra denna cmdlet på en server som är värd för käll databasen, om den sekundära databasen inte är tillgänglig, måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="da03d-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="da03d-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="da03d-143">-PartnerDatabase</span></span>
<span data-ttu-id="da03d-144">Anger namnet på den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="da03d-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="da03d-145">Om du anger ett namn måste det matcha käll databasens namn.</span><span class="sxs-lookup"><span data-stu-id="da03d-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da03d-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="da03d-146">-PartnerServer</span></span>
<span data-ttu-id="da03d-147">Anger namnet på den server som är värd för mål databasen.</span><span class="sxs-lookup"><span data-stu-id="da03d-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da03d-148">-Profil</span><span class="sxs-lookup"><span data-stu-id="da03d-148">-Profile</span></span>
<span data-ttu-id="da03d-149">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="da03d-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da03d-150">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="da03d-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da03d-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da03d-151">-ServerName</span></span>
<span data-ttu-id="da03d-152">Anger namnet på den server där käll databasen finns.</span><span class="sxs-lookup"><span data-stu-id="da03d-152">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da03d-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da03d-153">-Confirm</span></span>
<span data-ttu-id="da03d-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da03d-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da03d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da03d-155">-WhatIf</span></span>
<span data-ttu-id="da03d-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da03d-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da03d-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da03d-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da03d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da03d-158">CommonParameters</span></span>
<span data-ttu-id="da03d-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da03d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da03d-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da03d-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da03d-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da03d-161">INPUTS</span></span>

### <span data-ttu-id="da03d-162">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="da03d-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="da03d-163">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="da03d-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="da03d-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da03d-164">OUTPUTS</span></span>

### <span data-ttu-id="da03d-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="da03d-165">None</span></span>

## <span data-ttu-id="da03d-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da03d-166">NOTES</span></span>
* <span data-ttu-id="da03d-167">Verifiera: den här cmdleten kräver certifikatbaserad identifiering.</span><span class="sxs-lookup"><span data-stu-id="da03d-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="da03d-168">Ett exempel på hur certifikatbaserad identifiering används för att ange aktuellt abonnemang finns i cmdleten **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="da03d-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="da03d-169">Restriktioner: på den server som är värd för den sekundära databasen kan endast tvingande uppsägning användas.</span><span class="sxs-lookup"><span data-stu-id="da03d-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="da03d-170">Konsekvenserna av uppsägningen på den tidigare sekundära databasen: efter uppsägning blir den sekundära databasen en självständig databas.</span><span class="sxs-lookup"><span data-stu-id="da03d-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="da03d-171">Om dirigering redan har slutförts på den sekundära databasen är den här databasen öppen för fullständig åtkomst efter uppsägning.</span><span class="sxs-lookup"><span data-stu-id="da03d-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="da03d-172">Om käll databasen är en skrivskyddad databas blir den tidigare sekundära databasen en skrivskyddad databas också.</span><span class="sxs-lookup"><span data-stu-id="da03d-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="da03d-173">Om dirigering pågår avbryts dirigeringen och den tidigare sekundära databasen blir aldrig synlig på den server som är värd för den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="da03d-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="da03d-174">Du kan ange skrivskyddad käll databas.</span><span class="sxs-lookup"><span data-stu-id="da03d-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="da03d-175">Detta garanterar att källan och sekundära databaser synkroniseras efter uppsägning och ser till att inga transaktioner bevaras under uppsägningen.</span><span class="sxs-lookup"><span data-stu-id="da03d-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="da03d-176">När uppsägningen är klar återställer du källan till Läs-och skriv läge.</span><span class="sxs-lookup"><span data-stu-id="da03d-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="da03d-177">Du kan också ange den tidigare sekundära databasen till Läs-och skriv läge.</span><span class="sxs-lookup"><span data-stu-id="da03d-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="da03d-178">Övervakning: Använd cmdleten **Get-AzureSqlDatabaseOperation** för att bekräfta statusen för åtgärderna på både källa och mål för den kontinuerliga kopierings relationen.</span><span class="sxs-lookup"><span data-stu-id="da03d-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="da03d-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da03d-179">RELATED LINKS</span></span>

[<span data-ttu-id="da03d-180">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="da03d-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="da03d-181">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="da03d-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="da03d-182">Stoppa databas kopiering</span><span class="sxs-lookup"><span data-stu-id="da03d-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="da03d-183">Azure SQL-databas-cmdletar</span><span class="sxs-lookup"><span data-stu-id="da03d-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="da03d-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="da03d-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="da03d-185">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="da03d-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


