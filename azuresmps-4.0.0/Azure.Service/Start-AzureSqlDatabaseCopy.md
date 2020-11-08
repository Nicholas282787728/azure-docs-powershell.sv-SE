---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099075"
---
# <span data-ttu-id="11f63-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="11f63-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="11f63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11f63-102">SYNOPSIS</span></span>
<span data-ttu-id="11f63-103">Startar en kopiering av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="11f63-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="11f63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11f63-104">SYNTAX</span></span>

### <span data-ttu-id="11f63-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="11f63-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f63-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="11f63-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f63-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="11f63-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11f63-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="11f63-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11f63-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11f63-109">DESCRIPTION</span></span>
<span data-ttu-id="11f63-110">Cmdleten **Start-AzureSqlDatabaseCopy** startar en kopiering en gång eller en kontinuerlig kopiering av en specifik Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="11f63-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="11f63-111">Denna cmdlet är inte transaktionell.</span><span class="sxs-lookup"><span data-stu-id="11f63-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="11f63-112">Den ursprungliga databasen är käll databasen.</span><span class="sxs-lookup"><span data-stu-id="11f63-112">The original database is the source database.</span></span>
<span data-ttu-id="11f63-113">Kopian är den sekundära eller mål databasen.</span><span class="sxs-lookup"><span data-stu-id="11f63-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="11f63-114">För en kontinuerlig kopiering kan käll-och mål databaserna inte finnas på samma server och servrar som är värdar för käll-och mål databaserna måste ingå i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="11f63-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="11f63-115">Om du inte anger parametern *ContinuousCopy* skapar denna cmdlet en en kopia av käll databasen.</span><span class="sxs-lookup"><span data-stu-id="11f63-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="11f63-116">När svaret tas emot kan operationen fortfarande fortsätta.</span><span class="sxs-lookup"><span data-stu-id="11f63-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="11f63-117">Du kan övervaka åtgärden med hjälp av Get-AzureSqlDatabaseCopy eller Get-AzureSqlDatabaseOperation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11f63-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="11f63-118">Om du anger *ContinuousCopy* skapar denna cmdlet en kontinuerlig kopia av käll databasen.</span><span class="sxs-lookup"><span data-stu-id="11f63-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="11f63-119">När svaret tas emot behandlas åtgärden.</span><span class="sxs-lookup"><span data-stu-id="11f63-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="11f63-120">Du kan övervaka åtgärden genom att använda **Get-AzureSqlDatabaseCopy** eller **Get-AzureSqlDatabaseOperation**.</span><span class="sxs-lookup"><span data-stu-id="11f63-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="11f63-121">Du kan skapa en kontinuerlig kopia som en online-eller frånkopplad databas.</span><span class="sxs-lookup"><span data-stu-id="11f63-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="11f63-122">Den kontinuerliga kopian online används för att konfigurera Active Geo-Replication för Azure SQL Database https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .</span><span class="sxs-lookup"><span data-stu-id="11f63-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="11f63-123">Den kontinuerliga kopian offline används för att konfigurera standard Geo-Replication för Azure SQL Database https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .</span><span class="sxs-lookup"><span data-stu-id="11f63-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="11f63-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11f63-124">EXAMPLES</span></span>

### <span data-ttu-id="11f63-125">Exempel 1: tidsplanera en kontinuerlig kopia av en databas</span><span class="sxs-lookup"><span data-stu-id="11f63-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="11f63-126">Det här kommandot schemalägger en kontinuerlig kopia av databasen order på den server som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="11f63-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="11f63-127">Kommandot skapar en mål databas på den server som heter bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="11f63-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="11f63-128">Exempel 2: skapa en enstaka kopia på samma server</span><span class="sxs-lookup"><span data-stu-id="11f63-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="11f63-129">Det här kommandot skapar en enstaka kopia av databasen order på den server som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="11f63-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="11f63-130">Kommandot skapar en kopia med namnet OrdersCopy på samma server.</span><span class="sxs-lookup"><span data-stu-id="11f63-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="11f63-131">Exempel 3: schemalägga en kontinuerlig kopia av en offlinedatabas</span><span class="sxs-lookup"><span data-stu-id="11f63-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="11f63-132">Det här kommandot schemalägger en kontinuerlig kopia av databasen order på den server som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="11f63-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="11f63-133">Det här kommandot skapar en offlinedatabas för mål på servern med namnet bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="11f63-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="11f63-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11f63-134">PARAMETERS</span></span>

### <span data-ttu-id="11f63-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="11f63-135">-ContinuousCopy</span></span>
<span data-ttu-id="11f63-136">Visar att databas kopian kommer att vara en kopia (en replik databas).</span><span class="sxs-lookup"><span data-stu-id="11f63-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="11f63-137">Kontinuerlig kopiering stöds inte på samma server.</span><span class="sxs-lookup"><span data-stu-id="11f63-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="11f63-138">Om den här parametern inte anges utförs en kopiering i taget.</span><span class="sxs-lookup"><span data-stu-id="11f63-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="11f63-139">För en enstaka kopia måste käll-och partner databaserna finnas på samma server.</span><span class="sxs-lookup"><span data-stu-id="11f63-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f63-140">-Databas</span><span class="sxs-lookup"><span data-stu-id="11f63-140">-Database</span></span>
<span data-ttu-id="11f63-141">Anger ett objekt som representerar käll-Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="11f63-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="11f63-142">Den här parametern accepterar pipeline-inmatning.</span><span class="sxs-lookup"><span data-stu-id="11f63-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11f63-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="11f63-143">-DatabaseName</span></span>
<span data-ttu-id="11f63-144">Anger namnet på käll databasen.</span><span class="sxs-lookup"><span data-stu-id="11f63-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f63-145">-Force</span><span class="sxs-lookup"><span data-stu-id="11f63-145">-Force</span></span>
<span data-ttu-id="11f63-146">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="11f63-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11f63-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="11f63-147">-OfflineSecondary</span></span>
<span data-ttu-id="11f63-148">Anger att en kontinuerlig kopia är en passiv kopia i stället för en aktiv kopia.</span><span class="sxs-lookup"><span data-stu-id="11f63-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="11f63-149">Om käll databasen är en vanlig versions databas är den här parametern obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="11f63-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="11f63-150">Om du anger den här parametern måste du också ange *ContinuousCopy* .</span><span class="sxs-lookup"><span data-stu-id="11f63-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f63-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="11f63-151">-PartnerDatabase</span></span>
<span data-ttu-id="11f63-152">Anger namnet på mål databasen.</span><span class="sxs-lookup"><span data-stu-id="11f63-152">Specifies name of the target database.</span></span>
<span data-ttu-id="11f63-153">Om du anger parametern *ContinuousCopy* måste värdet för *PartnerDatabase* matcha namnet på käll databasen.</span><span class="sxs-lookup"><span data-stu-id="11f63-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="11f63-154">Om du inte anger *ContinuousCopy* måste du ange ett namn för mål databasen, som kan skilja sig från käll databasens namn.</span><span class="sxs-lookup"><span data-stu-id="11f63-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f63-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="11f63-155">-PartnerServer</span></span>
<span data-ttu-id="11f63-156">Anger namnet på den server som är värd för mål databasen.</span><span class="sxs-lookup"><span data-stu-id="11f63-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="11f63-157">Den här servern måste finnas i samma Azure-abonnemang som käll databas servern.</span><span class="sxs-lookup"><span data-stu-id="11f63-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f63-158">-Profil</span><span class="sxs-lookup"><span data-stu-id="11f63-158">-Profile</span></span>
<span data-ttu-id="11f63-159">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="11f63-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11f63-160">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="11f63-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11f63-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="11f63-161">-ServerName</span></span>
<span data-ttu-id="11f63-162">Anger namnet på den server där käll databasen finns.</span><span class="sxs-lookup"><span data-stu-id="11f63-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="11f63-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11f63-163">-Confirm</span></span>
<span data-ttu-id="11f63-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11f63-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11f63-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11f63-165">-WhatIf</span></span>
<span data-ttu-id="11f63-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11f63-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11f63-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11f63-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11f63-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f63-168">CommonParameters</span></span>
<span data-ttu-id="11f63-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f63-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f63-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f63-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f63-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11f63-171">INPUTS</span></span>

### <span data-ttu-id="11f63-172">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="11f63-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="11f63-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11f63-173">OUTPUTS</span></span>

### <span data-ttu-id="11f63-174">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="11f63-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="11f63-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11f63-175">NOTES</span></span>
* <span data-ttu-id="11f63-176">Verifiera: den här cmdleten kräver certifikatbaserad identifiering.</span><span class="sxs-lookup"><span data-stu-id="11f63-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="11f63-177">Ett exempel på hur certifikatbaserad identifiering används för att ange aktuell prenumeration finns i New-AzureSqlDatabaseServerContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11f63-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="11f63-178">Övervakning: Använd cmdleten **Get-AzureSqlDatabaseCopy** för att kontrol lera status för en eller flera kontinuerliga kopior som är aktiva på servern.</span><span class="sxs-lookup"><span data-stu-id="11f63-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="11f63-179">Använd cmdleten **Get-AzureSqlDatabaseOperation** för att kontrol lera status för åtgärderna på både källa och mål för den kontinuerliga kopierings relationen.</span><span class="sxs-lookup"><span data-stu-id="11f63-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="11f63-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11f63-180">RELATED LINKS</span></span>

[<span data-ttu-id="11f63-181">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="11f63-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="11f63-182">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="11f63-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="11f63-183">Starta databas kopiering</span><span class="sxs-lookup"><span data-stu-id="11f63-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="11f63-184">Azure SQL-databas-cmdletar</span><span class="sxs-lookup"><span data-stu-id="11f63-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="11f63-185">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="11f63-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="11f63-186">Stopp-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="11f63-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


