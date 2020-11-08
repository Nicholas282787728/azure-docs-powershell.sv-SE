---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099528"
---
# <span data-ttu-id="58142-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58142-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="58142-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58142-102">SYNOPSIS</span></span>
<span data-ttu-id="58142-103">Hämtar en eller flera databaser.</span><span class="sxs-lookup"><span data-stu-id="58142-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="58142-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58142-104">SYNTAX</span></span>

### <span data-ttu-id="58142-105">ByConnectionContext (standard)</span><span class="sxs-lookup"><span data-stu-id="58142-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="58142-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="58142-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="58142-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58142-107">DESCRIPTION</span></span>
<span data-ttu-id="58142-108">Cmdleten **Get-AzureSqlDatabase** returnerar en eller flera instanser av en Azure SQL-databas från en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="58142-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="58142-109">Du kan ange den server som du vill använda för att skapa en Azure SQL Database Server-kontext som du skapar via cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="58142-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="58142-110">Om du anger namnet på en Azure SQL-databas server används den aktuella Azure-prenumerations informationen för att autentisera begäran om att få åtkomst till servern.</span><span class="sxs-lookup"><span data-stu-id="58142-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="58142-111">Om du inte anger en databas returnerar cmdleten **Get-AzureSqlDatabase** alla databaser från den angivna servern.</span><span class="sxs-lookup"><span data-stu-id="58142-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="58142-112">Hämtar restorable tappade databaser:</span><span class="sxs-lookup"><span data-stu-id="58142-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="58142-113">Hämta restorable tappade databaser genom att använda parametern *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="58142-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="58142-114">Om du vill returnera alla restorable tappade databaser använder du parametern *RestorableDropped* utan *databasename* och *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="58142-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="58142-115">Om du vill returnera en viss restorable tappad databas använder du parametern *RestorableDropped* med parametrarna *databasename* och *DatabaseDeletionDate* .</span><span class="sxs-lookup"><span data-stu-id="58142-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="58142-116">När du hämtar en specifik restorable-avbruten databas med parametern *databasename* måste du också inkludera parametern *DatabaseDeletionDate* och det angivna *DatabaseDeletionDate* -värdet måste innehålla millisekunder för att matcha den önskade databasen.</span><span class="sxs-lookup"><span data-stu-id="58142-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="58142-117">Cmdleten **Get-AzureSqlDatabase** returnerar antingen alla restorable-förlorade databaser på en server eller en specifik databas som matchar både *databasename* och *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="58142-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="58142-118">Om du vill returnera restorable tappade databaser som uppfyller olika villkor, till exempel alla restorable-förlorade databaser med ett visst namn, måste du returnera alla restorable-förlorade databaser och sedan filtrera resultaten på klienten.</span><span class="sxs-lookup"><span data-stu-id="58142-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="58142-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58142-119">EXAMPLES</span></span>

### <span data-ttu-id="58142-120">Exempel 1: Hämta alla databaser på en server</span><span class="sxs-lookup"><span data-stu-id="58142-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="58142-121">Det här kommandot hämtar alla databaser på servern som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="58142-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="58142-122">Exempel 2: Hämta alla restorable tappade databaser på en server</span><span class="sxs-lookup"><span data-stu-id="58142-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="58142-123">Det här kommandot hämtar alla restorable tappade databaser på servern med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="58142-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="58142-124">Exempel 3: Hämta en databas från en server som anges av en anslutnings kontext</span><span class="sxs-lookup"><span data-stu-id="58142-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="58142-125">Det här kommandot hämtar databasen som heter Database01 från den server som anges av kontexten för anslutning $Context.</span><span class="sxs-lookup"><span data-stu-id="58142-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="58142-126">Exempel 4: lagra ett databas objekt i en variabel</span><span class="sxs-lookup"><span data-stu-id="58142-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="58142-127">Det här kommandot hämtar databasen med namnet Database01 från servern med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="58142-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="58142-128">Kommandot lagrar databasobjektet i variabeln $Database 01.</span><span class="sxs-lookup"><span data-stu-id="58142-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="58142-129">Exempel 5: Hämta en restorable tappad databas</span><span class="sxs-lookup"><span data-stu-id="58142-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="58142-130">Det här kommandot hämtar den restorable tappade databasen med namnet Database01 som togs bort på 11/9/2012 från servern med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="58142-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="58142-131">Det här kommandot lagrar resultatet i variabeln $DroppedDB.</span><span class="sxs-lookup"><span data-stu-id="58142-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="58142-132">Exempel 6: Hämta alla restorable tappade databaser på en server och filtrera resultaten</span><span class="sxs-lookup"><span data-stu-id="58142-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="58142-133">Det här kommandot hämtar alla restorable tappade databaser på servern med namnet lpqd0zbr8y och filtrerar sedan resultatet till de databaser som heter ContactDB.</span><span class="sxs-lookup"><span data-stu-id="58142-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="58142-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58142-134">PARAMETERS</span></span>

### <span data-ttu-id="58142-135">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="58142-135">-ConnectionContext</span></span>
<span data-ttu-id="58142-136">Anger den anslutnings kontext för en server som en databas ska hämtas från.</span><span class="sxs-lookup"><span data-stu-id="58142-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58142-137">-Databas</span><span class="sxs-lookup"><span data-stu-id="58142-137">-Database</span></span>
<span data-ttu-id="58142-138">Anger ett objekt som representerar databasen som hämtas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58142-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58142-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="58142-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="58142-140">Anger datum och tid för en borttagning.</span><span class="sxs-lookup"><span data-stu-id="58142-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="58142-141">Om du anger parametern *RestorableDropped* anger du den här parametern för att hämta en restorable-frånkopplad databas utifrån borttagnings datum och-tid.</span><span class="sxs-lookup"><span data-stu-id="58142-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="58142-142">Parametern *DatabaseDeletionDate* måste innehålla millisekunder för att matcha tiden för den önskade databasen.</span><span class="sxs-lookup"><span data-stu-id="58142-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="58142-143">Om du anger ett värde utan millisekunder hittas inte databasen.</span><span class="sxs-lookup"><span data-stu-id="58142-143">Specifying a value without milliseconds results in the database not being found.</span></span>

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

### <span data-ttu-id="58142-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="58142-144">-DatabaseName</span></span>
<span data-ttu-id="58142-145">Anger namnet på den databas som cmdleten returnerar.</span><span class="sxs-lookup"><span data-stu-id="58142-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="58142-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="58142-146">-Profile</span></span>
<span data-ttu-id="58142-147">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="58142-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58142-148">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="58142-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58142-149">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="58142-149">-RestorableDropped</span></span>
<span data-ttu-id="58142-150">Anger att denna cmdlet returnerar *RestorableDroppedDatabase* -objekt i stället för *databas* objekt.</span><span class="sxs-lookup"><span data-stu-id="58142-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="58142-151">Du kan använda parametern *DatabaseDeletionDate* för att välja en specifik restorable-förlorad databas.</span><span class="sxs-lookup"><span data-stu-id="58142-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

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

### <span data-ttu-id="58142-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="58142-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="58142-153">Anger ett objekt som representerar den restorable-släppta databasen som hämtas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58142-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58142-154">-ServerName</span><span class="sxs-lookup"><span data-stu-id="58142-154">-ServerName</span></span>
<span data-ttu-id="58142-155">Anger namnet på den server som innehåller databasen som hämtas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58142-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="58142-156">Cmdleten använder det aktuella Azure-abonnemanget för att komma åt servern.</span><span class="sxs-lookup"><span data-stu-id="58142-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58142-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58142-157">CommonParameters</span></span>
<span data-ttu-id="58142-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58142-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58142-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58142-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58142-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58142-160">INPUTS</span></span>

### <span data-ttu-id="58142-161">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="58142-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="58142-162">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="58142-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="58142-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58142-163">OUTPUTS</span></span>

### <span data-ttu-id="58142-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="58142-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="58142-165">Denna cmdlet returnerar ett *databas* objekt om du inte anger parametern *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="58142-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="58142-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="58142-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="58142-167">Denna cmdlet returnerar ett *RestorableDroppedDatabase* -objekt om du anger parametern *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="58142-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="58142-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58142-168">NOTES</span></span>

## <span data-ttu-id="58142-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58142-169">RELATED LINKS</span></span>

[<span data-ttu-id="58142-170">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="58142-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="58142-171">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="58142-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="58142-172">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58142-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="58142-173">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="58142-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="58142-174">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58142-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="58142-175">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58142-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


