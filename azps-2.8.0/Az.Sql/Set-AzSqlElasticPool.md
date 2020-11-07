---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: d78ca6ef2e342982dc6f5e53e8fff4de606dd5ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920443"
---
# <span data-ttu-id="72e25-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="72e25-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="72e25-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72e25-102">SYNOPSIS</span></span>
<span data-ttu-id="72e25-103">Ändrar egenskaper för en Elastic Database-pool i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="72e25-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="72e25-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72e25-104">SYNTAX</span></span>

### <span data-ttu-id="72e25-105">DtuBasedPool (standard)</span><span class="sxs-lookup"><span data-stu-id="72e25-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72e25-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="72e25-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e25-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72e25-107">DESCRIPTION</span></span>
<span data-ttu-id="72e25-108">Cmdleten **set-AzSqlElasticPool** anger egenskaper för en elastisk pool i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="72e25-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="72e25-109">Denna cmdlet kan ändra eDTUs per pool ( *DTU* ), Max storlek per pool ( *StorageMB* ), högsta EDTUs per databas ( *DatabaseDtuMax* ) och minimum eDTUs per databas ( *DatabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="72e25-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="72e25-110">Flera parametrar ( *-DTU,-DatabaseDtuMin och-DatabaseDtuMax* ) kräver att det värde som anges är från listan över giltiga värden för den parametern.</span><span class="sxs-lookup"><span data-stu-id="72e25-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="72e25-111">Till exempel kan-DatabaseDtuMax för en standard-100 eDTU-pool bara vara 10, 20, 50 eller 100.</span><span class="sxs-lookup"><span data-stu-id="72e25-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="72e25-112">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="72e25-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="72e25-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72e25-113">EXAMPLES</span></span>

### <span data-ttu-id="72e25-114">Exempel 1: ändra egenskaper för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="72e25-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="72e25-115">Det här kommandot ändrar egenskaper för en elastisk pool med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="72e25-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="72e25-116">Kommandot anger antalet DTUs för den elastiska poolen till 1000 och ställer in minimum-och maximum-DTUs.</span><span class="sxs-lookup"><span data-stu-id="72e25-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="72e25-117">Exempel 2: ändra maximal lagrings storlek för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="72e25-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="72e25-118">Det här kommandot ändrar egenskaper för en elastisk pool med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="72e25-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="72e25-119">Kommandot anger den maximala lagrings platsen för en elastisk pool till 2 TB.</span><span class="sxs-lookup"><span data-stu-id="72e25-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="72e25-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72e25-120">PARAMETERS</span></span>

### <span data-ttu-id="72e25-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72e25-121">-AsJob</span></span>
<span data-ttu-id="72e25-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="72e25-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72e25-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="72e25-123">-ComputeGeneration</span></span>
<span data-ttu-id="72e25-124">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="72e25-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e25-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="72e25-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="72e25-126">Anger maximalt antal DTUs som en enskild databas i poolen kan använda.</span><span class="sxs-lookup"><span data-stu-id="72e25-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="72e25-127">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="72e25-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="72e25-128">Standardvärdena för olika utgåvor är följande:</span><span class="sxs-lookup"><span data-stu-id="72e25-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="72e25-129">Basisk.</span><span class="sxs-lookup"><span data-stu-id="72e25-129">Basic.</span></span>  <span data-ttu-id="72e25-130">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="72e25-130">5 DTUs</span></span>
- <span data-ttu-id="72e25-131">Standar.</span><span class="sxs-lookup"><span data-stu-id="72e25-131">Standard.</span></span> <span data-ttu-id="72e25-132">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="72e25-132">100 DTUs</span></span>
- <span data-ttu-id="72e25-133">Beta.</span><span class="sxs-lookup"><span data-stu-id="72e25-133">Premium.</span></span> <span data-ttu-id="72e25-134">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="72e25-134">125 DTUs</span></span>

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

### <span data-ttu-id="72e25-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="72e25-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="72e25-136">Anger det minsta antal DTUs som den elastiska poolen garanterar till alla databaser i poolen.</span><span class="sxs-lookup"><span data-stu-id="72e25-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="72e25-137">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="72e25-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="72e25-138">Standardvärdet är noll (0).</span><span class="sxs-lookup"><span data-stu-id="72e25-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="72e25-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="72e25-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="72e25-140">Det högsta VCore-numret som en SqlAzure-databas kan använda i poolen.</span><span class="sxs-lookup"><span data-stu-id="72e25-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="72e25-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="72e25-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="72e25-142">Det minsta VCore numret som valfri SqlAzure-databas kan använda i poolen.</span><span class="sxs-lookup"><span data-stu-id="72e25-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="72e25-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e25-143">-DefaultProfile</span></span>
<span data-ttu-id="72e25-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72e25-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72e25-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="72e25-145">-Dtu</span></span>
<span data-ttu-id="72e25-146">Anger det totala antalet delade DTUs för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="72e25-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="72e25-147">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="72e25-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="72e25-148">Standardvärdena för olika utgåvor är följande:</span><span class="sxs-lookup"><span data-stu-id="72e25-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="72e25-149">Basisk.</span><span class="sxs-lookup"><span data-stu-id="72e25-149">Basic.</span></span> <span data-ttu-id="72e25-150">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="72e25-150">100 DTUs</span></span>
- <span data-ttu-id="72e25-151">Standar.</span><span class="sxs-lookup"><span data-stu-id="72e25-151">Standard.</span></span> <span data-ttu-id="72e25-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="72e25-152">100 DTUs</span></span>
- <span data-ttu-id="72e25-153">Beta.</span><span class="sxs-lookup"><span data-stu-id="72e25-153">Premium.</span></span> <span data-ttu-id="72e25-154">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="72e25-154">125 DTUs</span></span>

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

### <span data-ttu-id="72e25-155">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="72e25-155">-Edition</span></span>
<span data-ttu-id="72e25-156">Anger versionen av Azure SQL-databasen för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="72e25-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="72e25-157">Du kan inte ändra versionen.</span><span class="sxs-lookup"><span data-stu-id="72e25-157">You cannot change the edition.</span></span> <span data-ttu-id="72e25-158">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="72e25-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72e25-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="72e25-159">None</span></span>
- <span data-ttu-id="72e25-160">Basisk</span><span class="sxs-lookup"><span data-stu-id="72e25-160">Basic</span></span>
- <span data-ttu-id="72e25-161">Standar</span><span class="sxs-lookup"><span data-stu-id="72e25-161">Standard</span></span>
- <span data-ttu-id="72e25-162">Beta</span><span class="sxs-lookup"><span data-stu-id="72e25-162">Premium</span></span>
- <span data-ttu-id="72e25-163">Warehouse</span><span class="sxs-lookup"><span data-stu-id="72e25-163">DataWarehouse</span></span>
- <span data-ttu-id="72e25-164">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="72e25-164">Free</span></span>
- <span data-ttu-id="72e25-165">Sträckning</span><span class="sxs-lookup"><span data-stu-id="72e25-165">Stretch</span></span>
- <span data-ttu-id="72e25-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="72e25-166">GeneralPurpose</span></span>
- <span data-ttu-id="72e25-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="72e25-167">BusinessCritical</span></span>

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

### <span data-ttu-id="72e25-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="72e25-168">-ElasticPoolName</span></span>
<span data-ttu-id="72e25-169">Anger namnet på den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="72e25-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="72e25-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="72e25-170">-LicenseType</span></span>
<span data-ttu-id="72e25-171">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="72e25-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="72e25-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e25-172">-ResourceGroupName</span></span>
<span data-ttu-id="72e25-173">Anger namnet på den resurs grupp som den elastiska poolen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="72e25-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="72e25-174">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72e25-174">-ServerName</span></span>
<span data-ttu-id="72e25-175">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="72e25-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="72e25-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="72e25-176">-StorageMB</span></span>
<span data-ttu-id="72e25-177">Anger lagrings gränsen (i MB) för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="72e25-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="72e25-178">Mer information finns i New-AzSqlElasticPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72e25-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="72e25-179">-Taggar</span><span class="sxs-lookup"><span data-stu-id="72e25-179">-Tags</span></span>
<span data-ttu-id="72e25-180">Anger en ord lista med par med nyckelord som denna cmdlet associerar med den Elastic pool som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="72e25-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="72e25-181">Till exempel: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="72e25-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="72e25-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="72e25-182">-VCore</span></span>
<span data-ttu-id="72e25-183">Totalt antal delade vCore för den Elastic SQL Azure-poolen.</span><span class="sxs-lookup"><span data-stu-id="72e25-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e25-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="72e25-184">-ZoneRedundant</span></span>
<span data-ttu-id="72e25-185">Zonens redundans som ska kopplas till den Elastic Azure SQL-poolen</span><span class="sxs-lookup"><span data-stu-id="72e25-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="72e25-186">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72e25-186">-Confirm</span></span>
<span data-ttu-id="72e25-187">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72e25-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72e25-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e25-188">-WhatIf</span></span>
<span data-ttu-id="72e25-189">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72e25-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72e25-190">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72e25-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72e25-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e25-191">CommonParameters</span></span>
<span data-ttu-id="72e25-192">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e25-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e25-193">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72e25-193">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e25-194">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72e25-194">INPUTS</span></span>

### <span data-ttu-id="72e25-195">System. String</span><span class="sxs-lookup"><span data-stu-id="72e25-195">System.String</span></span>

## <span data-ttu-id="72e25-196">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72e25-196">OUTPUTS</span></span>

### <span data-ttu-id="72e25-197">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="72e25-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="72e25-198">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72e25-198">NOTES</span></span>

## <span data-ttu-id="72e25-199">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72e25-199">RELATED LINKS</span></span>

[<span data-ttu-id="72e25-200">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="72e25-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="72e25-201">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="72e25-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="72e25-202">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="72e25-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="72e25-203">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="72e25-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="72e25-204">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="72e25-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
