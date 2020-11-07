---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 3655204204dc35ea62473a1002a84d53ce0c327d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920589"
---
# <span data-ttu-id="3d554-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d554-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="3d554-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d554-102">SYNOPSIS</span></span>
<span data-ttu-id="3d554-103">Skapar en databas eller en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="3d554-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="3d554-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d554-104">SYNTAX</span></span>

### <span data-ttu-id="3d554-105">DtuBasedDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="3d554-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d554-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="3d554-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d554-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d554-107">DESCRIPTION</span></span>
<span data-ttu-id="3d554-108">Cmdleten **New-AzSqlDatabase** skapar en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3d554-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="3d554-109">Du kan också skapa en elastisk databas genom att ange parametern *ElasticPoolName* till en befintlig elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="3d554-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="3d554-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d554-110">EXAMPLES</span></span>

### <span data-ttu-id="3d554-111">Exempel 1: skapa en databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="3d554-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="3d554-112">Det här kommandot skapar en databas som heter Database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="3d554-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="3d554-113">Exempel 2: skapa en elastisk databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="3d554-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="3d554-114">Det här kommandot skapar en databas med namnet Database02 i den Elastic pool som heter ElasticPool01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="3d554-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="3d554-115">Exempel 3: skapa en vCore-databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="3d554-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="3d554-116">Det här kommandot skapar en vCore-databas som heter Database03 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="3d554-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="3d554-117">Exempel 4: skapa en Server databas på den angivna servern</span><span class="sxs-lookup"><span data-stu-id="3d554-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="3d554-118">Det här kommandot skapar en server lös databas med namnet Database04 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="3d554-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="3d554-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d554-119">PARAMETERS</span></span>

### <span data-ttu-id="3d554-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d554-120">-AsJob</span></span>
<span data-ttu-id="3d554-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3d554-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d554-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="3d554-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="3d554-123">Fördröjningen för automatisk paus i minuter för databasen (endast Server lös),-1 för att välja ut</span><span class="sxs-lookup"><span data-stu-id="3d554-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d554-124">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="3d554-124">-CatalogCollation</span></span>
<span data-ttu-id="3d554-125">Anger namnet på SQL-databasens katalog sortering.</span><span class="sxs-lookup"><span data-stu-id="3d554-125">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="3d554-126">-CollationName</span><span class="sxs-lookup"><span data-stu-id="3d554-126">-CollationName</span></span>
<span data-ttu-id="3d554-127">Anger namnet på sorteringen i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3d554-127">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="3d554-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3d554-128">-ComputeGeneration</span></span>
<span data-ttu-id="3d554-129">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="3d554-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="3d554-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="3d554-130">-ComputeModel</span></span>
<span data-ttu-id="3d554-131">Compute-modellen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3d554-131">The compute model for Azure Sql database.</span></span> <span data-ttu-id="3d554-132">Inte Server eller har etablerats</span><span class="sxs-lookup"><span data-stu-id="3d554-132">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d554-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d554-133">-DatabaseName</span></span>
<span data-ttu-id="3d554-134">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="3d554-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3d554-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d554-135">-DefaultProfile</span></span>
<span data-ttu-id="3d554-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3d554-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d554-137">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="3d554-137">-Edition</span></span>
<span data-ttu-id="3d554-138">Anger vilken utgåva som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="3d554-138">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="3d554-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3d554-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3d554-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d554-140">None</span></span>
- <span data-ttu-id="3d554-141">Basisk</span><span class="sxs-lookup"><span data-stu-id="3d554-141">Basic</span></span>
- <span data-ttu-id="3d554-142">Standar</span><span class="sxs-lookup"><span data-stu-id="3d554-142">Standard</span></span>
- <span data-ttu-id="3d554-143">Beta</span><span class="sxs-lookup"><span data-stu-id="3d554-143">Premium</span></span>
- <span data-ttu-id="3d554-144">Warehouse</span><span class="sxs-lookup"><span data-stu-id="3d554-144">DataWarehouse</span></span>
- <span data-ttu-id="3d554-145">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="3d554-145">Free</span></span>
- <span data-ttu-id="3d554-146">Sträckning</span><span class="sxs-lookup"><span data-stu-id="3d554-146">Stretch</span></span>
- <span data-ttu-id="3d554-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="3d554-147">GeneralPurpose</span></span>
- <span data-ttu-id="3d554-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="3d554-148">BusinessCritical</span></span>

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

### <span data-ttu-id="3d554-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3d554-149">-ElasticPoolName</span></span>
<span data-ttu-id="3d554-150">Anger namnet på den elastiska pool som databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="3d554-150">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="3d554-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3d554-151">-LicenseType</span></span>
<span data-ttu-id="3d554-152">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3d554-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="3d554-153">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="3d554-153">Possible values are:</span></span>
- <span data-ttu-id="3d554-154">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="3d554-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3d554-155">Databas priset kommer att diskonteras för befintliga licens ägare för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3d554-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3d554-156">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="3d554-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3d554-157">Databas priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3d554-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3d554-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="3d554-158">-MaxSizeBytes</span></span>
<span data-ttu-id="3d554-159">Anger den maximala storleken på databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="3d554-159">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="3d554-160">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="3d554-160">-MinimumCapacity</span></span>
<span data-ttu-id="3d554-161">Den minsta kapacitet som databasen alltid har tilldelats om den inte pausas.</span><span class="sxs-lookup"><span data-stu-id="3d554-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="3d554-162">Endast för serverbaserade Azure SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="3d554-162">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d554-163">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="3d554-163">-ReadScale</span></span>
<span data-ttu-id="3d554-164">Alternativet Läs skalning för att tilldela en Azure SQL-databas. (Aktiverat/inaktiverat)</span><span class="sxs-lookup"><span data-stu-id="3d554-164">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="3d554-165">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3d554-165">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="3d554-166">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="3d554-166">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="3d554-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d554-167">-ResourceGroupName</span></span>
<span data-ttu-id="3d554-168">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="3d554-168">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3d554-169">-SampleName</span><span class="sxs-lookup"><span data-stu-id="3d554-169">-SampleName</span></span>
<span data-ttu-id="3d554-170">Namnet på det exempel schema som ska användas när databasen skapas.</span><span class="sxs-lookup"><span data-stu-id="3d554-170">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="3d554-171">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d554-171">-ServerName</span></span>
<span data-ttu-id="3d554-172">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="3d554-172">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3d554-173">-Taggar</span><span class="sxs-lookup"><span data-stu-id="3d554-173">-Tags</span></span>
<span data-ttu-id="3d554-174">Anger en ord lista med par med nyckelord i form av en hash-tabell som denna cmdlet associerar med den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="3d554-174">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="3d554-175">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3d554-175">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3d554-176">-VCore</span><span class="sxs-lookup"><span data-stu-id="3d554-176">-VCore</span></span>
<span data-ttu-id="3d554-177">VCore-numret för Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="3d554-177">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d554-178">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="3d554-178">-ZoneRedundant</span></span>
<span data-ttu-id="3d554-179">Zonens redundans som ska kopplas till Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="3d554-179">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="3d554-180">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d554-180">-Confirm</span></span>
<span data-ttu-id="3d554-181">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d554-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d554-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d554-182">-WhatIf</span></span>
<span data-ttu-id="3d554-183">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d554-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d554-184">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d554-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d554-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d554-185">CommonParameters</span></span>
<span data-ttu-id="3d554-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d554-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d554-187">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d554-187">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d554-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d554-188">INPUTS</span></span>

### <span data-ttu-id="3d554-189">System. String</span><span class="sxs-lookup"><span data-stu-id="3d554-189">System.String</span></span>

## <span data-ttu-id="3d554-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d554-190">OUTPUTS</span></span>

### <span data-ttu-id="3d554-191">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3d554-191">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="3d554-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d554-192">NOTES</span></span>

## <span data-ttu-id="3d554-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d554-193">RELATED LINKS</span></span>

[<span data-ttu-id="3d554-194">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d554-194">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="3d554-195">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d554-195">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="3d554-196">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="3d554-196">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="3d554-197">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d554-197">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="3d554-198">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d554-198">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="3d554-199">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d554-199">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="3d554-200">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d554-200">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="3d554-201">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="3d554-201">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

