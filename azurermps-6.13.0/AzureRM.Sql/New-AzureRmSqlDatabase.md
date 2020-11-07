---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757335"
---
# <span data-ttu-id="53010-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="53010-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="53010-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53010-102">SYNOPSIS</span></span>
<span data-ttu-id="53010-103">Skapar en databas eller en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="53010-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53010-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53010-104">SYNTAX</span></span>

### <span data-ttu-id="53010-105">DtuBasedDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="53010-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53010-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="53010-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53010-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53010-107">DESCRIPTION</span></span>
<span data-ttu-id="53010-108">Cmdleten **New-AzureRmSqlDatabase** skapar en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="53010-108">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="53010-109">Du kan också skapa en elastisk databas genom att ange parametern *ElasticPoolName* till en befintlig elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="53010-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="53010-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53010-110">EXAMPLES</span></span>

### <span data-ttu-id="53010-111">Exempel 1: skapa en databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="53010-111">Example 1: Create a database on a specified server</span></span>
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
LicenseType                   :
Tags                          :
```

<span data-ttu-id="53010-112">Det här kommandot skapar en databas som heter Database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="53010-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="53010-113">Exempel 2: skapa en elastisk databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="53010-113">Example 2: Create an elastic database on a specified server</span></span>
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
LicenseType                   :
Tags                          :
```

<span data-ttu-id="53010-114">Det här kommandot skapar en databas med namnet Database02 i den Elastic pool som heter ElasticPool01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="53010-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="53010-115">Exempel 3: skapa en vCore-databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="53010-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="53010-116">Det här kommandot skapar en vCore-databas som heter Database03 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="53010-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="53010-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53010-117">PARAMETERS</span></span>

### <span data-ttu-id="53010-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53010-118">-AsJob</span></span>
<span data-ttu-id="53010-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="53010-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="53010-120">-CatalogCollation</span></span>
<span data-ttu-id="53010-121">Anger namnet på SQL-databasens katalog sortering.</span><span class="sxs-lookup"><span data-stu-id="53010-121">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="53010-122">-CollationName</span></span>
<span data-ttu-id="53010-123">Anger namnet på sorteringen i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="53010-123">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="53010-124">-ComputeGeneration</span></span>
<span data-ttu-id="53010-125">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="53010-125">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53010-126">-DatabaseName</span></span>
<span data-ttu-id="53010-127">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="53010-127">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53010-128">-DefaultProfile</span></span>
<span data-ttu-id="53010-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="53010-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-130">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="53010-130">-Edition</span></span>
<span data-ttu-id="53010-131">Anger vilken utgåva som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="53010-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="53010-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="53010-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="53010-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="53010-133">None</span></span>
- <span data-ttu-id="53010-134">Basisk</span><span class="sxs-lookup"><span data-stu-id="53010-134">Basic</span></span>
- <span data-ttu-id="53010-135">Standar</span><span class="sxs-lookup"><span data-stu-id="53010-135">Standard</span></span>
- <span data-ttu-id="53010-136">Beta</span><span class="sxs-lookup"><span data-stu-id="53010-136">Premium</span></span>
- <span data-ttu-id="53010-137">Warehouse</span><span class="sxs-lookup"><span data-stu-id="53010-137">DataWarehouse</span></span>
- <span data-ttu-id="53010-138">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="53010-138">Free</span></span>
- <span data-ttu-id="53010-139">Sträckning</span><span class="sxs-lookup"><span data-stu-id="53010-139">Stretch</span></span>
- <span data-ttu-id="53010-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="53010-140">GeneralPurpose</span></span>
- <span data-ttu-id="53010-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="53010-141">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="53010-142">-ElasticPoolName</span></span>
<span data-ttu-id="53010-143">Anger namnet på den elastiska pool som databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="53010-143">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="53010-144">-LicenseType</span></span>
<span data-ttu-id="53010-145">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="53010-145">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-146">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="53010-146">-MaxSizeBytes</span></span>
<span data-ttu-id="53010-147">Anger den maximala storleken på databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="53010-147">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-148">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="53010-148">-ReadScale</span></span>
<span data-ttu-id="53010-149">Alternativet Läs skalning för att tilldela en Azure SQL-databas. (Aktiverat/inaktiverat)</span><span class="sxs-lookup"><span data-stu-id="53010-149">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-150">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="53010-150">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="53010-151">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="53010-151">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53010-152">-ResourceGroupName</span></span>
<span data-ttu-id="53010-153">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="53010-153">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53010-154">-SampleName</span><span class="sxs-lookup"><span data-stu-id="53010-154">-SampleName</span></span>
<span data-ttu-id="53010-155">Namnet på det exempel schema som ska användas när databasen skapas.</span><span class="sxs-lookup"><span data-stu-id="53010-155">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="53010-156">-ServerName</span></span>
<span data-ttu-id="53010-157">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="53010-157">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53010-158">-Taggar</span><span class="sxs-lookup"><span data-stu-id="53010-158">-Tags</span></span>
<span data-ttu-id="53010-159">Anger en ord lista med par med nyckelord i form av en hash-tabell som denna cmdlet associerar med den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="53010-159">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="53010-160">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="53010-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="53010-161">-VCore</span></span>
<span data-ttu-id="53010-162">VCore-numret för Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="53010-162">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="53010-163">-ZoneRedundant</span></span>
<span data-ttu-id="53010-164">Zonens redundans som ska kopplas till Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="53010-164">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53010-165">-Confirm</span></span>
<span data-ttu-id="53010-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53010-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53010-167">-WhatIf</span></span>
<span data-ttu-id="53010-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53010-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53010-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53010-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53010-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53010-170">CommonParameters</span></span>
<span data-ttu-id="53010-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53010-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53010-172">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53010-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53010-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53010-173">INPUTS</span></span>

### <span data-ttu-id="53010-174">System. String</span><span class="sxs-lookup"><span data-stu-id="53010-174">System.String</span></span>

## <span data-ttu-id="53010-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53010-175">OUTPUTS</span></span>

### <span data-ttu-id="53010-176">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="53010-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="53010-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53010-177">NOTES</span></span>

## <span data-ttu-id="53010-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53010-178">RELATED LINKS</span></span>

[<span data-ttu-id="53010-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="53010-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="53010-180">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="53010-180">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="53010-181">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="53010-181">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="53010-182">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="53010-182">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="53010-183">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="53010-183">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="53010-184">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="53010-184">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="53010-185">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="53010-185">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="53010-186">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="53010-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

