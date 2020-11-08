---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099525"
---
# <span data-ttu-id="b20e8-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b20e8-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="b20e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b20e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b20e8-103">Kontrollerar statusen för kopierings relationer.</span><span class="sxs-lookup"><span data-stu-id="b20e8-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="b20e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b20e8-104">SYNTAX</span></span>

### <span data-ttu-id="b20e8-105">ByServerNameOnly (standard)</span><span class="sxs-lookup"><span data-stu-id="b20e8-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b20e8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b20e8-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b20e8-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="b20e8-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b20e8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b20e8-108">DESCRIPTION</span></span>
<span data-ttu-id="b20e8-109">Cmdleten **Get-AzureSqlDatabaseCopy** kontrollerar statusen för en eller flera aktiva kopierings relationer.</span><span class="sxs-lookup"><span data-stu-id="b20e8-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="b20e8-110">Kör den här cmdleten när du har kört Start-AzureSqlDatabaseCopy eller Stop-AzureSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b20e8-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="b20e8-111">Du kan kontrol lera en specifik kopierings relation, alla kopierings relationer eller en filtrerad lista över kopierings relationer, till exempel alla kopior på en specifik mål server.</span><span class="sxs-lookup"><span data-stu-id="b20e8-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="b20e8-112">Du kan köra denna cmdlet på den server som är värd för käll-eller mål databasen.</span><span class="sxs-lookup"><span data-stu-id="b20e8-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="b20e8-113">Denna cmdlet är synkron.</span><span class="sxs-lookup"><span data-stu-id="b20e8-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="b20e8-114">Cmdleten blockerar Azure PowerShell-konsolen tills den returnerar ett status-objekt.</span><span class="sxs-lookup"><span data-stu-id="b20e8-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="b20e8-115">Parametrarna *PartnerServer* och *PartnerDatabase* är valfria.</span><span class="sxs-lookup"><span data-stu-id="b20e8-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="b20e8-116">Om du inte anger någon parameter returnerar denna cmdlet en tabell med resultat.</span><span class="sxs-lookup"><span data-stu-id="b20e8-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="b20e8-117">Om du vill visa statusen för endast en viss databas anger du båda parametrarna.</span><span class="sxs-lookup"><span data-stu-id="b20e8-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="b20e8-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b20e8-118">EXAMPLES</span></span>

### <span data-ttu-id="b20e8-119">Exempel 1: få kopierings status för en databas</span><span class="sxs-lookup"><span data-stu-id="b20e8-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="b20e8-120">Det här kommandot får statusen för databasen order på den server som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="b20e8-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="b20e8-121">Parametern *PartnerServer* begränsar det här kommandot till bk0b8kf658-servern.</span><span class="sxs-lookup"><span data-stu-id="b20e8-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="b20e8-122">Exempel 2: få status för alla kopior på en serverGet status för alla kopior på en server</span><span class="sxs-lookup"><span data-stu-id="b20e8-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="b20e8-123">Det här kommandot får statusen för alla aktiva kopior på servern som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="b20e8-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="b20e8-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b20e8-124">PARAMETERS</span></span>

### <span data-ttu-id="b20e8-125">-Databas</span><span class="sxs-lookup"><span data-stu-id="b20e8-125">-Database</span></span>
<span data-ttu-id="b20e8-126">Anger ett objekt som representerar käll-Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b20e8-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="b20e8-127">Denna cmdlet hämtar kopierings statusen för databasen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b20e8-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="b20e8-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b20e8-128">-DatabaseCopy</span></span>
<span data-ttu-id="b20e8-129">Anger ett objekt som representerar en databas.</span><span class="sxs-lookup"><span data-stu-id="b20e8-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="b20e8-130">Denna cmdlet hämtar kopierings statusen för databasen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b20e8-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="b20e8-131">Den här parametern accepterar pipeline-inmatning.</span><span class="sxs-lookup"><span data-stu-id="b20e8-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="b20e8-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b20e8-132">-DatabaseName</span></span>
<span data-ttu-id="b20e8-133">Anger namnet på käll databasen.</span><span class="sxs-lookup"><span data-stu-id="b20e8-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="b20e8-134">Denna cmdlet får kopierings status för databasen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b20e8-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20e8-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="b20e8-135">-PartnerDatabase</span></span>
<span data-ttu-id="b20e8-136">Anger namnet på den sekundära databasen.</span><span class="sxs-lookup"><span data-stu-id="b20e8-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="b20e8-137">Om den här databasen inte finns i vyn sys.dm_database_copies dynamisk hantering returnerar denna cmdlet ett tomt status-objekt.</span><span class="sxs-lookup"><span data-stu-id="b20e8-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20e8-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="b20e8-138">-PartnerServer</span></span>
<span data-ttu-id="b20e8-139">Anger namnet på den server som är värd för mål databasen.</span><span class="sxs-lookup"><span data-stu-id="b20e8-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="b20e8-140">Om den här servern inte finns i vyn sys.dm_database_copies dynamisk hantering returnerar denna cmdlet ett tomt status-objekt.</span><span class="sxs-lookup"><span data-stu-id="b20e8-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20e8-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="b20e8-141">-Profile</span></span>
<span data-ttu-id="b20e8-142">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b20e8-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b20e8-143">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b20e8-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b20e8-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b20e8-144">-ServerName</span></span>
<span data-ttu-id="b20e8-145">Anger namnet på den server där databas kopian finns.</span><span class="sxs-lookup"><span data-stu-id="b20e8-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="b20e8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b20e8-146">CommonParameters</span></span>
<span data-ttu-id="b20e8-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b20e8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b20e8-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b20e8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b20e8-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b20e8-149">INPUTS</span></span>

### <span data-ttu-id="b20e8-150">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b20e8-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="b20e8-151">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="b20e8-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="b20e8-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b20e8-152">OUTPUTS</span></span>

### <span data-ttu-id="b20e8-153">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b20e8-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="b20e8-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b20e8-154">NOTES</span></span>
* <span data-ttu-id="b20e8-155">Verifiera: den här cmdleten kräver certifikatbaserad identifiering.</span><span class="sxs-lookup"><span data-stu-id="b20e8-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="b20e8-156">Ett exempel på hur certifikatbaserad verifikation används för att ange aktuell prenumeration finns i New-AzureSqlDatabaseServerContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b20e8-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="b20e8-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b20e8-157">RELATED LINKS</span></span>

[<span data-ttu-id="b20e8-158">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="b20e8-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b20e8-159">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="b20e8-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b20e8-160">Azure SQL-databas-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b20e8-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="b20e8-161">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b20e8-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="b20e8-162">Stopp-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b20e8-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


