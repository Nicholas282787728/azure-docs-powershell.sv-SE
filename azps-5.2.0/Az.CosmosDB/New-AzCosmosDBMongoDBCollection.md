---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401979"
---
# <span data-ttu-id="02f5d-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="02f5d-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="02f5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="02f5d-103">Skapar en ny CosmosDB MongoDB-samling.</span><span class="sxs-lookup"><span data-stu-id="02f5d-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="02f5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02f5d-104">SYNTAX</span></span>

### <span data-ttu-id="02f5d-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="02f5d-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02f5d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02f5d-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02f5d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02f5d-107">DESCRIPTION</span></span>
<span data-ttu-id="02f5d-108">Skapar en ny CosmosDB MongoDB-samling.</span><span class="sxs-lookup"><span data-stu-id="02f5d-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="02f5d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02f5d-109">EXAMPLES</span></span>

### <span data-ttu-id="02f5d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="02f5d-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="02f5d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02f5d-111">PARAMETERS</span></span>

### <span data-ttu-id="02f5d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02f5d-112">-AccountName</span></span>
<span data-ttu-id="02f5d-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="02f5d-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="02f5d-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="02f5d-115">TTL för analytisk lagring.</span><span class="sxs-lookup"><span data-stu-id="02f5d-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="02f5d-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="02f5d-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="02f5d-117">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="02f5d-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="02f5d-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02f5d-118">-Confirm</span></span>
<span data-ttu-id="02f5d-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02f5d-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02f5d-120">-DatabaseName</span></span>
<span data-ttu-id="02f5d-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="02f5d-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f5d-122">-DefaultProfile</span></span>
<span data-ttu-id="02f5d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02f5d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-124">-Index</span><span class="sxs-lookup"><span data-stu-id="02f5d-124">-Index</span></span>
<span data-ttu-id="02f5d-125">Matris med PSMongoIndex-objekt.</span><span class="sxs-lookup"><span data-stu-id="02f5d-125">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="02f5d-126">-Name</span></span>
<span data-ttu-id="02f5d-127">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="02f5d-127">Collection name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02f5d-128">-ParentObject</span></span>
<span data-ttu-id="02f5d-129">Mongo.</span><span class="sxs-lookup"><span data-stu-id="02f5d-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f5d-130">-ResourceGroupName</span></span>
<span data-ttu-id="02f5d-131">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="02f5d-131">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="02f5d-132">-Shard</span></span>
<span data-ttu-id="02f5d-133">Sharding nyckel Sök väg.</span><span class="sxs-lookup"><span data-stu-id="02f5d-133">Sharding key path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-134">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="02f5d-134">-Throughput</span></span>
<span data-ttu-id="02f5d-135">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="02f5d-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="02f5d-136">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="02f5d-136">Default value is 400.</span></span>

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

### <span data-ttu-id="02f5d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f5d-137">-WhatIf</span></span>
<span data-ttu-id="02f5d-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02f5d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02f5d-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02f5d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f5d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f5d-140">CommonParameters</span></span>
<span data-ttu-id="02f5d-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f5d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f5d-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02f5d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f5d-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02f5d-143">INPUTS</span></span>

### <span data-ttu-id="02f5d-144">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="02f5d-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="02f5d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02f5d-145">OUTPUTS</span></span>

### <span data-ttu-id="02f5d-146">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="02f5d-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="02f5d-147">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="02f5d-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="02f5d-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02f5d-148">NOTES</span></span>

## <span data-ttu-id="02f5d-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02f5d-149">RELATED LINKS</span></span>
