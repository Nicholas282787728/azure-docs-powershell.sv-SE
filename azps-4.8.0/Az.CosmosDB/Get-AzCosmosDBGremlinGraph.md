---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261931"
---
# <span data-ttu-id="52673-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="52673-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="52673-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52673-102">SYNOPSIS</span></span>
<span data-ttu-id="52673-103">Hämtar diagrammet CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="52673-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="52673-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52673-104">SYNTAX</span></span>

### <span data-ttu-id="52673-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="52673-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="52673-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52673-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52673-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52673-107">DESCRIPTION</span></span>
<span data-ttu-id="52673-108">Cmdleten **Get-AzCosmosDBGremlinGraph** hämtar diagram egenskaperna för CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="52673-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="52673-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52673-109">EXAMPLES</span></span>

### <span data-ttu-id="52673-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52673-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="52673-111">Resource-objekt innehåller IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="52673-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="52673-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52673-112">PARAMETERS</span></span>

### <span data-ttu-id="52673-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52673-113">-AccountName</span></span>
<span data-ttu-id="52673-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="52673-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="52673-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52673-115">-DatabaseName</span></span>
<span data-ttu-id="52673-116">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="52673-116">Database name.</span></span>

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

### <span data-ttu-id="52673-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52673-117">-DefaultProfile</span></span>
<span data-ttu-id="52673-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52673-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52673-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="52673-119">-Name</span></span>
<span data-ttu-id="52673-120">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="52673-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="52673-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="52673-121">-ParentObject</span></span>
<span data-ttu-id="52673-122">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="52673-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="52673-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52673-123">-ResourceGroupName</span></span>
<span data-ttu-id="52673-124">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="52673-124">Name of resource group.</span></span>

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

### <span data-ttu-id="52673-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52673-125">CommonParameters</span></span>
<span data-ttu-id="52673-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52673-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52673-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52673-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52673-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52673-128">INPUTS</span></span>

### <span data-ttu-id="52673-129">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="52673-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="52673-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52673-130">OUTPUTS</span></span>

### <span data-ttu-id="52673-131">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="52673-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="52673-132">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="52673-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="52673-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52673-133">NOTES</span></span>

## <span data-ttu-id="52673-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52673-134">RELATED LINKS</span></span>