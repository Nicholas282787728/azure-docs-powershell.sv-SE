---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 6b059905cdc1e9474ce455f78fac88f282b5ce10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577804"
---
# <span data-ttu-id="92da2-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="92da2-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="92da2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92da2-102">SYNOPSIS</span></span>
<span data-ttu-id="92da2-103">Ändrar egenskaper för en Elastic Database-pool i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="92da2-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92da2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92da2-104">SYNTAX</span></span>

### <span data-ttu-id="92da2-105">DtuBasedPool (standard)</span><span class="sxs-lookup"><span data-stu-id="92da2-105">DtuBasedPool (Default)</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92da2-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="92da2-106">VcoreBasedPool</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92da2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92da2-107">DESCRIPTION</span></span>
<span data-ttu-id="92da2-108">Cmdleten **set-AzureRmSqlElasticPool** anger egenskaper för en elastisk pool i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="92da2-108">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="92da2-109">Denna cmdlet kan ändra eDTUs per pool ( *DTU* ), Max storlek per pool ( *StorageMB* ), högsta EDTUs per databas ( *DatabaseDtuMax* ) och minimum eDTUs per databas ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="92da2-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>
<span data-ttu-id="92da2-110">Flera parametrar ( *-DTU,-DatabaseDtuMin och-DatabaseDtuMax* ) kräver att det värde som anges är från listan över giltiga värden för den parametern.</span><span class="sxs-lookup"><span data-stu-id="92da2-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="92da2-111">Till exempel kan-DatabaseDtuMax för en standard-100 eDTU-pool bara vara 10, 20, 50 eller 100.</span><span class="sxs-lookup"><span data-stu-id="92da2-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="92da2-112">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="92da2-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="92da2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92da2-113">EXAMPLES</span></span>

### <span data-ttu-id="92da2-114">Exempel 1: ändra egenskaper för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="92da2-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="92da2-115">Det här kommandot ändrar egenskaper för en elastisk pool med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="92da2-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="92da2-116">Kommandot anger antalet DTUs för den elastiska poolen till 1000 och ställer in minimum-och maximum-DTUs.</span><span class="sxs-lookup"><span data-stu-id="92da2-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="92da2-117">Exempel 2: ändra maximal lagrings storlek för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="92da2-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="92da2-118">Det här kommandot ändrar egenskaper för en elastisk pool med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="92da2-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="92da2-119">Kommandot anger den maximala lagrings platsen för en elastisk pool till 2 TB.</span><span class="sxs-lookup"><span data-stu-id="92da2-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="92da2-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92da2-120">PARAMETERS</span></span>

### <span data-ttu-id="92da2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92da2-121">-AsJob</span></span>
<span data-ttu-id="92da2-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="92da2-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92da2-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="92da2-123">-ComputeGeneration</span></span>
<span data-ttu-id="92da2-124">Den generationens generering som ska kopplas.</span><span class="sxs-lookup"><span data-stu-id="92da2-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="92da2-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="92da2-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="92da2-126">Anger maximalt antal DTUs som en enskild databas i poolen kan använda.</span><span class="sxs-lookup"><span data-stu-id="92da2-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="92da2-127">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="92da2-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="92da2-128">Standardvärdena för olika utgåvor är följande:</span><span class="sxs-lookup"><span data-stu-id="92da2-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="92da2-129">Basisk.</span><span class="sxs-lookup"><span data-stu-id="92da2-129">Basic.</span></span>  <span data-ttu-id="92da2-130">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="92da2-130">5 DTUs</span></span>
- <span data-ttu-id="92da2-131">Standar.</span><span class="sxs-lookup"><span data-stu-id="92da2-131">Standard.</span></span> <span data-ttu-id="92da2-132">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="92da2-132">100 DTUs</span></span>
- <span data-ttu-id="92da2-133">Beta.</span><span class="sxs-lookup"><span data-stu-id="92da2-133">Premium.</span></span> <span data-ttu-id="92da2-134">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="92da2-134">125 DTUs</span></span>

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

### <span data-ttu-id="92da2-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="92da2-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="92da2-136">Anger det minsta antal DTUs som den elastiska poolen garanterar till alla databaser i poolen.</span><span class="sxs-lookup"><span data-stu-id="92da2-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="92da2-137">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="92da2-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="92da2-138">Standardvärdet är noll (0).</span><span class="sxs-lookup"><span data-stu-id="92da2-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="92da2-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="92da2-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="92da2-140">Maxmium VCore-nummer alla SqlAzure-databaser kan använda poolen.</span><span class="sxs-lookup"><span data-stu-id="92da2-140">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="92da2-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="92da2-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="92da2-142">Det minsta VCore numret som valfri SqlAzure-databas kan använda i poolen.</span><span class="sxs-lookup"><span data-stu-id="92da2-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="92da2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92da2-143">-DefaultProfile</span></span>
<span data-ttu-id="92da2-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="92da2-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92da2-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="92da2-145">-Dtu</span></span>
<span data-ttu-id="92da2-146">Anger det totala antalet delade DTUs för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="92da2-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="92da2-147">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="92da2-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="92da2-148">Standardvärdena för olika utgåvor är följande:</span><span class="sxs-lookup"><span data-stu-id="92da2-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="92da2-149">Basisk.</span><span class="sxs-lookup"><span data-stu-id="92da2-149">Basic.</span></span> <span data-ttu-id="92da2-150">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="92da2-150">100 DTUs</span></span>
- <span data-ttu-id="92da2-151">Standar.</span><span class="sxs-lookup"><span data-stu-id="92da2-151">Standard.</span></span> <span data-ttu-id="92da2-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="92da2-152">100 DTUs</span></span>
- <span data-ttu-id="92da2-153">Beta.</span><span class="sxs-lookup"><span data-stu-id="92da2-153">Premium.</span></span> <span data-ttu-id="92da2-154">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="92da2-154">125 DTUs</span></span>

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

### <span data-ttu-id="92da2-155">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="92da2-155">-Edition</span></span>
<span data-ttu-id="92da2-156">Anger versionen av Azure SQL-databasen för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="92da2-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="92da2-157">Du kan inte ändra versionen.</span><span class="sxs-lookup"><span data-stu-id="92da2-157">You cannot change the edition.</span></span> <span data-ttu-id="92da2-158">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="92da2-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92da2-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="92da2-159">None</span></span>
- <span data-ttu-id="92da2-160">Basisk</span><span class="sxs-lookup"><span data-stu-id="92da2-160">Basic</span></span>
- <span data-ttu-id="92da2-161">Standar</span><span class="sxs-lookup"><span data-stu-id="92da2-161">Standard</span></span>
- <span data-ttu-id="92da2-162">Beta</span><span class="sxs-lookup"><span data-stu-id="92da2-162">Premium</span></span>
- <span data-ttu-id="92da2-163">Warehouse</span><span class="sxs-lookup"><span data-stu-id="92da2-163">DataWarehouse</span></span>
- <span data-ttu-id="92da2-164">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="92da2-164">Free</span></span>
- <span data-ttu-id="92da2-165">Sträckning</span><span class="sxs-lookup"><span data-stu-id="92da2-165">Stretch</span></span>
- <span data-ttu-id="92da2-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="92da2-166">GeneralPurpose</span></span>
- <span data-ttu-id="92da2-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="92da2-167">BusinessCritical</span></span>

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

### <span data-ttu-id="92da2-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="92da2-168">-ElasticPoolName</span></span>
<span data-ttu-id="92da2-169">Anger namnet på den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="92da2-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="92da2-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="92da2-170">-LicenseType</span></span>
<span data-ttu-id="92da2-171">Licens typen för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="92da2-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="92da2-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92da2-172">-ResourceGroupName</span></span>
<span data-ttu-id="92da2-173">Anger namnet på den resurs grupp som den elastiska poolen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="92da2-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="92da2-174">-ServerName</span><span class="sxs-lookup"><span data-stu-id="92da2-174">-ServerName</span></span>
<span data-ttu-id="92da2-175">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="92da2-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="92da2-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="92da2-176">-StorageMB</span></span>
<span data-ttu-id="92da2-177">Anger lagrings gränsen (i MB) för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="92da2-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="92da2-178">Mer information finns i New-AzureRmSqlElasticPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92da2-178">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="92da2-179">-Taggar</span><span class="sxs-lookup"><span data-stu-id="92da2-179">-Tags</span></span>
<span data-ttu-id="92da2-180">Anger en ord lista med par med nyckelord som denna cmdlet associerar med den Elastic pool som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="92da2-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="92da2-181">Till exempel: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="92da2-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="92da2-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="92da2-182">-VCore</span></span>
<span data-ttu-id="92da2-183">Totalt antal delade vCore för den Elastic SQL Azure-poolen.</span><span class="sxs-lookup"><span data-stu-id="92da2-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="92da2-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="92da2-184">-ZoneRedundant</span></span>
<span data-ttu-id="92da2-185">Zonens redundans som ska kopplas till den Elastic Azure SQL-poolen</span><span class="sxs-lookup"><span data-stu-id="92da2-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="92da2-186">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92da2-186">-Confirm</span></span>
<span data-ttu-id="92da2-187">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92da2-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92da2-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92da2-188">-WhatIf</span></span>
<span data-ttu-id="92da2-189">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92da2-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92da2-190">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92da2-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92da2-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92da2-191">CommonParameters</span></span>
<span data-ttu-id="92da2-192">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92da2-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92da2-193">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92da2-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92da2-194">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92da2-194">INPUTS</span></span>

### <span data-ttu-id="92da2-195">System. String</span><span class="sxs-lookup"><span data-stu-id="92da2-195">System.String</span></span>

## <span data-ttu-id="92da2-196">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92da2-196">OUTPUTS</span></span>

### <span data-ttu-id="92da2-197">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="92da2-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="92da2-198">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92da2-198">NOTES</span></span>

## <span data-ttu-id="92da2-199">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92da2-199">RELATED LINKS</span></span>

[<span data-ttu-id="92da2-200">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="92da2-200">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="92da2-201">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="92da2-201">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="92da2-202">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="92da2-202">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="92da2-203">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="92da2-203">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="92da2-204">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="92da2-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
