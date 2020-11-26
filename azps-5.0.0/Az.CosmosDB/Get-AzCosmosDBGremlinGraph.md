---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321700"
---
# <span data-ttu-id="b42f6-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="b42f6-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="b42f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b42f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b42f6-103">Hämtar diagrammet CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b42f6-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b42f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b42f6-104">SYNTAX</span></span>

### <span data-ttu-id="b42f6-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b42f6-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="b42f6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b42f6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b42f6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b42f6-107">DESCRIPTION</span></span>
<span data-ttu-id="b42f6-108">Cmdleten **Get-AzCosmosDBGremlinGraph** hämtar diagram egenskaperna för CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b42f6-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="b42f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b42f6-109">EXAMPLES</span></span>

### <span data-ttu-id="b42f6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b42f6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="b42f6-111">Resource-objekt innehåller IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="b42f6-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="b42f6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b42f6-112">PARAMETERS</span></span>

### <span data-ttu-id="b42f6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b42f6-113">-AccountName</span></span>
<span data-ttu-id="b42f6-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="b42f6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b42f6-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b42f6-115">-DatabaseName</span></span>
<span data-ttu-id="b42f6-116">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="b42f6-116">Database name.</span></span>

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

### <span data-ttu-id="b42f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b42f6-117">-DefaultProfile</span></span>
<span data-ttu-id="b42f6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b42f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b42f6-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b42f6-119">-Name</span></span>
<span data-ttu-id="b42f6-120">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="b42f6-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b42f6-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b42f6-121">-ParentObject</span></span>
<span data-ttu-id="b42f6-122">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b42f6-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="b42f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b42f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="b42f6-124">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b42f6-124">Name of resource group.</span></span>

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

### <span data-ttu-id="b42f6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b42f6-125">CommonParameters</span></span>
<span data-ttu-id="b42f6-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b42f6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b42f6-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b42f6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b42f6-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b42f6-128">INPUTS</span></span>

### <span data-ttu-id="b42f6-129">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b42f6-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b42f6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b42f6-130">OUTPUTS</span></span>

### <span data-ttu-id="b42f6-131">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b42f6-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="b42f6-132">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b42f6-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b42f6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b42f6-133">NOTES</span></span>

## <span data-ttu-id="b42f6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b42f6-134">RELATED LINKS</span></span>