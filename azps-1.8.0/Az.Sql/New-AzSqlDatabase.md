---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746634"
---
# <span data-ttu-id="7dd69-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7dd69-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="7dd69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7dd69-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd69-103">Skapar en databas eller en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="7dd69-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="7dd69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7dd69-104">SYNTAX</span></span>

### <span data-ttu-id="7dd69-105">DtuBasedDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="7dd69-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dd69-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="7dd69-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dd69-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7dd69-107">DESCRIPTION</span></span>
<span data-ttu-id="7dd69-108">Cmdleten **New-AzSqlDatabase** skapar en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="7dd69-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="7dd69-109">Du kan också skapa en elastisk databas genom att ange parametern *ElasticPoolName* till en befintlig elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="7dd69-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="7dd69-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7dd69-110">EXAMPLES</span></span>

### <span data-ttu-id="7dd69-111">Exempel 1: skapa en databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="7dd69-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="7dd69-112">Det här kommandot skapar en databas som heter Database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="7dd69-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="7dd69-113">Exempel 2: skapa en elastisk databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="7dd69-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="7dd69-114">Det här kommandot skapar en databas med namnet Database02 i den Elastic pool som heter ElasticPool01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="7dd69-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="7dd69-115">Exempel 3: skapa en vCore-databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="7dd69-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
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

<span data-ttu-id="7dd69-116">Det här kommandot skapar en vCore-databas som heter Database03 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="7dd69-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="7dd69-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7dd69-117">PARAMETERS</span></span>

### <span data-ttu-id="7dd69-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dd69-118">-AsJob</span></span>
<span data-ttu-id="7dd69-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7dd69-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7dd69-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="7dd69-120">-CatalogCollation</span></span>
<span data-ttu-id="7dd69-121">Anger namnet på SQL-databasens katalog sortering.</span><span class="sxs-lookup"><span data-stu-id="7dd69-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="7dd69-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="7dd69-122">-CollationName</span></span>
<span data-ttu-id="7dd69-123">Anger namnet på sorteringen i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="7dd69-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="7dd69-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="7dd69-124">-ComputeGeneration</span></span>
<span data-ttu-id="7dd69-125">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="7dd69-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="7dd69-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7dd69-126">-DatabaseName</span></span>
<span data-ttu-id="7dd69-127">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="7dd69-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="7dd69-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd69-128">-DefaultProfile</span></span>
<span data-ttu-id="7dd69-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7dd69-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dd69-130">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="7dd69-130">-Edition</span></span>
<span data-ttu-id="7dd69-131">Anger vilken utgåva som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="7dd69-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="7dd69-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7dd69-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7dd69-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="7dd69-133">None</span></span>
- <span data-ttu-id="7dd69-134">Basisk</span><span class="sxs-lookup"><span data-stu-id="7dd69-134">Basic</span></span>
- <span data-ttu-id="7dd69-135">Standar</span><span class="sxs-lookup"><span data-stu-id="7dd69-135">Standard</span></span>
- <span data-ttu-id="7dd69-136">Beta</span><span class="sxs-lookup"><span data-stu-id="7dd69-136">Premium</span></span>
- <span data-ttu-id="7dd69-137">Warehouse</span><span class="sxs-lookup"><span data-stu-id="7dd69-137">DataWarehouse</span></span>
- <span data-ttu-id="7dd69-138">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="7dd69-138">Free</span></span>
- <span data-ttu-id="7dd69-139">Sträckning</span><span class="sxs-lookup"><span data-stu-id="7dd69-139">Stretch</span></span>
- <span data-ttu-id="7dd69-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="7dd69-140">GeneralPurpose</span></span>
- <span data-ttu-id="7dd69-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="7dd69-141">BusinessCritical</span></span>

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

### <span data-ttu-id="7dd69-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7dd69-142">-ElasticPoolName</span></span>
<span data-ttu-id="7dd69-143">Anger namnet på den elastiska pool som databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="7dd69-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="7dd69-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7dd69-144">-LicenseType</span></span>
<span data-ttu-id="7dd69-145">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="7dd69-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="7dd69-146">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="7dd69-146">Possible values are:</span></span>
- <span data-ttu-id="7dd69-147">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="7dd69-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="7dd69-148">Databas priset kommer att diskonteras för befintliga licens ägare för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7dd69-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="7dd69-149">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="7dd69-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="7dd69-150">Databas priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7dd69-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="7dd69-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="7dd69-151">-MaxSizeBytes</span></span>
<span data-ttu-id="7dd69-152">Anger den maximala storleken på databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="7dd69-152">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="7dd69-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="7dd69-153">-ReadScale</span></span>
<span data-ttu-id="7dd69-154">Alternativet Läs skalning för att tilldela en Azure SQL-databas. (Aktiverat/inaktiverat)</span><span class="sxs-lookup"><span data-stu-id="7dd69-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="7dd69-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="7dd69-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="7dd69-156">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="7dd69-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="7dd69-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dd69-157">-ResourceGroupName</span></span>
<span data-ttu-id="7dd69-158">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="7dd69-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7dd69-159">-SampleName</span><span class="sxs-lookup"><span data-stu-id="7dd69-159">-SampleName</span></span>
<span data-ttu-id="7dd69-160">Namnet på det exempel schema som ska användas när databasen skapas.</span><span class="sxs-lookup"><span data-stu-id="7dd69-160">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="7dd69-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7dd69-161">-ServerName</span></span>
<span data-ttu-id="7dd69-162">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="7dd69-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="7dd69-163">-Taggar</span><span class="sxs-lookup"><span data-stu-id="7dd69-163">-Tags</span></span>
<span data-ttu-id="7dd69-164">Anger en ord lista med par med nyckelord i form av en hash-tabell som denna cmdlet associerar med den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="7dd69-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="7dd69-165">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="7dd69-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7dd69-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="7dd69-166">-VCore</span></span>
<span data-ttu-id="7dd69-167">VCore-numret för Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="7dd69-167">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="7dd69-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7dd69-168">-ZoneRedundant</span></span>
<span data-ttu-id="7dd69-169">Zonens redundans som ska kopplas till Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="7dd69-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="7dd69-170">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7dd69-170">-Confirm</span></span>
<span data-ttu-id="7dd69-171">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7dd69-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dd69-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dd69-172">-WhatIf</span></span>
<span data-ttu-id="7dd69-173">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7dd69-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dd69-174">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7dd69-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dd69-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd69-175">CommonParameters</span></span>
<span data-ttu-id="7dd69-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd69-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd69-177">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dd69-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd69-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7dd69-178">INPUTS</span></span>

### <span data-ttu-id="7dd69-179">System. String</span><span class="sxs-lookup"><span data-stu-id="7dd69-179">System.String</span></span>

## <span data-ttu-id="7dd69-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7dd69-180">OUTPUTS</span></span>

### <span data-ttu-id="7dd69-181">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7dd69-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="7dd69-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7dd69-182">NOTES</span></span>

## <span data-ttu-id="7dd69-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7dd69-183">RELATED LINKS</span></span>

[<span data-ttu-id="7dd69-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7dd69-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="7dd69-185">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7dd69-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="7dd69-186">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="7dd69-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="7dd69-187">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7dd69-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="7dd69-188">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7dd69-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="7dd69-189">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7dd69-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="7dd69-190">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7dd69-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="7dd69-191">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="7dd69-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

