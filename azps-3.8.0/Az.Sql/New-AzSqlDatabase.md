---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 32329ac1e36c74c08dcf25f8f8b4295e81633e90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088478"
---
# <span data-ttu-id="aa52b-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aa52b-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="aa52b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa52b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa52b-103">Skapar en databas eller en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="aa52b-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="aa52b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa52b-104">SYNTAX</span></span>

### <span data-ttu-id="aa52b-105">DtuBasedDatabase (standard)</span><span class="sxs-lookup"><span data-stu-id="aa52b-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa52b-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="aa52b-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa52b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa52b-107">DESCRIPTION</span></span>
<span data-ttu-id="aa52b-108">Cmdleten **New-AzSqlDatabase** skapar en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="aa52b-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="aa52b-109">Du kan också skapa en elastisk databas genom att ange parametern *ElasticPoolName* till en befintlig elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="aa52b-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="aa52b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa52b-110">EXAMPLES</span></span>

### <span data-ttu-id="aa52b-111">Exempel 1: skapa en databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="aa52b-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="aa52b-112">Det här kommandot skapar en databas som heter Database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="aa52b-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="aa52b-113">Exempel 2: skapa en elastisk databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="aa52b-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="aa52b-114">Det här kommandot skapar en databas med namnet Database02 i den Elastic pool som heter ElasticPool01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="aa52b-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="aa52b-115">Exempel 3: skapa en vCore-databas på en angiven server</span><span class="sxs-lookup"><span data-stu-id="aa52b-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="aa52b-116">Det här kommandot skapar en vCore-databas som heter Database03 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="aa52b-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="aa52b-117">Exempel 4: skapa en Server databas på den angivna servern</span><span class="sxs-lookup"><span data-stu-id="aa52b-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="aa52b-118">Det här kommandot skapar en server lös databas med namnet Database04 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="aa52b-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="aa52b-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa52b-119">PARAMETERS</span></span>

### <span data-ttu-id="aa52b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa52b-120">-AsJob</span></span>
<span data-ttu-id="aa52b-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="aa52b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa52b-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="aa52b-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="aa52b-123">Fördröjningen för automatisk paus i minuter för databasen (endast Server lös),-1 för att välja ut</span><span class="sxs-lookup"><span data-stu-id="aa52b-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="aa52b-124">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="aa52b-124">-CatalogCollation</span></span>
<span data-ttu-id="aa52b-125">Anger namnet på SQL-databasens katalog sortering.</span><span class="sxs-lookup"><span data-stu-id="aa52b-125">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="aa52b-126">-CollationName</span><span class="sxs-lookup"><span data-stu-id="aa52b-126">-CollationName</span></span>
<span data-ttu-id="aa52b-127">Anger namnet på sorteringen i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="aa52b-127">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="aa52b-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="aa52b-128">-ComputeGeneration</span></span>
<span data-ttu-id="aa52b-129">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="aa52b-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="aa52b-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="aa52b-130">-ComputeModel</span></span>
<span data-ttu-id="aa52b-131">Compute-modellen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="aa52b-131">The compute model for Azure Sql database.</span></span> <span data-ttu-id="aa52b-132">Inte Server eller har etablerats</span><span class="sxs-lookup"><span data-stu-id="aa52b-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="aa52b-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa52b-133">-DatabaseName</span></span>
<span data-ttu-id="aa52b-134">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="aa52b-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="aa52b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa52b-135">-DefaultProfile</span></span>
<span data-ttu-id="aa52b-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aa52b-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa52b-137">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="aa52b-137">-Edition</span></span>
<span data-ttu-id="aa52b-138">Anger vilken utgåva som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="aa52b-138">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="aa52b-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aa52b-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa52b-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="aa52b-140">None</span></span>
- <span data-ttu-id="aa52b-141">Basisk</span><span class="sxs-lookup"><span data-stu-id="aa52b-141">Basic</span></span>
- <span data-ttu-id="aa52b-142">Standar</span><span class="sxs-lookup"><span data-stu-id="aa52b-142">Standard</span></span>
- <span data-ttu-id="aa52b-143">Beta</span><span class="sxs-lookup"><span data-stu-id="aa52b-143">Premium</span></span>
- <span data-ttu-id="aa52b-144">Warehouse</span><span class="sxs-lookup"><span data-stu-id="aa52b-144">DataWarehouse</span></span>
- <span data-ttu-id="aa52b-145">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="aa52b-145">Free</span></span>
- <span data-ttu-id="aa52b-146">Sträckning</span><span class="sxs-lookup"><span data-stu-id="aa52b-146">Stretch</span></span>
- <span data-ttu-id="aa52b-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="aa52b-147">GeneralPurpose</span></span>
- <span data-ttu-id="aa52b-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="aa52b-148">BusinessCritical</span></span>

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

### <span data-ttu-id="aa52b-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="aa52b-149">-ElasticPoolName</span></span>
<span data-ttu-id="aa52b-150">Anger namnet på den elastiska pool som databasen ska placeras i.</span><span class="sxs-lookup"><span data-stu-id="aa52b-150">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="aa52b-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="aa52b-151">-LicenseType</span></span>
<span data-ttu-id="aa52b-152">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="aa52b-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="aa52b-153">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="aa52b-153">Possible values are:</span></span>
- <span data-ttu-id="aa52b-154">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="aa52b-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="aa52b-155">Databas priset kommer att diskonteras för befintliga licens ägare för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="aa52b-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="aa52b-156">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="aa52b-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="aa52b-157">Databas priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="aa52b-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="aa52b-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="aa52b-158">-MaxSizeBytes</span></span>
<span data-ttu-id="aa52b-159">Anger den maximala storleken på databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="aa52b-159">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="aa52b-160">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="aa52b-160">-MinimumCapacity</span></span>
<span data-ttu-id="aa52b-161">Den minsta kapacitet som databasen alltid har tilldelats om den inte pausas.</span><span class="sxs-lookup"><span data-stu-id="aa52b-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="aa52b-162">Endast för serverbaserade Azure SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="aa52b-162">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="aa52b-163">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="aa52b-163">-ReadReplicaCount</span></span>
<span data-ttu-id="aa52b-164">Antalet skrivskyddade sekundära repliker som är associerade med databasen och som är skrivskyddade med den.</span><span class="sxs-lookup"><span data-stu-id="aa52b-164">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="aa52b-165">Den här egenskapen kan bara anges för databaser med storskalig version.</span><span class="sxs-lookup"><span data-stu-id="aa52b-165">This property is only settable for Hyperscale edition databases.</span></span>

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

### <span data-ttu-id="aa52b-166">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="aa52b-166">-ReadScale</span></span>
<span data-ttu-id="aa52b-167">Om den är aktive rad kan de anslutningar som har ställts in för att vara skrivskyddade i deras anslutnings sträng dirigeras till en skrivskyddad sekundär replik.</span><span class="sxs-lookup"><span data-stu-id="aa52b-167">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="aa52b-168">Den här egenskapen kan bara anges för Premium-och Business Critical-databaser.</span><span class="sxs-lookup"><span data-stu-id="aa52b-168">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="aa52b-169">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="aa52b-169">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="aa52b-170">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="aa52b-170">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="aa52b-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa52b-171">-ResourceGroupName</span></span>
<span data-ttu-id="aa52b-172">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="aa52b-172">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="aa52b-173">-SampleName</span><span class="sxs-lookup"><span data-stu-id="aa52b-173">-SampleName</span></span>
<span data-ttu-id="aa52b-174">Namnet på det exempel schema som ska användas när databasen skapas.</span><span class="sxs-lookup"><span data-stu-id="aa52b-174">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="aa52b-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aa52b-175">-ServerName</span></span>
<span data-ttu-id="aa52b-176">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="aa52b-176">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="aa52b-177">-Taggar</span><span class="sxs-lookup"><span data-stu-id="aa52b-177">-Tags</span></span>
<span data-ttu-id="aa52b-178">Anger en ord lista med par med nyckelord i form av en hash-tabell som denna cmdlet associerar med den nya databasen.</span><span class="sxs-lookup"><span data-stu-id="aa52b-178">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="aa52b-179">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="aa52b-179">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aa52b-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="aa52b-180">-VCore</span></span>
<span data-ttu-id="aa52b-181">VCore-numret för Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="aa52b-181">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="aa52b-182">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="aa52b-182">-ZoneRedundant</span></span>
<span data-ttu-id="aa52b-183">Zonens redundans som ska kopplas till Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="aa52b-183">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="aa52b-184">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aa52b-184">-Confirm</span></span>
<span data-ttu-id="aa52b-185">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aa52b-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa52b-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa52b-186">-WhatIf</span></span>
<span data-ttu-id="aa52b-187">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aa52b-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa52b-188">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aa52b-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa52b-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa52b-189">CommonParameters</span></span>
<span data-ttu-id="aa52b-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa52b-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa52b-191">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa52b-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa52b-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa52b-192">INPUTS</span></span>

### <span data-ttu-id="aa52b-193">System. String</span><span class="sxs-lookup"><span data-stu-id="aa52b-193">System.String</span></span>

## <span data-ttu-id="aa52b-194">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa52b-194">OUTPUTS</span></span>

### <span data-ttu-id="aa52b-195">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="aa52b-195">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="aa52b-196">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa52b-196">NOTES</span></span>

## <span data-ttu-id="aa52b-197">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa52b-197">RELATED LINKS</span></span>

[<span data-ttu-id="aa52b-198">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aa52b-198">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="aa52b-199">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="aa52b-199">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="aa52b-200">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="aa52b-200">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="aa52b-201">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aa52b-201">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="aa52b-202">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aa52b-202">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="aa52b-203">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aa52b-203">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="aa52b-204">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aa52b-204">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="aa52b-205">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="aa52b-205">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

