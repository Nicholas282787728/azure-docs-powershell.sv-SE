---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: f16313710e0ab007f23df0cfa3a2214f78a8963a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920304"
---
# <span data-ttu-id="4d9f0-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4d9f0-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="4d9f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d9f0-102">SYNOPSIS</span></span>
<span data-ttu-id="4d9f0-103">Skapar en elastisk databas för en SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="4d9f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d9f0-104">SYNTAX</span></span>

### <span data-ttu-id="4d9f0-105">DtuBasedPool (standard)</span><span class="sxs-lookup"><span data-stu-id="4d9f0-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d9f0-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="4d9f0-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d9f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d9f0-107">DESCRIPTION</span></span>
<span data-ttu-id="4d9f0-108">Cmdleten **New-AzSqlElasticPool** skapar en elastisk databas för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="4d9f0-109">Flera parametrar ( *-DTU,-DatabaseDtuMin och-DatabaseDtuMax* ) kräver att det värde som anges är från listan över giltiga värden för den parametern.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="4d9f0-110">Till exempel kan-DatabaseDtuMax för en standard-100 eDTU-pool bara vara 10, 20, 50 eller 100.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="4d9f0-111">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="4d9f0-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="4d9f0-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d9f0-112">EXAMPLES</span></span>

### <span data-ttu-id="4d9f0-113">Exempel 1: skapa en elastisk pool för DTU</span><span class="sxs-lookup"><span data-stu-id="4d9f0-113">Example 1: Create a DTU elastic pool</span></span>

```
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4d9f0-114">Det här kommandot skapar en elastisk pool i standard tjänst nivån som heter ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="4d9f0-115">Servern med namnet Server01, tilldelad till en Azure-adressresurs med namnet ResourceGroup01, är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="4d9f0-116">Kommandot anger värden för egenskapen DTU för poolen och databaserna i poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="4d9f0-117">Exempel 2: skapa en vCore elastisk pool</span><span class="sxs-lookup"><span data-stu-id="4d9f0-117">Example 2: Create a vCore elastic pool</span></span>

```
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                : 
```


<span data-ttu-id="4d9f0-118">Det här kommandot skapar en elastisk pool i GengeralPurpose tjänst nivå med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="4d9f0-119">Servern med namnet Server01, tilldelad till en Azure-adressresurs med namnet ResourceGroup01, är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="4d9f0-120">Kommandot anger vCore egenskaps värden för poolen och databaserna i poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="4d9f0-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d9f0-121">PARAMETERS</span></span>

### <span data-ttu-id="4d9f0-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d9f0-122">-AsJob</span></span>
<span data-ttu-id="4d9f0-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4d9f0-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d9f0-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4d9f0-124">-ComputeGeneration</span></span>
<span data-ttu-id="4d9f0-125">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-125">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9f0-126">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="4d9f0-126">-DatabaseDtuMax</span></span>
<span data-ttu-id="4d9f0-127">Anger det maximala antalet databas data flödes enheter (DTUs) som en enskild databas i poolen kan förbruka.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-127">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="4d9f0-128">Standardvärdena för de olika versionerna är följande:</span><span class="sxs-lookup"><span data-stu-id="4d9f0-128">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="4d9f0-129">Basisk.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-129">Basic.</span></span> <span data-ttu-id="4d9f0-130">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="4d9f0-130">5 DTUs</span></span>
- <span data-ttu-id="4d9f0-131">Standar.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-131">Standard.</span></span> <span data-ttu-id="4d9f0-132">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="4d9f0-132">100 DTUs</span></span>
- <span data-ttu-id="4d9f0-133">Beta.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-133">Premium.</span></span> <span data-ttu-id="4d9f0-134">125 DTUs mer information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="4d9f0-134">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9f0-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="4d9f0-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="4d9f0-136">Anger det minsta antal DTUs som den elastiska poolen garanterar till alla databaser i poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="4d9f0-137">Standardvärdet är noll (0).</span><span class="sxs-lookup"><span data-stu-id="4d9f0-137">The default value is zero (0).</span></span>
<span data-ttu-id="4d9f0-138">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="4d9f0-138">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9f0-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="4d9f0-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="4d9f0-140">Det högsta VCore-numret som en SqlAzure-databas kan använda i poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9f0-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="4d9f0-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="4d9f0-142">Det minsta VCore numret som valfri SqlAzure-databas kan använda i poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9f0-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d9f0-143">-DefaultProfile</span></span>
<span data-ttu-id="4d9f0-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4d9f0-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d9f0-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="4d9f0-145">-Dtu</span></span>
<span data-ttu-id="4d9f0-146">Anger det totala antalet delade DTUs för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="4d9f0-147">Standardvärdena för de olika versionerna är följande:</span><span class="sxs-lookup"><span data-stu-id="4d9f0-147">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="4d9f0-148">Basisk.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-148">Basic.</span></span>
<span data-ttu-id="4d9f0-149">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="4d9f0-149">100 DTUs</span></span>
- <span data-ttu-id="4d9f0-150">Standar.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-150">Standard.</span></span>
<span data-ttu-id="4d9f0-151">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="4d9f0-151">100 DTUs</span></span>
- <span data-ttu-id="4d9f0-152">Beta.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-152">Premium.</span></span>
<span data-ttu-id="4d9f0-153">125 DTUs mer information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="4d9f0-153">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9f0-154">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="4d9f0-154">-Edition</span></span>
<span data-ttu-id="4d9f0-155">Anger den version av Azure SQL-databasen som används för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-155">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="4d9f0-156">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4d9f0-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d9f0-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="4d9f0-157">None</span></span>
- <span data-ttu-id="4d9f0-158">Basisk</span><span class="sxs-lookup"><span data-stu-id="4d9f0-158">Basic</span></span>
- <span data-ttu-id="4d9f0-159">Standar</span><span class="sxs-lookup"><span data-stu-id="4d9f0-159">Standard</span></span>
- <span data-ttu-id="4d9f0-160">Beta</span><span class="sxs-lookup"><span data-stu-id="4d9f0-160">Premium</span></span>
- <span data-ttu-id="4d9f0-161">Warehouse</span><span class="sxs-lookup"><span data-stu-id="4d9f0-161">DataWarehouse</span></span>
- <span data-ttu-id="4d9f0-162">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="4d9f0-162">Free</span></span>
- <span data-ttu-id="4d9f0-163">Sträckning</span><span class="sxs-lookup"><span data-stu-id="4d9f0-163">Stretch</span></span>
- <span data-ttu-id="4d9f0-164">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="4d9f0-164">GeneralPurpose</span></span>
- <span data-ttu-id="4d9f0-165">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="4d9f0-165">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9f0-166">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4d9f0-166">-ElasticPoolName</span></span>
<span data-ttu-id="4d9f0-167">Anger namnet på den Elastic pool som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-167">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9f0-168">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4d9f0-168">-LicenseType</span></span>
<span data-ttu-id="4d9f0-169">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-169">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="4d9f0-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d9f0-170">-ResourceGroupName</span></span>
<span data-ttu-id="4d9f0-171">Anger namnet på den resurs grupp som den här cmdleten tilldelar den elastiska poolen till.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-171">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="4d9f0-172">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4d9f0-172">-ServerName</span></span>
<span data-ttu-id="4d9f0-173">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-173">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="4d9f0-174">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="4d9f0-174">-StorageMB</span></span>
<span data-ttu-id="4d9f0-175">Anger lagrings gränsen (i MB) för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-175">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="4d9f0-176">Om du inte anger den här parametern beräknar den här cmdleten ett värde som är beroende av värdet för *DTU* -parametern.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-176">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="4d9f0-177">Se [eDTU-och lagrings gränser](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) för möjliga värden.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-177">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="4d9f0-178">-Taggar</span><span class="sxs-lookup"><span data-stu-id="4d9f0-178">-Tags</span></span>
<span data-ttu-id="4d9f0-179">Anger en ord lista med par med nyckelord i form av en hash-tabell som denna cmdlet associerar med den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-179">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="4d9f0-180">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="4d9f0-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4d9f0-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="4d9f0-181">-VCore</span></span>
<span data-ttu-id="4d9f0-182">Totalt antal delade vCores för den Elastic SQL Azure-poolen.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-182">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9f0-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="4d9f0-183">-ZoneRedundant</span></span>
<span data-ttu-id="4d9f0-184">Zonens redundans som ska kopplas till den Elastic Azure SQL-poolen</span><span class="sxs-lookup"><span data-stu-id="4d9f0-184">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="4d9f0-185">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d9f0-185">-Confirm</span></span>
<span data-ttu-id="4d9f0-186">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d9f0-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d9f0-187">-WhatIf</span></span>
<span data-ttu-id="4d9f0-188">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d9f0-189">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d9f0-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9f0-190">CommonParameters</span></span>
<span data-ttu-id="4d9f0-191">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d9f0-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9f0-192">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d9f0-192">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9f0-193">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d9f0-193">INPUTS</span></span>

### <span data-ttu-id="4d9f0-194">System. String</span><span class="sxs-lookup"><span data-stu-id="4d9f0-194">System.String</span></span>

## <span data-ttu-id="4d9f0-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d9f0-195">OUTPUTS</span></span>

### <span data-ttu-id="4d9f0-196">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="4d9f0-196">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="4d9f0-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d9f0-197">NOTES</span></span>

## <span data-ttu-id="4d9f0-198">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d9f0-198">RELATED LINKS</span></span>

[<span data-ttu-id="4d9f0-199">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4d9f0-199">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="4d9f0-200">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="4d9f0-200">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="4d9f0-201">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="4d9f0-201">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="4d9f0-202">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4d9f0-202">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="4d9f0-203">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4d9f0-203">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="4d9f0-204">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="4d9f0-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
