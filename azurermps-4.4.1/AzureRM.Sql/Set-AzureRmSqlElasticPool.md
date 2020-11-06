---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575762"
---
# <span data-ttu-id="32605-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="32605-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="32605-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32605-102">SYNOPSIS</span></span>
<span data-ttu-id="32605-103">Ändrar egenskaper för en Elastic Database-pool i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="32605-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32605-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32605-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32605-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32605-105">DESCRIPTION</span></span>
<span data-ttu-id="32605-106">Cmdleten **set-AzureRmSqlElasticPool** ändrar egenskaper för en elastisk Databasvy i en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="32605-106">The **Set-AzureRmSqlElasticPool** cmdlet modifies properties for an elastic database pool in an Azure SQL Database.</span></span> <span data-ttu-id="32605-107">Med den här cmdleten kan du ändra minsta antalet databas data flödes enheter (DTUs) per databas utöver det högsta antalet DTUs per databas, antal DTUs för poolen och lagrings gränsen för poolen.</span><span class="sxs-lookup"><span data-stu-id="32605-107">This cmdlet can modify the minimum Database Throughput Units (DTUs) per database in addition to the maximum DTUs per database, the number of DTUs for the pool, and the storage limit for the pool.</span></span>

<span data-ttu-id="32605-108">Flera parametrar ( *-DTU,-DatabaseDtuMin och-DatabaseDtuMax* ) kräver att det värde som anges är från listan över giltiga värden för den parametern.</span><span class="sxs-lookup"><span data-stu-id="32605-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="32605-109">Till exempel kan-DatabaseDtuMax för en standard-100 eDTU-pool bara vara 10, 20, 50 eller 100.</span><span class="sxs-lookup"><span data-stu-id="32605-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="32605-110">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="32605-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="32605-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32605-111">EXAMPLES</span></span>

### <span data-ttu-id="32605-112">Exempel 1: ändra egenskaper för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="32605-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="32605-113">Det här kommandot ändrar egenskaper för en elastisk pool med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="32605-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="32605-114">Kommandot anger antalet DTUs för den elastiska poolen till 1000 och ställer in minimum-och maximum-DTUs.</span><span class="sxs-lookup"><span data-stu-id="32605-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="32605-115">Exempel 2: ändra Max utrymmet för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="32605-115">Example 2: Modify the max storage of an elastic pool</span></span>
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

<span data-ttu-id="32605-116">Det här kommandot ändrar egenskaper för en elastisk pool med namnet elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="32605-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="32605-117">Kommandot anger den maximala lagrings platsen för en elastisk pool till 2 TB.</span><span class="sxs-lookup"><span data-stu-id="32605-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="32605-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32605-118">PARAMETERS</span></span>

### <span data-ttu-id="32605-119">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="32605-119">-DatabaseDtuMax</span></span>
<span data-ttu-id="32605-120">Anger maximalt antal DTUs som en enskild databas i poolen kan använda.</span><span class="sxs-lookup"><span data-stu-id="32605-120">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="32605-121">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="32605-121">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="32605-122">Standardvärdena för olika utgåvor är följande:</span><span class="sxs-lookup"><span data-stu-id="32605-122">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="32605-123">Basisk.</span><span class="sxs-lookup"><span data-stu-id="32605-123">Basic.</span></span>  <span data-ttu-id="32605-124">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="32605-124">5 DTUs</span></span>
- <span data-ttu-id="32605-125">Standar.</span><span class="sxs-lookup"><span data-stu-id="32605-125">Standard.</span></span> <span data-ttu-id="32605-126">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="32605-126">100 DTUs</span></span>
- <span data-ttu-id="32605-127">Beta.</span><span class="sxs-lookup"><span data-stu-id="32605-127">Premium.</span></span> <span data-ttu-id="32605-128">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="32605-128">125 DTUs</span></span>


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

### <span data-ttu-id="32605-129">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="32605-129">-DatabaseDtuMin</span></span>
<span data-ttu-id="32605-130">Anger det minsta antal DTUs som den elastiska poolen garanterar till alla databaser i poolen.</span><span class="sxs-lookup"><span data-stu-id="32605-130">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="32605-131">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="32605-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="32605-132">Standardvärdet är noll (0).</span><span class="sxs-lookup"><span data-stu-id="32605-132">The default value is zero (0).</span></span>

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

### <span data-ttu-id="32605-133">-DTU</span><span class="sxs-lookup"><span data-stu-id="32605-133">-Dtu</span></span>
<span data-ttu-id="32605-134">Anger det totala antalet delade DTUs för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="32605-134">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="32605-135">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="32605-135">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="32605-136">Standardvärdena för olika utgåvor är följande:</span><span class="sxs-lookup"><span data-stu-id="32605-136">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="32605-137">Basisk.</span><span class="sxs-lookup"><span data-stu-id="32605-137">Basic.</span></span> <span data-ttu-id="32605-138">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="32605-138">100 DTUs</span></span>
- <span data-ttu-id="32605-139">Standar.</span><span class="sxs-lookup"><span data-stu-id="32605-139">Standard.</span></span> <span data-ttu-id="32605-140">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="32605-140">100 DTUs</span></span>
- <span data-ttu-id="32605-141">Beta.</span><span class="sxs-lookup"><span data-stu-id="32605-141">Premium.</span></span> <span data-ttu-id="32605-142">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="32605-142">125 DTUs</span></span>

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

### <span data-ttu-id="32605-143">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="32605-143">-Edition</span></span>
<span data-ttu-id="32605-144">Anger versionen av Azure SQL-databasen för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="32605-144">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="32605-145">Du kan inte ändra versionen.</span><span class="sxs-lookup"><span data-stu-id="32605-145">You cannot change the edition.</span></span> <span data-ttu-id="32605-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="32605-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32605-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="32605-147">None</span></span>
- <span data-ttu-id="32605-148">Basisk</span><span class="sxs-lookup"><span data-stu-id="32605-148">Basic</span></span>
- <span data-ttu-id="32605-149">Standar</span><span class="sxs-lookup"><span data-stu-id="32605-149">Standard</span></span>
- <span data-ttu-id="32605-150">Beta</span><span class="sxs-lookup"><span data-stu-id="32605-150">Premium</span></span>
- <span data-ttu-id="32605-151">Premie</span><span class="sxs-lookup"><span data-stu-id="32605-151">PremiumRS</span></span>
- <span data-ttu-id="32605-152">Warehouse</span><span class="sxs-lookup"><span data-stu-id="32605-152">DataWarehouse</span></span>
- <span data-ttu-id="32605-153">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="32605-153">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32605-154">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="32605-154">-ElasticPoolName</span></span>
<span data-ttu-id="32605-155">Anger namnet på den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="32605-155">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="32605-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32605-156">-ResourceGroupName</span></span>
<span data-ttu-id="32605-157">Anger namnet på den resurs grupp som den elastiska poolen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="32605-157">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="32605-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32605-158">-ServerName</span></span>
<span data-ttu-id="32605-159">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="32605-159">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="32605-160">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="32605-160">-StorageMB</span></span>
<span data-ttu-id="32605-161">Anger lagrings gränsen (i MB) för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="32605-161">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="32605-162">Mer information finns i New-AzureRmSqlElasticPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32605-162">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="32605-163">-Taggar</span><span class="sxs-lookup"><span data-stu-id="32605-163">-Tags</span></span>
<span data-ttu-id="32605-164">Anger en ord lista med par med nyckelord som denna cmdlet associerar med den Elastic pool som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="32605-164">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="32605-165">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="32605-165">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="32605-166">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="32605-166">-Confirm</span></span>
<span data-ttu-id="32605-167">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="32605-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32605-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32605-168">-WhatIf</span></span>
<span data-ttu-id="32605-169">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="32605-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32605-170">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="32605-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32605-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32605-171">-DefaultProfile</span></span>
<span data-ttu-id="32605-172">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32605-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32605-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32605-173">CommonParameters</span></span>
<span data-ttu-id="32605-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32605-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32605-175">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32605-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32605-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32605-176">INPUTS</span></span>

## <span data-ttu-id="32605-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32605-177">OUTPUTS</span></span>

### <span data-ttu-id="32605-178">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="32605-178">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="32605-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32605-179">NOTES</span></span>

## <span data-ttu-id="32605-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32605-180">RELATED LINKS</span></span>

[<span data-ttu-id="32605-181">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="32605-181">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="32605-182">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="32605-182">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="32605-183">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="32605-183">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="32605-184">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="32605-184">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="32605-185">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="32605-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
