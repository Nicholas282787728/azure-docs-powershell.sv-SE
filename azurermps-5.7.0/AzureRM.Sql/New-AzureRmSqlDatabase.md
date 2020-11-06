---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: f5fc78f3e06150f3283e35c23bf80edce4f47650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580948"
---
# <span data-ttu-id="e6fae-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6fae-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="e6fae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6fae-102">SYNOPSIS</span></span>
<span data-ttu-id="e6fae-103">Skapar en databas eller en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="e6fae-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6fae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6fae-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6fae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6fae-105">DESCRIPTION</span></span>
<span data-ttu-id="e6fae-106">Cmdleten **New-AzureRmSqlDatabase** skapar en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e6fae-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="e6fae-107">Du kan också skapa en elastisk databas genom att ange parametern *ElasticPoolName* till en befintlig elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="e6fae-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="e6fae-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6fae-108">EXAMPLES</span></span>

### <span data-ttu-id="e6fae-109">Exempel 1: skapa en databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="e6fae-109">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="e6fae-110">Det här kommandot skapar en databas som heter Database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="e6fae-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="e6fae-111">Exempel 2: skapa en elastisk databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="e6fae-111">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="e6fae-112">Det här kommandot skapar en databas med namnet Database01 i den Elastic pool som heter ElasticPool01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="e6fae-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="e6fae-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6fae-113">PARAMETERS</span></span>

### <span data-ttu-id="e6fae-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6fae-114">-AsJob</span></span>
<span data-ttu-id="e6fae-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e6fae-115">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="e6fae-116">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="e6fae-116">-CatalogCollation</span></span>
<span data-ttu-id="e6fae-117">Anger namnet på SQL-databasens katalog sortering.</span><span class="sxs-lookup"><span data-stu-id="e6fae-117">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="e6fae-118">-CollationName</span><span class="sxs-lookup"><span data-stu-id="e6fae-118">-CollationName</span></span>
<span data-ttu-id="e6fae-119">Anger namnet på sorteringen i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e6fae-119">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="e6fae-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6fae-120">-DatabaseName</span></span>
<span data-ttu-id="e6fae-121">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="e6fae-121">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6fae-122">-DefaultProfile</span></span>
<span data-ttu-id="e6fae-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e6fae-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6fae-124">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="e6fae-124">-Edition</span></span>
<span data-ttu-id="e6fae-125">Anger vilken utgåva som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="e6fae-125">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="e6fae-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e6fae-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6fae-127">Vis</span><span class="sxs-lookup"><span data-stu-id="e6fae-127">Default</span></span>
- <span data-ttu-id="e6fae-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="e6fae-128">None</span></span>
- <span data-ttu-id="e6fae-129">Beta</span><span class="sxs-lookup"><span data-stu-id="e6fae-129">Premium</span></span>
- <span data-ttu-id="e6fae-130">Basisk</span><span class="sxs-lookup"><span data-stu-id="e6fae-130">Basic</span></span>
- <span data-ttu-id="e6fae-131">Standar</span><span class="sxs-lookup"><span data-stu-id="e6fae-131">Standard</span></span>
- <span data-ttu-id="e6fae-132">Warehouse</span><span class="sxs-lookup"><span data-stu-id="e6fae-132">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fae-133">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e6fae-133">-ElasticPoolName</span></span>
<span data-ttu-id="e6fae-134">Anger namnet på den elastiska pool som databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="e6fae-134">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="e6fae-135">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e6fae-135">-MaxSizeBytes</span></span>
<span data-ttu-id="e6fae-136">Anger den maximala storleken på databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="e6fae-136">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="e6fae-137">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="e6fae-137">-ReadScale</span></span>
<span data-ttu-id="e6fae-138">Alternativet Läs skalning för att tilldela en Azure SQL-databas. (Aktiverat/inaktiverat)</span><span class="sxs-lookup"><span data-stu-id="e6fae-138">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fae-139">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e6fae-139">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="e6fae-140">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="e6fae-140">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="e6fae-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fae-141">-ResourceGroupName</span></span>
<span data-ttu-id="e6fae-142">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="e6fae-142">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e6fae-143">-SampleName</span><span class="sxs-lookup"><span data-stu-id="e6fae-143">-SampleName</span></span>
<span data-ttu-id="e6fae-144">Namnet på det exempel schema som ska användas när databasen skapas.</span><span class="sxs-lookup"><span data-stu-id="e6fae-144">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fae-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6fae-145">-ServerName</span></span>
<span data-ttu-id="e6fae-146">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="e6fae-146">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fae-147">-Taggar</span><span class="sxs-lookup"><span data-stu-id="e6fae-147">-Tags</span></span>
<span data-ttu-id="e6fae-148">Anger en ord lista med par med nyckelord i form av en hash-tabell som denna cmdlet associerar med den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="e6fae-148">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="e6fae-149">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e6fae-149">For example:</span></span>

<span data-ttu-id="e6fae-150">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e6fae-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6fae-151">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e6fae-151">-ZoneRedundant</span></span>
<span data-ttu-id="e6fae-152">Zonens redundans som ska kopplas till Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="e6fae-152">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="e6fae-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6fae-153">-Confirm</span></span>
<span data-ttu-id="e6fae-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6fae-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6fae-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6fae-155">-WhatIf</span></span>
<span data-ttu-id="e6fae-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6fae-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6fae-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6fae-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6fae-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fae-158">CommonParameters</span></span>
<span data-ttu-id="e6fae-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6fae-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fae-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6fae-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fae-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6fae-161">INPUTS</span></span>

### <span data-ttu-id="e6fae-162">Ingen</span><span class="sxs-lookup"><span data-stu-id="e6fae-162">None</span></span>
<span data-ttu-id="e6fae-163">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e6fae-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6fae-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6fae-164">OUTPUTS</span></span>

### <span data-ttu-id="e6fae-165">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e6fae-165">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e6fae-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6fae-166">NOTES</span></span>

## <span data-ttu-id="e6fae-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6fae-167">RELATED LINKS</span></span>

[<span data-ttu-id="e6fae-168">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6fae-168">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="e6fae-169">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e6fae-169">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e6fae-170">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="e6fae-170">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="e6fae-171">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6fae-171">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="e6fae-172">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6fae-172">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="e6fae-173">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6fae-173">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="e6fae-174">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6fae-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="e6fae-175">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e6fae-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
