---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092163"
---
# <span data-ttu-id="498fc-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="498fc-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="498fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="498fc-102">SYNOPSIS</span></span>
<span data-ttu-id="498fc-103">Anger samlingen CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="498fc-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="498fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="498fc-104">SYNTAX</span></span>

### <span data-ttu-id="498fc-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="498fc-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498fc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="498fc-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="498fc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="498fc-107">DESCRIPTION</span></span>
<span data-ttu-id="498fc-108">Cmdleten **set-AzCosmosDBMongoDBCollection** anger samlingen CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="498fc-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="498fc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="498fc-109">EXAMPLES</span></span>

### <span data-ttu-id="498fc-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="498fc-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="498fc-111">Resurs objekt innehåller MongoIndexes, _rid _ts _etag egenskaper.</span><span class="sxs-lookup"><span data-stu-id="498fc-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="498fc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="498fc-112">PARAMETERS</span></span>

### <span data-ttu-id="498fc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="498fc-113">-AccountName</span></span>
<span data-ttu-id="498fc-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="498fc-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="498fc-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="498fc-115">-Confirm</span></span>
<span data-ttu-id="498fc-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="498fc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="498fc-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="498fc-117">-DatabaseName</span></span>
<span data-ttu-id="498fc-118">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="498fc-118">Database name.</span></span>

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

### <span data-ttu-id="498fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498fc-119">-DefaultProfile</span></span>
<span data-ttu-id="498fc-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="498fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="498fc-121">-Index</span><span class="sxs-lookup"><span data-stu-id="498fc-121">-Index</span></span>
<span data-ttu-id="498fc-122">Matris med PSMongoIndex-objekt.</span><span class="sxs-lookup"><span data-stu-id="498fc-122">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="498fc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="498fc-123">-InputObject</span></span>
<span data-ttu-id="498fc-124">Mongo.</span><span class="sxs-lookup"><span data-stu-id="498fc-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="498fc-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="498fc-125">-Name</span></span>
<span data-ttu-id="498fc-126">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="498fc-126">Collection name.</span></span>

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

### <span data-ttu-id="498fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="498fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="498fc-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="498fc-128">Name of resource group.</span></span>

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

### <span data-ttu-id="498fc-129">-Shard</span><span class="sxs-lookup"><span data-stu-id="498fc-129">-Shard</span></span>
<span data-ttu-id="498fc-130">Sharding nyckel Sök väg.</span><span class="sxs-lookup"><span data-stu-id="498fc-130">Sharding key path.</span></span>

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

### <span data-ttu-id="498fc-131">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="498fc-131">-Throughput</span></span>
<span data-ttu-id="498fc-132">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="498fc-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="498fc-133">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="498fc-133">Default value is 400.</span></span>

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

### <span data-ttu-id="498fc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="498fc-134">-WhatIf</span></span>
<span data-ttu-id="498fc-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="498fc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="498fc-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="498fc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="498fc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498fc-137">CommonParameters</span></span>
<span data-ttu-id="498fc-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="498fc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498fc-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="498fc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498fc-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="498fc-140">INPUTS</span></span>

### <span data-ttu-id="498fc-141">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="498fc-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="498fc-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="498fc-142">OUTPUTS</span></span>

### <span data-ttu-id="498fc-143">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="498fc-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="498fc-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="498fc-144">NOTES</span></span>

## <span data-ttu-id="498fc-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="498fc-145">RELATED LINKS</span></span>
