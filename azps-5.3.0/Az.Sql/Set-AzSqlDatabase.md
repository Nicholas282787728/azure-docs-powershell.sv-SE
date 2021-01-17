---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 6d737abb6c58ea8c74085f8390d7a6acbdf54dc8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420179"
---
# <span data-ttu-id="9d321-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9d321-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="9d321-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d321-102">SYNOPSIS</span></span>
<span data-ttu-id="9d321-103">Anger egenskaper för en databas eller flyttar en befintlig databas till en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="9d321-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="9d321-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d321-104">SYNTAX</span></span>

### <span data-ttu-id="9d321-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="9d321-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d321-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="9d321-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d321-107">Byta namn på</span><span class="sxs-lookup"><span data-stu-id="9d321-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d321-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d321-108">DESCRIPTION</span></span>
<span data-ttu-id="9d321-109">Cmdleten **set-AzSqlDatabase** anger egenskaper för en databas i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="9d321-110">Denna cmdlet kan ändra tjänst nivån (*utgåvan*), Performance Level (*RequestedServiceObjectiveName*) och *MaxSizeBytes*(Storage maximum size) för databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="9d321-111">Dessutom kan du ange parametern *ElasticPoolName* om du vill flytta en databas till en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="9d321-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="9d321-112">Om en databas redan finns i en elastisk pool kan du använda parametern *RequestedServiceObjectiveName* för att flytta databasen från en elastisk pool och till en prestanda nivå för enskilda databaser.</span><span class="sxs-lookup"><span data-stu-id="9d321-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="9d321-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d321-113">EXAMPLES</span></span>

### <span data-ttu-id="9d321-114">Exempel 1: uppdatera en databas till en vanlig S0-databas</span><span class="sxs-lookup"><span data-stu-id="9d321-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="9d321-115">Det här kommandot uppdaterar en databas som heter Database01 till en vanlig S0-databas på en server med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="9d321-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="9d321-116">Exempel 2: lägga till en databas i en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="9d321-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="9d321-117">Det här kommandot lägger till en databas med namnet Database01 i den Elastic pool som heter ElasticPool01 som finns på servern med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="9d321-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="9d321-118">Exempel 3: ändra Max storleken på en databas</span><span class="sxs-lookup"><span data-stu-id="9d321-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="9d321-119">Det här kommandot uppdaterar en databas med namnet Database01 för att ange max storleken till 1 TB.</span><span class="sxs-lookup"><span data-stu-id="9d321-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="9d321-120">Exempel 4: uppdatera en befintlig allmän syftes databas till storskalig tjänst nivå</span><span class="sxs-lookup"><span data-stu-id="9d321-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Hyperscale" -RequestedServiceObjectiveName "HS_Gen5_2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : 56246136-839f-4171-80af-4c28142463b1
Edition                       : Hyperscale
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : -1
Status                        : Online
CreationDate                  : 12/6/2020 5:34:16 PM
CurrentServiceObjectiveId     : 00000000-0000-0000-0000-000000000000
CurrentServiceObjectiveName   : HS_Gen5_2
RequestedServiceObjectiveName : HS_Gen5_2
RequestedServiceObjectiveId   :
ElasticPoolName               :
EarliestRestoreDate           : 12/6/2020 5:34:16 PM
Tags                          : {}
ResourceId                    : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/Server01/databases/Database01
CreateMode                    :
ReadScale                     : Enabled
ZoneRedundant                 :
Capacity                      : 2
Family                        : Gen5
SkuName                       : HS_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       :
MinimumCapacity               :
ReadReplicaCount              : 1
BackupStorageRedundancy       : Geo
```

<span data-ttu-id="9d321-121">Det här kommandot uppdaterar en databas som heter Database01 från allmänt syfte till storskalig tjänst nivå.</span><span class="sxs-lookup"><span data-stu-id="9d321-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="9d321-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d321-122">PARAMETERS</span></span>

### <span data-ttu-id="9d321-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d321-123">-AsJob</span></span>
<span data-ttu-id="9d321-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9d321-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d321-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="9d321-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="9d321-126">Fördröjningen för automatisk paus i minuter för databasen (endast Server lös),-1 för att välja ut</span><span class="sxs-lookup"><span data-stu-id="9d321-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="9d321-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="9d321-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="9d321-128">Säkerhets kopians lagrings utrymme som används för att lagra säkerhets kopior för SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="9d321-129">Alternativen är: lokal, zon och geo.</span><span class="sxs-lookup"><span data-stu-id="9d321-129">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d321-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="9d321-130">-ComputeGeneration</span></span>
<span data-ttu-id="9d321-131">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="9d321-131">The compute generation to assign.</span></span>

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

### <span data-ttu-id="9d321-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="9d321-132">-ComputeModel</span></span>
<span data-ttu-id="9d321-133">Beräknad modell av Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="9d321-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="9d321-134">Inte Server eller har etablerats</span><span class="sxs-lookup"><span data-stu-id="9d321-134">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="9d321-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9d321-135">-DatabaseName</span></span>
<span data-ttu-id="9d321-136">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="9d321-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d321-137">-DefaultProfile</span></span>
<span data-ttu-id="9d321-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9d321-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d321-139">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="9d321-139">-Edition</span></span>
<span data-ttu-id="9d321-140">Anger versionen för databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="9d321-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9d321-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d321-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="9d321-142">None</span></span>
- <span data-ttu-id="9d321-143">Basisk</span><span class="sxs-lookup"><span data-stu-id="9d321-143">Basic</span></span>
- <span data-ttu-id="9d321-144">Standar</span><span class="sxs-lookup"><span data-stu-id="9d321-144">Standard</span></span>
- <span data-ttu-id="9d321-145">Beta</span><span class="sxs-lookup"><span data-stu-id="9d321-145">Premium</span></span>
- <span data-ttu-id="9d321-146">Warehouse</span><span class="sxs-lookup"><span data-stu-id="9d321-146">DataWarehouse</span></span>
- <span data-ttu-id="9d321-147">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="9d321-147">Free</span></span>
- <span data-ttu-id="9d321-148">Sträckning</span><span class="sxs-lookup"><span data-stu-id="9d321-148">Stretch</span></span>
- <span data-ttu-id="9d321-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="9d321-149">GeneralPurpose</span></span>
- <span data-ttu-id="9d321-150">Gråskala</span><span class="sxs-lookup"><span data-stu-id="9d321-150">Hyperscale</span></span>
- <span data-ttu-id="9d321-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="9d321-151">BusinessCritical</span></span>

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

### <span data-ttu-id="9d321-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9d321-152">-ElasticPoolName</span></span>
<span data-ttu-id="9d321-153">Anger namnet på den Elastic pool som databasen ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="9d321-153">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="9d321-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="9d321-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="9d321-155">Antalet skrivskyddade sekundära repliker som är associerade med databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="9d321-156">Endast för högskalan.</span><span class="sxs-lookup"><span data-stu-id="9d321-156">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d321-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9d321-157">-LicenseType</span></span>
<span data-ttu-id="9d321-158">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="9d321-159">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="9d321-159">Possible values are:</span></span>
- <span data-ttu-id="9d321-160">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="9d321-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="9d321-161">Databas priset kommer att diskonteras för befintliga licens ägare för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9d321-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="9d321-162">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="9d321-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="9d321-163">Databas priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9d321-163">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="9d321-164">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="9d321-164">-MaxSizeBytes</span></span>
<span data-ttu-id="9d321-165">Maximal storlek för Azure SQL-databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="9d321-165">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="9d321-166">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="9d321-166">-MinimumCapacity</span></span>
<span data-ttu-id="9d321-167">Den minsta kapacitet som databasen alltid har tilldelats om den inte pausas.</span><span class="sxs-lookup"><span data-stu-id="9d321-167">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="9d321-168">Endast för serverbaserade Azure SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="9d321-168">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="9d321-169">-NewName</span><span class="sxs-lookup"><span data-stu-id="9d321-169">-NewName</span></span>
<span data-ttu-id="9d321-170">Det nya namnet för att byta namn på databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-170">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="9d321-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="9d321-171">-ReadScale</span></span>
<span data-ttu-id="9d321-172">Om den är aktive rad kan de anslutningar som har ställts in för att vara skrivskyddade i deras anslutnings sträng dirigeras till en skrivskyddad sekundär replik.</span><span class="sxs-lookup"><span data-stu-id="9d321-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="9d321-173">Den här egenskapen kan bara anges för Premium-och Business Critical-databaser.</span><span class="sxs-lookup"><span data-stu-id="9d321-173">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="9d321-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9d321-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="9d321-175">Anger namnet på det tjänst mål som ska kopplas till databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-175">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="9d321-176">Information om tjänst mål finns i [Azure SQL Database Service tieres and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) i Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="9d321-176">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="9d321-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d321-177">-ResourceGroupName</span></span>
<span data-ttu-id="9d321-178">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="9d321-178">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9d321-179">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="9d321-179">-SecondaryType</span></span>
<span data-ttu-id="9d321-180">Den sekundära typen för databasen om den är en sekundär.</span><span class="sxs-lookup"><span data-stu-id="9d321-180">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="9d321-181">Giltiga värden är geo och named.</span><span class="sxs-lookup"><span data-stu-id="9d321-181">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d321-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9d321-182">-ServerName</span></span>
<span data-ttu-id="9d321-183">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="9d321-183">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="9d321-184">-Taggar</span><span class="sxs-lookup"><span data-stu-id="9d321-184">-Tags</span></span>
<span data-ttu-id="9d321-185">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9d321-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9d321-186">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="9d321-186">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9d321-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="9d321-187">-VCore</span></span>
<span data-ttu-id="9d321-188">VCore-numret för Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="9d321-188">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="9d321-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="9d321-189">-ZoneRedundant</span></span>
<span data-ttu-id="9d321-190">Zonens redundans som ska kopplas till Azure SQL-databasen</span><span class="sxs-lookup"><span data-stu-id="9d321-190">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="9d321-191">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9d321-191">-Confirm</span></span>
<span data-ttu-id="9d321-192">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9d321-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d321-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d321-193">-WhatIf</span></span>
<span data-ttu-id="9d321-194">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9d321-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d321-195">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9d321-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d321-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d321-196">CommonParameters</span></span>
<span data-ttu-id="9d321-197">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d321-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d321-198">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d321-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d321-199">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d321-199">INPUTS</span></span>

### <span data-ttu-id="9d321-200">System. String</span><span class="sxs-lookup"><span data-stu-id="9d321-200">System.String</span></span>

## <span data-ttu-id="9d321-201">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d321-201">OUTPUTS</span></span>

### <span data-ttu-id="9d321-202">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9d321-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9d321-203">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d321-203">NOTES</span></span>

## <span data-ttu-id="9d321-204">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d321-204">RELATED LINKS</span></span>

[<span data-ttu-id="9d321-205">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9d321-205">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="9d321-206">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9d321-206">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="9d321-207">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9d321-207">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="9d321-208">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9d321-208">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="9d321-209">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9d321-209">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="9d321-210">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9d321-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
