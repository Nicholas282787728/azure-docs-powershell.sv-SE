---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091848"
---
# <span data-ttu-id="b0822-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="b0822-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="b0822-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0822-102">SYNOPSIS</span></span>
<span data-ttu-id="b0822-103">Hämtar diagrammet CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b0822-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b0822-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0822-104">SYNTAX</span></span>

### <span data-ttu-id="b0822-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b0822-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="b0822-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0822-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0822-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0822-107">DESCRIPTION</span></span>
<span data-ttu-id="b0822-108">Cmdleten **Get-AzCosmosDBGremlinGraph** hämtar diagram egenskaperna för CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b0822-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="b0822-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0822-109">EXAMPLES</span></span>

### <span data-ttu-id="b0822-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b0822-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="b0822-111">Resource-objekt innehåller IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="b0822-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="b0822-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0822-112">PARAMETERS</span></span>

### <span data-ttu-id="b0822-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0822-113">-AccountName</span></span>
<span data-ttu-id="b0822-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="b0822-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b0822-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0822-115">-DatabaseName</span></span>
<span data-ttu-id="b0822-116">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="b0822-116">Database name.</span></span>

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

### <span data-ttu-id="b0822-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0822-117">-DefaultProfile</span></span>
<span data-ttu-id="b0822-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0822-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0822-119">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="b0822-119">-Detailed</span></span>
<span data-ttu-id="b0822-120">Om den anges returnerar cmdleten Gremlin-diagrammet med motsvarande genomflöde-värde.</span><span class="sxs-lookup"><span data-stu-id="b0822-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="b0822-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0822-121">-InputObject</span></span>
<span data-ttu-id="b0822-122">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b0822-122">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0822-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0822-123">-Name</span></span>
<span data-ttu-id="b0822-124">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="b0822-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b0822-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0822-125">-ResourceGroupName</span></span>
<span data-ttu-id="b0822-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b0822-126">Name of resource group.</span></span>

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

### <span data-ttu-id="b0822-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0822-127">CommonParameters</span></span>
<span data-ttu-id="b0822-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0822-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0822-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0822-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0822-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0822-130">INPUTS</span></span>

### <span data-ttu-id="b0822-131">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b0822-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b0822-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0822-132">OUTPUTS</span></span>

### <span data-ttu-id="b0822-133">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b0822-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="b0822-134">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b0822-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b0822-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0822-135">NOTES</span></span>

## <span data-ttu-id="b0822-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0822-136">RELATED LINKS</span></span>
