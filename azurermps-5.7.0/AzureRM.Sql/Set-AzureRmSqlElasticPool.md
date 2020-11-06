---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579283"
---
# <span data-ttu-id="3d717-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d717-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="3d717-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d717-102">SYNOPSIS</span></span>
<span data-ttu-id="3d717-103">Ändrar egenskaper för en Elastic Database-pool i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3d717-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d717-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d717-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d717-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d717-105">DESCRIPTION</span></span>
<span data-ttu-id="3d717-106">Cmdleten **set-AzureRmSqlElasticPool** anger egenskaper för en elastisk pool i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="3d717-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="3d717-107">Denna cmdlet kan ändra eDTUs per pool ( *DTU* ), Max storlek per pool ( *StorageMB* ), högsta EDTUs per databas ( *DatabaseDtuMax* ) och minimum eDTUs per databas ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="3d717-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="3d717-108">Flera parametrar ( *-DTU,-DatabaseDtuMin och-DatabaseDtuMax* ) kräver att det värde som anges är från listan över giltiga värden för den parametern.</span><span class="sxs-lookup"><span data-stu-id="3d717-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="3d717-109">Till exempel kan-DatabaseDtuMax för en standard-100 eDTU-pool bara vara 10, 20, 50 eller 100.</span><span class="sxs-lookup"><span data-stu-id="3d717-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="3d717-110">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3d717-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="3d717-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d717-111">EXAMPLES</span></span>

### <span data-ttu-id="3d717-112">Exempel 1: ändra egenskaper för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="3d717-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="3d717-113">Det här kommandot ändrar egenskaper för en elastisk pool med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="3d717-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="3d717-114">Kommandot anger antalet DTUs för den elastiska poolen till 1000 och ställer in minimum-och maximum-DTUs.</span><span class="sxs-lookup"><span data-stu-id="3d717-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="3d717-115">Exempel 2: ändra maximal lagrings storlek för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="3d717-115">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="3d717-116">Det här kommandot ändrar egenskaper för en elastisk pool med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="3d717-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="3d717-117">Kommandot anger den maximala lagrings platsen för en elastisk pool till 2 TB.</span><span class="sxs-lookup"><span data-stu-id="3d717-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="3d717-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d717-118">PARAMETERS</span></span>

### <span data-ttu-id="3d717-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d717-119">-AsJob</span></span>
<span data-ttu-id="3d717-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3d717-120">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-121">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="3d717-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="3d717-122">Anger maximalt antal DTUs som en enskild databas i poolen kan använda.</span><span class="sxs-lookup"><span data-stu-id="3d717-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="3d717-123">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3d717-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="3d717-124">Standardvärdena för olika utgåvor är följande:</span><span class="sxs-lookup"><span data-stu-id="3d717-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="3d717-125">Basisk.</span><span class="sxs-lookup"><span data-stu-id="3d717-125">Basic.</span></span>  <span data-ttu-id="3d717-126">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="3d717-126">5 DTUs</span></span>
- <span data-ttu-id="3d717-127">Standar.</span><span class="sxs-lookup"><span data-stu-id="3d717-127">Standard.</span></span> <span data-ttu-id="3d717-128">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="3d717-128">100 DTUs</span></span>
- <span data-ttu-id="3d717-129">Beta.</span><span class="sxs-lookup"><span data-stu-id="3d717-129">Premium.</span></span> <span data-ttu-id="3d717-130">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="3d717-130">125 DTUs</span></span>


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="3d717-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="3d717-132">Anger det minsta antal DTUs som den elastiska poolen garanterar till alla databaser i poolen.</span><span class="sxs-lookup"><span data-stu-id="3d717-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="3d717-133">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3d717-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="3d717-134">Standardvärdet är noll (0).</span><span class="sxs-lookup"><span data-stu-id="3d717-134">The default value is zero (0).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d717-135">-DefaultProfile</span></span>
<span data-ttu-id="3d717-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3d717-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-137">-DTU</span><span class="sxs-lookup"><span data-stu-id="3d717-137">-Dtu</span></span>
<span data-ttu-id="3d717-138">Anger det totala antalet delade DTUs för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="3d717-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="3d717-139">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3d717-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="3d717-140">Standardvärdena för olika utgåvor är följande:</span><span class="sxs-lookup"><span data-stu-id="3d717-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="3d717-141">Basisk.</span><span class="sxs-lookup"><span data-stu-id="3d717-141">Basic.</span></span> <span data-ttu-id="3d717-142">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="3d717-142">100 DTUs</span></span>
- <span data-ttu-id="3d717-143">Standar.</span><span class="sxs-lookup"><span data-stu-id="3d717-143">Standard.</span></span> <span data-ttu-id="3d717-144">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="3d717-144">100 DTUs</span></span>
- <span data-ttu-id="3d717-145">Beta.</span><span class="sxs-lookup"><span data-stu-id="3d717-145">Premium.</span></span> <span data-ttu-id="3d717-146">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="3d717-146">125 DTUs</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-147">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="3d717-147">-Edition</span></span>
<span data-ttu-id="3d717-148">Anger versionen av Azure SQL-databasen för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="3d717-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="3d717-149">Du kan inte ändra versionen.</span><span class="sxs-lookup"><span data-stu-id="3d717-149">You cannot change the edition.</span></span> <span data-ttu-id="3d717-150">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3d717-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d717-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d717-151">None</span></span>
- <span data-ttu-id="3d717-152">Basisk</span><span class="sxs-lookup"><span data-stu-id="3d717-152">Basic</span></span>
- <span data-ttu-id="3d717-153">Standar</span><span class="sxs-lookup"><span data-stu-id="3d717-153">Standard</span></span>
- <span data-ttu-id="3d717-154">Beta</span><span class="sxs-lookup"><span data-stu-id="3d717-154">Premium</span></span>
- <span data-ttu-id="3d717-155">Warehouse</span><span class="sxs-lookup"><span data-stu-id="3d717-155">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-156">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3d717-156">-ElasticPoolName</span></span>
<span data-ttu-id="3d717-157">Anger namnet på den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="3d717-157">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d717-158">-ResourceGroupName</span></span>
<span data-ttu-id="3d717-159">Anger namnet på den resurs grupp som den elastiska poolen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="3d717-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d717-160">-ServerName</span></span>
<span data-ttu-id="3d717-161">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="3d717-161">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="3d717-162">-StorageMB</span></span>
<span data-ttu-id="3d717-163">Anger lagrings gränsen (i MB) för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="3d717-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="3d717-164">Mer information finns i New-AzureRmSqlElasticPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d717-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-165">-Taggar</span><span class="sxs-lookup"><span data-stu-id="3d717-165">-Tags</span></span>
<span data-ttu-id="3d717-166">Anger en ord lista med par med nyckelord som denna cmdlet associerar med den Elastic pool som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3d717-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="3d717-167">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="3d717-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="3d717-168">-ZoneRedundant</span></span>
<span data-ttu-id="3d717-169">Zonens redundans som ska kopplas till den Elastic Azure SQL-poolen</span><span class="sxs-lookup"><span data-stu-id="3d717-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-170">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d717-170">-Confirm</span></span>
<span data-ttu-id="3d717-171">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d717-171">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d717-172">-WhatIf</span></span>
<span data-ttu-id="3d717-173">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d717-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d717-174">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d717-174">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d717-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d717-175">CommonParameters</span></span>
<span data-ttu-id="3d717-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d717-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d717-177">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d717-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d717-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d717-178">INPUTS</span></span>

### <span data-ttu-id="3d717-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d717-179">None</span></span>
<span data-ttu-id="3d717-180">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3d717-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d717-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d717-181">OUTPUTS</span></span>

### <span data-ttu-id="3d717-182">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="3d717-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="3d717-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d717-183">NOTES</span></span>

## <span data-ttu-id="3d717-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d717-184">RELATED LINKS</span></span>

[<span data-ttu-id="3d717-185">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d717-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="3d717-186">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="3d717-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="3d717-187">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="3d717-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="3d717-188">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d717-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="3d717-189">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="3d717-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
