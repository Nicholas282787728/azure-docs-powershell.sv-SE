---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fbc0d1e1ac32906c081c5a9714c8420e0f1292e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746618"
---
# <span data-ttu-id="f7b02-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f7b02-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="f7b02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7b02-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b02-103">Skapar en elastisk databas för en SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f7b02-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="f7b02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7b02-104">SYNTAX</span></span>

### <span data-ttu-id="f7b02-105">DtuBasedPool (standard)</span><span class="sxs-lookup"><span data-stu-id="f7b02-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b02-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="f7b02-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b02-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7b02-107">DESCRIPTION</span></span>
<span data-ttu-id="f7b02-108">Cmdleten **New-AzSqlElasticPool** skapar en elastisk databas för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f7b02-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="f7b02-109">Flera parametrar ( *-DTU,-DatabaseDtuMin och-DatabaseDtuMax* ) kräver att det värde som anges är från listan över giltiga värden för den parametern.</span><span class="sxs-lookup"><span data-stu-id="f7b02-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="f7b02-110">Till exempel kan-DatabaseDtuMax för en standard-100 eDTU-pool bara vara 10, 20, 50 eller 100.</span><span class="sxs-lookup"><span data-stu-id="f7b02-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="f7b02-111">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f7b02-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="f7b02-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7b02-112">EXAMPLES</span></span>

### <span data-ttu-id="f7b02-113">Exempel 1: skapa en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="f7b02-113">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="f7b02-114">Det här kommandot skapar en elastisk pool i standard tjänst nivån som heter ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="f7b02-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="f7b02-115">Servern med namnet Server01, tilldelad till en Azure-adressresurs med namnet ResourceGroup01, är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="f7b02-116">Kommandot anger värden för egenskapen DTU för poolen och databaserna i poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="f7b02-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7b02-117">PARAMETERS</span></span>

### <span data-ttu-id="f7b02-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7b02-118">-AsJob</span></span>
<span data-ttu-id="f7b02-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f7b02-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7b02-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="f7b02-120">-ComputeGeneration</span></span>
<span data-ttu-id="f7b02-121">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="f7b02-121">The compute generation to assign.</span></span>

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

### <span data-ttu-id="f7b02-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="f7b02-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="f7b02-123">Anger det maximala antalet databas data flödes enheter (DTUs) som en enskild databas i poolen kan förbruka.</span><span class="sxs-lookup"><span data-stu-id="f7b02-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="f7b02-124">Standardvärdena för de olika versionerna är följande:</span><span class="sxs-lookup"><span data-stu-id="f7b02-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="f7b02-125">Basisk.</span><span class="sxs-lookup"><span data-stu-id="f7b02-125">Basic.</span></span> <span data-ttu-id="f7b02-126">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="f7b02-126">5 DTUs</span></span>
- <span data-ttu-id="f7b02-127">Standar.</span><span class="sxs-lookup"><span data-stu-id="f7b02-127">Standard.</span></span> <span data-ttu-id="f7b02-128">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="f7b02-128">100 DTUs</span></span>
- <span data-ttu-id="f7b02-129">Beta.</span><span class="sxs-lookup"><span data-stu-id="f7b02-129">Premium.</span></span> <span data-ttu-id="f7b02-130">125 DTUs mer information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="f7b02-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="f7b02-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="f7b02-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="f7b02-132">Anger det minsta antal DTUs som den elastiska poolen garanterar till alla databaser i poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="f7b02-133">Standardvärdet är noll (0).</span><span class="sxs-lookup"><span data-stu-id="f7b02-133">The default value is zero (0).</span></span>
<span data-ttu-id="f7b02-134">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f7b02-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="f7b02-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="f7b02-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="f7b02-136">Maxmium VCore-nummer alla SqlAzure-databaser kan använda poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="f7b02-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="f7b02-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="f7b02-138">Det minsta VCore numret som valfri SqlAzure-databas kan använda i poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="f7b02-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b02-139">-DefaultProfile</span></span>
<span data-ttu-id="f7b02-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f7b02-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7b02-141">-DTU</span><span class="sxs-lookup"><span data-stu-id="f7b02-141">-Dtu</span></span>
<span data-ttu-id="f7b02-142">Anger det totala antalet delade DTUs för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="f7b02-143">Standardvärdena för de olika versionerna är följande:</span><span class="sxs-lookup"><span data-stu-id="f7b02-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="f7b02-144">Basisk.</span><span class="sxs-lookup"><span data-stu-id="f7b02-144">Basic.</span></span>
<span data-ttu-id="f7b02-145">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="f7b02-145">100 DTUs</span></span>
- <span data-ttu-id="f7b02-146">Standar.</span><span class="sxs-lookup"><span data-stu-id="f7b02-146">Standard.</span></span>
<span data-ttu-id="f7b02-147">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="f7b02-147">100 DTUs</span></span>
- <span data-ttu-id="f7b02-148">Beta.</span><span class="sxs-lookup"><span data-stu-id="f7b02-148">Premium.</span></span>
<span data-ttu-id="f7b02-149">125 DTUs mer information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f7b02-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="f7b02-150">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="f7b02-150">-Edition</span></span>
<span data-ttu-id="f7b02-151">Anger den version av Azure SQL-databasen som används för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="f7b02-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f7b02-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7b02-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="f7b02-153">None</span></span>
- <span data-ttu-id="f7b02-154">Basisk</span><span class="sxs-lookup"><span data-stu-id="f7b02-154">Basic</span></span>
- <span data-ttu-id="f7b02-155">Standar</span><span class="sxs-lookup"><span data-stu-id="f7b02-155">Standard</span></span>
- <span data-ttu-id="f7b02-156">Beta</span><span class="sxs-lookup"><span data-stu-id="f7b02-156">Premium</span></span>
- <span data-ttu-id="f7b02-157">Warehouse</span><span class="sxs-lookup"><span data-stu-id="f7b02-157">DataWarehouse</span></span>
- <span data-ttu-id="f7b02-158">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="f7b02-158">Free</span></span>
- <span data-ttu-id="f7b02-159">Sträckning</span><span class="sxs-lookup"><span data-stu-id="f7b02-159">Stretch</span></span>
- <span data-ttu-id="f7b02-160">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="f7b02-160">GeneralPurpose</span></span>
- <span data-ttu-id="f7b02-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="f7b02-161">BusinessCritical</span></span>

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

### <span data-ttu-id="f7b02-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f7b02-162">-ElasticPoolName</span></span>
<span data-ttu-id="f7b02-163">Anger namnet på den Elastic pool som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="f7b02-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f7b02-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f7b02-164">-LicenseType</span></span>
<span data-ttu-id="f7b02-165">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="f7b02-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b02-166">-ResourceGroupName</span></span>
<span data-ttu-id="f7b02-167">Anger namnet på den resurs grupp som den här cmdleten tilldelar den elastiska poolen till.</span><span class="sxs-lookup"><span data-stu-id="f7b02-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="f7b02-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f7b02-168">-ServerName</span></span>
<span data-ttu-id="f7b02-169">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-169">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="f7b02-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="f7b02-170">-StorageMB</span></span>
<span data-ttu-id="f7b02-171">Anger lagrings gränsen (i MB) för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="f7b02-172">Om du inte anger den här parametern beräknar den här cmdleten ett värde som är beroende av värdet för *DTU* -parametern.</span><span class="sxs-lookup"><span data-stu-id="f7b02-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="f7b02-173">Se [eDTU-och lagrings gränser](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) för möjliga värden.</span><span class="sxs-lookup"><span data-stu-id="f7b02-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="f7b02-174">-Taggar</span><span class="sxs-lookup"><span data-stu-id="f7b02-174">-Tags</span></span>
<span data-ttu-id="f7b02-175">Anger en ord lista med par med nyckelord i form av en hash-tabell som denna cmdlet associerar med den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="f7b02-176">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f7b02-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f7b02-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="f7b02-177">-VCore</span></span>
<span data-ttu-id="f7b02-178">Totalt antal delade vCores för den Elastic SQL Azure-poolen.</span><span class="sxs-lookup"><span data-stu-id="f7b02-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="f7b02-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="f7b02-179">-ZoneRedundant</span></span>
<span data-ttu-id="f7b02-180">Zonens redundans som ska kopplas till den Elastic Azure SQL-poolen</span><span class="sxs-lookup"><span data-stu-id="f7b02-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="f7b02-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7b02-181">-Confirm</span></span>
<span data-ttu-id="f7b02-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7b02-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b02-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b02-183">-WhatIf</span></span>
<span data-ttu-id="f7b02-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7b02-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b02-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7b02-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b02-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b02-186">CommonParameters</span></span>
<span data-ttu-id="f7b02-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b02-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b02-188">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7b02-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b02-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7b02-189">INPUTS</span></span>

### <span data-ttu-id="f7b02-190">System. String</span><span class="sxs-lookup"><span data-stu-id="f7b02-190">System.String</span></span>

## <span data-ttu-id="f7b02-191">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7b02-191">OUTPUTS</span></span>

### <span data-ttu-id="f7b02-192">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="f7b02-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="f7b02-193">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7b02-193">NOTES</span></span>

## <span data-ttu-id="f7b02-194">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7b02-194">RELATED LINKS</span></span>

[<span data-ttu-id="f7b02-195">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f7b02-195">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="f7b02-196">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f7b02-196">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="f7b02-197">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f7b02-197">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="f7b02-198">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f7b02-198">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="f7b02-199">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f7b02-199">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="f7b02-200">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="f7b02-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
