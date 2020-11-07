---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758370"
---
# <span data-ttu-id="da20b-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="da20b-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="da20b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da20b-102">SYNOPSIS</span></span>
<span data-ttu-id="da20b-103">Skapar en elastisk databas för en SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="da20b-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da20b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da20b-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da20b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da20b-105">DESCRIPTION</span></span>
<span data-ttu-id="da20b-106">Cmdleten **New-AzureRmSqlElasticPool** skapar en elastisk databas för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="da20b-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="da20b-107">Flera parametrar ( *-DTU,-DatabaseDtuMin och-DatabaseDtuMax* ) kräver att det värde som anges är från listan över giltiga värden för den parametern.</span><span class="sxs-lookup"><span data-stu-id="da20b-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="da20b-108">Till exempel kan-DatabaseDtuMax för en standard-100 eDTU-pool bara vara 10, 20, 50 eller 100.</span><span class="sxs-lookup"><span data-stu-id="da20b-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="da20b-109">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="da20b-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="da20b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da20b-110">EXAMPLES</span></span>

### <span data-ttu-id="da20b-111">Exempel 1: skapa en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="da20b-111">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="da20b-112">Det här kommandot skapar en elastisk pool i standard tjänst nivån som heter ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="da20b-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="da20b-113">Servern med namnet Server01, tilldelad till en Azure-adressresurs med namnet ResourceGroup01, är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="da20b-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="da20b-114">Kommandot anger värden för egenskapen DTU för poolen och databaserna i poolen.</span><span class="sxs-lookup"><span data-stu-id="da20b-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="da20b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da20b-115">PARAMETERS</span></span>

### <span data-ttu-id="da20b-116">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="da20b-116">-DatabaseDtuMax</span></span>
<span data-ttu-id="da20b-117">Anger det maximala antalet databas data flödes enheter (DTUs) som en enskild databas i poolen kan förbruka.</span><span class="sxs-lookup"><span data-stu-id="da20b-117">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="da20b-118">Standardvärdena för de olika versionerna är följande:</span><span class="sxs-lookup"><span data-stu-id="da20b-118">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="da20b-119">Basisk.</span><span class="sxs-lookup"><span data-stu-id="da20b-119">Basic.</span></span> <span data-ttu-id="da20b-120">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="da20b-120">5 DTUs</span></span>
- <span data-ttu-id="da20b-121">Standar.</span><span class="sxs-lookup"><span data-stu-id="da20b-121">Standard.</span></span> <span data-ttu-id="da20b-122">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="da20b-122">100 DTUs</span></span>
- <span data-ttu-id="da20b-123">Beta.</span><span class="sxs-lookup"><span data-stu-id="da20b-123">Premium.</span></span> <span data-ttu-id="da20b-124">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="da20b-124">125 DTUs</span></span>

<span data-ttu-id="da20b-125">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="da20b-125">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="da20b-126">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="da20b-126">-DatabaseDtuMin</span></span>
<span data-ttu-id="da20b-127">Anger det minsta antal DTUs som den elastiska poolen garanterar till alla databaser i poolen.</span><span class="sxs-lookup"><span data-stu-id="da20b-127">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="da20b-128">Standardvärdet är noll (0).</span><span class="sxs-lookup"><span data-stu-id="da20b-128">The default value is zero (0).</span></span>

<span data-ttu-id="da20b-129">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="da20b-129">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="da20b-130">-DTU</span><span class="sxs-lookup"><span data-stu-id="da20b-130">-Dtu</span></span>
<span data-ttu-id="da20b-131">Anger det totala antalet delade DTUs för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="da20b-131">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="da20b-132">Standardvärdena för de olika versionerna är följande:</span><span class="sxs-lookup"><span data-stu-id="da20b-132">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="da20b-133">Basisk.</span><span class="sxs-lookup"><span data-stu-id="da20b-133">Basic.</span></span>
<span data-ttu-id="da20b-134">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="da20b-134">100 DTUs</span></span>
- <span data-ttu-id="da20b-135">Standar.</span><span class="sxs-lookup"><span data-stu-id="da20b-135">Standard.</span></span>
<span data-ttu-id="da20b-136">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="da20b-136">100 DTUs</span></span>
- <span data-ttu-id="da20b-137">Beta.</span><span class="sxs-lookup"><span data-stu-id="da20b-137">Premium.</span></span>
<span data-ttu-id="da20b-138">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="da20b-138">125 DTUs</span></span>

<span data-ttu-id="da20b-139">Information om vilka värden som är giltiga finns i tabellen för din specifika poolstorlek i [elastiska pooler](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="da20b-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="da20b-140">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="da20b-140">-Edition</span></span>
<span data-ttu-id="da20b-141">Anger den version av Azure SQL-databasen som används för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="da20b-141">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="da20b-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="da20b-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="da20b-143">Beta</span><span class="sxs-lookup"><span data-stu-id="da20b-143">Premium</span></span>
- <span data-ttu-id="da20b-144">Basisk</span><span class="sxs-lookup"><span data-stu-id="da20b-144">Basic</span></span>
- <span data-ttu-id="da20b-145">Standar</span><span class="sxs-lookup"><span data-stu-id="da20b-145">Standard</span></span>
- <span data-ttu-id="da20b-146">Warehouse</span><span class="sxs-lookup"><span data-stu-id="da20b-146">DataWarehouse</span></span>
- <span data-ttu-id="da20b-147">Sträckning</span><span class="sxs-lookup"><span data-stu-id="da20b-147">Stretch</span></span>
- <span data-ttu-id="da20b-148">Gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="da20b-148">Free</span></span>
- <span data-ttu-id="da20b-149">Premie</span><span class="sxs-lookup"><span data-stu-id="da20b-149">PremiumRS</span></span>

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

### <span data-ttu-id="da20b-150">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="da20b-150">-ElasticPoolName</span></span>
<span data-ttu-id="da20b-151">Anger namnet på den Elastic pool som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="da20b-151">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="da20b-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da20b-152">-ResourceGroupName</span></span>
<span data-ttu-id="da20b-153">Anger namnet på den resurs grupp som den här cmdleten tilldelar den elastiska poolen till.</span><span class="sxs-lookup"><span data-stu-id="da20b-153">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="da20b-154">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da20b-154">-ServerName</span></span>
<span data-ttu-id="da20b-155">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="da20b-155">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="da20b-156">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="da20b-156">-StorageMB</span></span>
<span data-ttu-id="da20b-157">Anger lagrings gränsen (i MB) för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="da20b-157">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="da20b-158">Om du inte anger den här parametern beräknar den här cmdleten ett värde som är beroende av värdet för *DTU* -parametern.</span><span class="sxs-lookup"><span data-stu-id="da20b-158">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="da20b-159">Se [eDTU-och lagrings gränser](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) för möjliga värden.</span><span class="sxs-lookup"><span data-stu-id="da20b-159">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="da20b-160">-Taggar</span><span class="sxs-lookup"><span data-stu-id="da20b-160">-Tags</span></span>
<span data-ttu-id="da20b-161">Anger en ord lista med par med nyckelord i form av en hash-tabell som denna cmdlet associerar med den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="da20b-161">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="da20b-162">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="da20b-162">For example:</span></span>

<span data-ttu-id="da20b-163">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="da20b-163">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="da20b-164">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da20b-164">-Confirm</span></span>
<span data-ttu-id="da20b-165">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da20b-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da20b-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da20b-166">-WhatIf</span></span>
<span data-ttu-id="da20b-167">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da20b-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da20b-168">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da20b-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da20b-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da20b-169">-DefaultProfile</span></span>
<span data-ttu-id="da20b-170">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da20b-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da20b-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da20b-171">CommonParameters</span></span>
<span data-ttu-id="da20b-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da20b-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da20b-173">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da20b-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da20b-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da20b-174">INPUTS</span></span>

## <span data-ttu-id="da20b-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da20b-175">OUTPUTS</span></span>

### <span data-ttu-id="da20b-176">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="da20b-176">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="da20b-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da20b-177">NOTES</span></span>

## <span data-ttu-id="da20b-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da20b-178">RELATED LINKS</span></span>

[<span data-ttu-id="da20b-179">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="da20b-179">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="da20b-180">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="da20b-180">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="da20b-181">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="da20b-181">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="da20b-182">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="da20b-182">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="da20b-183">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="da20b-183">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="da20b-184">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="da20b-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
