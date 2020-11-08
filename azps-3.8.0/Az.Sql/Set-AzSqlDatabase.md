---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 180cd3c8d9301ab287bc4a37c13f7b07276f7794
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088597"
---
# <span data-ttu-id="0496c-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0496c-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="0496c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0496c-102">SYNOPSIS</span></span>
<span data-ttu-id="0496c-103">Anger egenskaper för en databas eller flyttar en befintlig databas till en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="0496c-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="0496c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0496c-104">SYNTAX</span></span>

### <span data-ttu-id="0496c-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="0496c-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0496c-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="0496c-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0496c-107">Byta namn på</span><span class="sxs-lookup"><span data-stu-id="0496c-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0496c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0496c-108">DESCRIPTION</span></span>
<span data-ttu-id="0496c-109">Cmdleten **set-AzSqlDatabase** anger egenskaper för en databas i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="0496c-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="0496c-110">Denna cmdlet kan ändra tjänst nivån ( *utgåvan* ), Performance Level ( *RequestedServiceObjectiveName* ) och *MaxSizeBytes* (Storage maximum size) för databasen.</span><span class="sxs-lookup"><span data-stu-id="0496c-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="0496c-111">Dessutom kan du ange parametern *ElasticPoolName* om du vill flytta en databas till en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="0496c-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="0496c-112">Om en databas redan finns i en elastisk pool kan du använda parametern *RequestedServiceObjectiveName* för att flytta databasen från en elastisk pool och till en prestanda nivå för enskilda databaser.</span><span class="sxs-lookup"><span data-stu-id="0496c-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="0496c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0496c-113">EXAMPLES</span></span>

### <span data-ttu-id="0496c-114">Exempel 1: uppdatera en databas till en vanlig S0-databas</span><span class="sxs-lookup"><span data-stu-id="0496c-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
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
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="0496c-115">Det här kommandot uppdaterar en databas som heter Database01 till en vanlig S0-databas på en server med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="0496c-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="0496c-116">Exempel 2: lägga till en databas i en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="0496c-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="0496c-117">Det här kommandot lägger till en databas med namnet Database01 i den Elastic pool som heter ElasticPool01 som finns på servern med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="0496c-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="0496c-118">Exempel 3: ändra Max storleken på en databas</span><span class="sxs-lookup"><span data-stu-id="0496c-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="0496c-119">Det här kommandot uppdaterar en databas med namnet Database01 för att ange max storleken till 1 TB.</span><span class="sxs-lookup"><span data-stu-id="0496c-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="0496c-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0496c-120">PARAMETERS</span></span>

### <span data-ttu-id="0496c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0496c-121">-AsJob</span></span>
<span data-ttu-id="0496c-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0496c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0496c-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="0496c-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="0496c-124">Fördröjningen för automatisk paus i minuter för databasen (endast Server lös),-1 för att välja ut</span><span class="sxs-lookup"><span data-stu-id="0496c-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-125">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0496c-125">-ComputeGeneration</span></span>
<span data-ttu-id="0496c-126">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="0496c-126">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-127">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="0496c-127">-ComputeModel</span></span>
<span data-ttu-id="0496c-128">Beräknad modell av Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="0496c-128">Computed model of Azure Sql database.</span></span> <span data-ttu-id="0496c-129">Inte Server eller har etablerats</span><span class="sxs-lookup"><span data-stu-id="0496c-129">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0496c-130">-DatabaseName</span></span>
<span data-ttu-id="0496c-131">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="0496c-131">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0496c-132">-DefaultProfile</span></span>
<span data-ttu-id="0496c-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0496c-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0496c-134">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="0496c-134">-Edition</span></span>
<span data-ttu-id="0496c-135">Anger versionen för databasen.</span><span class="sxs-lookup"><span data-stu-id="0496c-135">Specifies the edition for the database.</span></span>
<span data-ttu-id="0496c-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0496c-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0496c-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="0496c-137">None</span></span>
- <span data-ttu-id="0496c-138">Basisk</span><span class="sxs-lookup"><span data-stu-id="0496c-138">Basic</span></span>
- <span data-ttu-id="0496c-139">Standar</span><span class="sxs-lookup"><span data-stu-id="0496c-139">Standard</span></span>
- <span data-ttu-id="0496c-140">Beta</span><span class="sxs-lookup"><span data-stu-id="0496c-140">Premium</span></span>
- <span data-ttu-id="0496c-141">Warehouse</span><span class="sxs-lookup"><span data-stu-id="0496c-141">DataWarehouse</span></span>
- <span data-ttu-id="0496c-142">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="0496c-142">Free</span></span>
- <span data-ttu-id="0496c-143">Sträckning</span><span class="sxs-lookup"><span data-stu-id="0496c-143">Stretch</span></span>
- <span data-ttu-id="0496c-144">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0496c-144">GeneralPurpose</span></span>
- <span data-ttu-id="0496c-145">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0496c-145">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-146">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0496c-146">-ElasticPoolName</span></span>
<span data-ttu-id="0496c-147">Anger namnet på den Elastic pool som databasen ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="0496c-147">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0496c-148">-LicenseType</span></span>
<span data-ttu-id="0496c-149">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="0496c-149">The license type for the Azure Sql database.</span></span> <span data-ttu-id="0496c-150">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="0496c-150">Possible values are:</span></span>
- <span data-ttu-id="0496c-151">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="0496c-151">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="0496c-152">Databas priset kommer att diskonteras för befintliga licens ägare för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0496c-152">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="0496c-153">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="0496c-153">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="0496c-154">Databas priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0496c-154">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-155">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="0496c-155">-MaxSizeBytes</span></span>
<span data-ttu-id="0496c-156">Maximal storlek för Azure SQL-databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="0496c-156">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-157">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="0496c-157">-MinimumCapacity</span></span>
<span data-ttu-id="0496c-158">Den minsta kapacitet som databasen alltid har tilldelats om den inte pausas.</span><span class="sxs-lookup"><span data-stu-id="0496c-158">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="0496c-159">Endast för serverbaserade Azure SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="0496c-159">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-160">-NewName</span><span class="sxs-lookup"><span data-stu-id="0496c-160">-NewName</span></span>
<span data-ttu-id="0496c-161">Det nya namnet för att byta namn på databasen.</span><span class="sxs-lookup"><span data-stu-id="0496c-161">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-162">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="0496c-162">-ReadReplicaCount</span></span>
<span data-ttu-id="0496c-163">Antalet skrivskyddade sekundära repliker som är associerade med databasen.</span><span class="sxs-lookup"><span data-stu-id="0496c-163">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="0496c-164">Endast för högskalan.</span><span class="sxs-lookup"><span data-stu-id="0496c-164">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-165">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="0496c-165">-ReadScale</span></span>
<span data-ttu-id="0496c-166">Om den är aktive rad kan de anslutningar som har ställts in för att vara skrivskyddade i deras anslutnings sträng dirigeras till en skrivskyddad sekundär replik.</span><span class="sxs-lookup"><span data-stu-id="0496c-166">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="0496c-167">Den här egenskapen kan bara anges för Premium-och Business Critical-databaser.</span><span class="sxs-lookup"><span data-stu-id="0496c-167">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-168">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="0496c-168">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="0496c-169">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="0496c-169">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="0496c-170">Information om tjänst mål finns i [Azure SQL Database Service tieres and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="0496c-170">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0496c-171">-ResourceGroupName</span></span>
<span data-ttu-id="0496c-172">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="0496c-172">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0496c-173">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0496c-173">-ServerName</span></span>
<span data-ttu-id="0496c-174">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="0496c-174">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0496c-175">-Taggar</span><span class="sxs-lookup"><span data-stu-id="0496c-175">-Tags</span></span>
<span data-ttu-id="0496c-176">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0496c-176">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0496c-177">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="0496c-177">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-178">-VCore</span><span class="sxs-lookup"><span data-stu-id="0496c-178">-VCore</span></span>
<span data-ttu-id="0496c-179">VCore-numret för Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="0496c-179">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-180">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0496c-180">-ZoneRedundant</span></span>
<span data-ttu-id="0496c-181">Zonens redundans som ska kopplas till Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="0496c-181">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0496c-182">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0496c-182">-Confirm</span></span>
<span data-ttu-id="0496c-183">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0496c-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0496c-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0496c-184">-WhatIf</span></span>
<span data-ttu-id="0496c-185">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0496c-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0496c-186">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0496c-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0496c-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0496c-187">CommonParameters</span></span>
<span data-ttu-id="0496c-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0496c-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0496c-189">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0496c-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0496c-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0496c-190">INPUTS</span></span>

### <span data-ttu-id="0496c-191">System. String</span><span class="sxs-lookup"><span data-stu-id="0496c-191">System.String</span></span>

## <span data-ttu-id="0496c-192">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0496c-192">OUTPUTS</span></span>

### <span data-ttu-id="0496c-193">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0496c-193">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0496c-194">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0496c-194">NOTES</span></span>

## <span data-ttu-id="0496c-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0496c-195">RELATED LINKS</span></span>

[<span data-ttu-id="0496c-196">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0496c-196">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0496c-197">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0496c-197">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="0496c-198">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0496c-198">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="0496c-199">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0496c-199">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="0496c-200">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0496c-200">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="0496c-201">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="0496c-201">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
