---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099095"
---
# <span data-ttu-id="812fc-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="812fc-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="812fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="812fc-102">SYNOPSIS</span></span>
<span data-ttu-id="812fc-103">Anger egenskaper för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="812fc-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="812fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="812fc-104">SYNTAX</span></span>

### <span data-ttu-id="812fc-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="812fc-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="812fc-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="812fc-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="812fc-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="812fc-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="812fc-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="812fc-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="812fc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="812fc-109">DESCRIPTION</span></span>
<span data-ttu-id="812fc-110">Cmdleten **set-AzureSqlDatabase** anger egenskaper för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="812fc-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="812fc-111">Du kan ange databasen efter namn eller skicka ett Azure SQL-databasobjekt genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="812fc-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="812fc-112">Du kan ange servern efter namn eller överföra en Azure SQL Database Server-kontext.</span><span class="sxs-lookup"><span data-stu-id="812fc-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="812fc-113">Skapa en anslutnings kontext genom att köra cmdleten **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="812fc-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="812fc-114">Om du anger server med namn använder cmdlet den aktuella Azure-prenumerations informationen för att autentisera begäran.</span><span class="sxs-lookup"><span data-stu-id="812fc-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="812fc-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="812fc-115">EXAMPLES</span></span>

### <span data-ttu-id="812fc-116">Exempel 1: ändra storleken på en databas med hjälp av en anslutnings kontext</span><span class="sxs-lookup"><span data-stu-id="812fc-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="812fc-117">I det här exemplet ändras storleken på databasen som heter Database01 till 20 GB i $Context kontexten för anslutning till SQL-.</span><span class="sxs-lookup"><span data-stu-id="812fc-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="812fc-118">Exempel 2: ändra storleken på en databas med hjälp av ett server namn</span><span class="sxs-lookup"><span data-stu-id="812fc-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="812fc-119">I det här exemplet ändras storleken på databasen som heter Database01 till 20 GB i servern lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="812fc-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="812fc-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="812fc-120">PARAMETERS</span></span>

### <span data-ttu-id="812fc-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="812fc-121">-ConnectionContext</span></span>
<span data-ttu-id="812fc-122">Anger en servers anslutning.</span><span class="sxs-lookup"><span data-stu-id="812fc-122">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="812fc-123">-Databas</span><span class="sxs-lookup"><span data-stu-id="812fc-123">-Database</span></span>
<span data-ttu-id="812fc-124">Anger ett objekt som representerar den Azure SQL-databas som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="812fc-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="812fc-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="812fc-125">-DatabaseName</span></span>
<span data-ttu-id="812fc-126">Anger namnet på den databas som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="812fc-126">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812fc-127">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="812fc-127">-Edition</span></span>
<span data-ttu-id="812fc-128">Anger den nya versionen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="812fc-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="812fc-129">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="812fc-129">Valid values are:</span></span> 

- <span data-ttu-id="812fc-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="812fc-130">None</span></span>
- <span data-ttu-id="812fc-131">Webben</span><span class="sxs-lookup"><span data-stu-id="812fc-131">Web</span></span>
- <span data-ttu-id="812fc-132">Uppmana</span><span class="sxs-lookup"><span data-stu-id="812fc-132">Business</span></span>
- <span data-ttu-id="812fc-133">Basisk</span><span class="sxs-lookup"><span data-stu-id="812fc-133">Basic</span></span>
- <span data-ttu-id="812fc-134">Standar</span><span class="sxs-lookup"><span data-stu-id="812fc-134">Standard</span></span>
-  <span data-ttu-id="812fc-135">Beta</span><span class="sxs-lookup"><span data-stu-id="812fc-135">Premium</span></span>

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

### <span data-ttu-id="812fc-136">-Force</span><span class="sxs-lookup"><span data-stu-id="812fc-136">-Force</span></span>
<span data-ttu-id="812fc-137">Gör det möjligt att slutföra åtgärden utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="812fc-137">Allows the action to complete without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="812fc-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="812fc-138">-MaxSizeBytes</span></span>
<span data-ttu-id="812fc-139">Anger den nya maximala storleken för databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="812fc-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="812fc-140">Du kan ange antingen den här parametern eller parametern *MaxSizeGB* .</span><span class="sxs-lookup"><span data-stu-id="812fc-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="812fc-141">Se *MaxSizeGB* -parametern för acceptabla värden baserat på Edition.</span><span class="sxs-lookup"><span data-stu-id="812fc-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="812fc-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="812fc-142">-MaxSizeGB</span></span>
<span data-ttu-id="812fc-143">Anger den nya maximala storleken för databasen i gigabyte.</span><span class="sxs-lookup"><span data-stu-id="812fc-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="812fc-144">Du kan ange antingen den här parametern eller parametern *MaxSizeBytes* .</span><span class="sxs-lookup"><span data-stu-id="812fc-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="812fc-145">De acceptabla värdena varierar beroende på utgåva.</span><span class="sxs-lookup"><span data-stu-id="812fc-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="812fc-146">Grundläggande Edition-värden: 1 eller 2</span><span class="sxs-lookup"><span data-stu-id="812fc-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="812fc-147">Standard Edition-värden: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 eller 250</span><span class="sxs-lookup"><span data-stu-id="812fc-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="812fc-148">Premium Edition-värden: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 eller 500</span><span class="sxs-lookup"><span data-stu-id="812fc-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="812fc-149">Web Edition-värden: 1 eller 5</span><span class="sxs-lookup"><span data-stu-id="812fc-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="812fc-150">Business Edition-värden: 10, 20, 30, 40, 50, 100 eller 150</span><span class="sxs-lookup"><span data-stu-id="812fc-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="812fc-151">-NewDatabaseName</span><span class="sxs-lookup"><span data-stu-id="812fc-151">-NewDatabaseName</span></span>
<span data-ttu-id="812fc-152">Anger det nya namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="812fc-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812fc-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="812fc-153">-PassThru</span></span>
<span data-ttu-id="812fc-154">Returnerar den uppdaterade Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="812fc-154">Returns the updated Azure SQL Database.</span></span>

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

### <span data-ttu-id="812fc-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="812fc-155">-Profile</span></span>
<span data-ttu-id="812fc-156">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="812fc-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="812fc-157">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="812fc-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="812fc-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="812fc-158">-ServerName</span></span>
<span data-ttu-id="812fc-159">Anger namnet på den server som innehåller databasen som ändras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="812fc-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="812fc-160">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="812fc-160">-ServiceObjective</span></span>
<span data-ttu-id="812fc-161">Anger ett objekt som representerar det nya tjänst målet (prestanda nivå) för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="812fc-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="812fc-162">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="812fc-162">Valid values are:</span></span> 

- <span data-ttu-id="812fc-163">Grundläggande: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="812fc-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="812fc-164">Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="812fc-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="812fc-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="812fc-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="812fc-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="812fc-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="812fc-167">\* Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="812fc-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="812fc-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="812fc-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="812fc-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="812fc-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="812fc-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="812fc-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="812fc-171">\* Standard (S3) är en del av den senaste SQL-V12 (för hands version).</span><span class="sxs-lookup"><span data-stu-id="812fc-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="812fc-172">Mer information finns i Nyheter i för hands versionen av V12 för Azure SQL Database https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="812fc-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="812fc-173">-Synkronisera</span><span class="sxs-lookup"><span data-stu-id="812fc-173">-Sync</span></span>
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

### <span data-ttu-id="812fc-174">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="812fc-174">-Confirm</span></span>
<span data-ttu-id="812fc-175">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="812fc-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="812fc-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="812fc-176">-WhatIf</span></span>
<span data-ttu-id="812fc-177">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="812fc-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="812fc-178">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="812fc-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="812fc-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812fc-179">CommonParameters</span></span>
<span data-ttu-id="812fc-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="812fc-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812fc-181">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="812fc-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812fc-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="812fc-182">INPUTS</span></span>

### <span data-ttu-id="812fc-183">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="812fc-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="812fc-184">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="812fc-184">OUTPUTS</span></span>

### <span data-ttu-id="812fc-185">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="812fc-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="812fc-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="812fc-186">NOTES</span></span>

## <span data-ttu-id="812fc-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="812fc-187">RELATED LINKS</span></span>

[<span data-ttu-id="812fc-188">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="812fc-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="812fc-189">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="812fc-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="812fc-190">Uppdatera databas</span><span class="sxs-lookup"><span data-stu-id="812fc-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="812fc-191">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="812fc-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="812fc-192">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="812fc-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="812fc-193">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="812fc-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="812fc-194">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="812fc-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


