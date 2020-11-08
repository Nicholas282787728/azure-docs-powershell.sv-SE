---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099203"
---
# <span data-ttu-id="49ea3-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49ea3-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="49ea3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="49ea3-103">Skapar en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="49ea3-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="49ea3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49ea3-104">SYNTAX</span></span>

### <span data-ttu-id="49ea3-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="49ea3-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ea3-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="49ea3-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ea3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49ea3-107">DESCRIPTION</span></span>
<span data-ttu-id="49ea3-108">Cmdleten **New-AzureSqlDatabase** skapar en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="49ea3-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="49ea3-109">Du kan ange servern genom att använda en kontext för Server anslutning i Azure SQL som du skapar med den nya cmdleten **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="49ea3-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="49ea3-110">Om du anger Server namnet används den aktuella Azure-prenumerations informationen för att autentisera begäran om att få åtkomst till servern.</span><span class="sxs-lookup"><span data-stu-id="49ea3-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="49ea3-111">När du skapar en ny databas genom att ange en Azure SQL Database-Server skapar cmdlet **New-AzureSqlDatabase** en tillfällig anslutnings kontext med det angivna Server namnet och den aktuella Azure-prenumerations informationen för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="49ea3-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="49ea3-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49ea3-112">EXAMPLES</span></span>

### <span data-ttu-id="49ea3-113">Exempel 1: skapa en databas</span><span class="sxs-lookup"><span data-stu-id="49ea3-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="49ea3-114">Det här kommandot skapar en Azure SQL-databas med namnet database1 för $Context för Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="49ea3-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="49ea3-115">Exempel 2: skapa en databas i det aktuella abonnemanget</span><span class="sxs-lookup"><span data-stu-id="49ea3-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="49ea3-116">I det här exemplet skapas en databas med namnet database1 i den angivna Azure SQL-databas servern med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="49ea3-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="49ea3-117">Cmdleten använder den aktuella Azure-prenumerationen för att autentisera begäran om att få åtkomst till servern.</span><span class="sxs-lookup"><span data-stu-id="49ea3-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="49ea3-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49ea3-118">PARAMETERS</span></span>

### <span data-ttu-id="49ea3-119">-Sortering</span><span class="sxs-lookup"><span data-stu-id="49ea3-119">-Collation</span></span>
<span data-ttu-id="49ea3-120">Anger en sortering för den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="49ea3-120">Specifies a collation for the new database.</span></span>

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

### <span data-ttu-id="49ea3-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="49ea3-121">-ConnectionContext</span></span>
<span data-ttu-id="49ea3-122">Anger den anslutnings kontext för en server där denna cmdlet skapar en databas.</span><span class="sxs-lookup"><span data-stu-id="49ea3-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ea3-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49ea3-123">-DatabaseName</span></span>
<span data-ttu-id="49ea3-124">Anger namnet på den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="49ea3-124">Specifies the name of the new database.</span></span>

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

### <span data-ttu-id="49ea3-125">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="49ea3-125">-Edition</span></span>
<span data-ttu-id="49ea3-126">Anger versionen för den nya Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="49ea3-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="49ea3-127">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="49ea3-127">Valid values are:</span></span> 

- <span data-ttu-id="49ea3-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="49ea3-128">None</span></span>
- <span data-ttu-id="49ea3-129">Webben</span><span class="sxs-lookup"><span data-stu-id="49ea3-129">Web</span></span>
- <span data-ttu-id="49ea3-130">Uppmana</span><span class="sxs-lookup"><span data-stu-id="49ea3-130">Business</span></span>
- <span data-ttu-id="49ea3-131">Basisk</span><span class="sxs-lookup"><span data-stu-id="49ea3-131">Basic</span></span>
- <span data-ttu-id="49ea3-132">Standar</span><span class="sxs-lookup"><span data-stu-id="49ea3-132">Standard</span></span>
-  <span data-ttu-id="49ea3-133">Beta</span><span class="sxs-lookup"><span data-stu-id="49ea3-133">Premium</span></span>

<span data-ttu-id="49ea3-134">Standardvärdet är Web.</span><span class="sxs-lookup"><span data-stu-id="49ea3-134">The default value is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ea3-135">-Force</span><span class="sxs-lookup"><span data-stu-id="49ea3-135">-Force</span></span>
<span data-ttu-id="49ea3-136">Gör att åtgärden kan slutföras utan att användaren uppmanas att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="49ea3-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="49ea3-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="49ea3-137">-MaxSizeBytes</span></span>
<span data-ttu-id="49ea3-138">Anger den maximala storleken på databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="49ea3-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="49ea3-139">Du kan ange antingen den här parametern eller parametern *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="49ea3-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="49ea3-140">Se beskrivningen av *MaxSizeGB* -parametern för acceptabla värden baserat på Edition.</span><span class="sxs-lookup"><span data-stu-id="49ea3-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ea3-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="49ea3-141">-MaxSizeGB</span></span>
<span data-ttu-id="49ea3-142">Anger den maximala storleken på databasen i gigabyte.</span><span class="sxs-lookup"><span data-stu-id="49ea3-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="49ea3-143">Du kan ange antingen den här parametern eller parametern *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="49ea3-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="49ea3-144">De acceptabla värdena varierar beroende på utgåva.</span><span class="sxs-lookup"><span data-stu-id="49ea3-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="49ea3-145">Grundläggande Edition-värden: 1 eller 2</span><span class="sxs-lookup"><span data-stu-id="49ea3-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="49ea3-146">Standard Edition-värden: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 eller 250</span><span class="sxs-lookup"><span data-stu-id="49ea3-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="49ea3-147">Premium Edition-värden: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 eller 500</span><span class="sxs-lookup"><span data-stu-id="49ea3-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="49ea3-148">Web Edition-värden: 1 eller 5</span><span class="sxs-lookup"><span data-stu-id="49ea3-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="49ea3-149">Business Edition-värden: 10, 20, 30, 40, 50, 100 eller 150</span><span class="sxs-lookup"><span data-stu-id="49ea3-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ea3-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="49ea3-150">-Profile</span></span>
<span data-ttu-id="49ea3-151">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="49ea3-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49ea3-152">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="49ea3-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49ea3-153">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49ea3-153">-ServerName</span></span>
<span data-ttu-id="49ea3-154">Anger namnet på den Azure SQL-databasserver som ska innehålla den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="49ea3-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

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

### <span data-ttu-id="49ea3-155">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="49ea3-155">-ServiceObjective</span></span>
<span data-ttu-id="49ea3-156">Anger ett objekt som representerar den nya tjänstens mål (prestanda nivå) för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="49ea3-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="49ea3-157">Det här värdet representerar den resurs nivå som är kopplad till den här databasen.</span><span class="sxs-lookup"><span data-stu-id="49ea3-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="49ea3-158">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="49ea3-158">Valid values are:</span></span> 

<span data-ttu-id="49ea3-159">Grundläggande: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c (S0): f1173c43-91bd-4AAA-973c-54e79e15235b standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \* standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="49ea3-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="49ea3-160">\* Standard (S3) är en del av den senaste SQL-V12 (för hands version).</span><span class="sxs-lookup"><span data-stu-id="49ea3-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="49ea3-161">Mer information finns i Nyheter i för hands versionen av V12 för Azure SQL Database https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="49ea3-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ea3-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49ea3-162">-Confirm</span></span>
<span data-ttu-id="49ea3-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49ea3-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ea3-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ea3-164">-WhatIf</span></span>
<span data-ttu-id="49ea3-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49ea3-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ea3-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49ea3-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ea3-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ea3-167">CommonParameters</span></span>
<span data-ttu-id="49ea3-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ea3-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ea3-169">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ea3-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ea3-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49ea3-170">INPUTS</span></span>

## <span data-ttu-id="49ea3-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49ea3-171">OUTPUTS</span></span>

### <span data-ttu-id="49ea3-172">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="49ea3-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="49ea3-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49ea3-173">NOTES</span></span>
* <span data-ttu-id="49ea3-174">Använd Remove-AzureSqlDatabase cmdlet för att ta bort en databas som har skapats av **New-AzureSqlDatabase**.</span><span class="sxs-lookup"><span data-stu-id="49ea3-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="49ea3-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49ea3-175">RELATED LINKS</span></span>

[<span data-ttu-id="49ea3-176">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="49ea3-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="49ea3-177">Skapa databas</span><span class="sxs-lookup"><span data-stu-id="49ea3-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="49ea3-178">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="49ea3-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="49ea3-179">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49ea3-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="49ea3-180">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="49ea3-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="49ea3-181">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49ea3-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="49ea3-182">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49ea3-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


