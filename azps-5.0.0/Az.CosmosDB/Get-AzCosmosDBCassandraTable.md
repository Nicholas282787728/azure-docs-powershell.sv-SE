---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321712"
---
# <span data-ttu-id="0efe8-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="0efe8-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="0efe8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0efe8-102">SYNOPSIS</span></span>
<span data-ttu-id="0efe8-103">Hämtar en CosmosDB Cassandra-tabell.</span><span class="sxs-lookup"><span data-stu-id="0efe8-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="0efe8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0efe8-104">SYNTAX</span></span>

### <span data-ttu-id="0efe8-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0efe8-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0efe8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0efe8-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0efe8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0efe8-107">DESCRIPTION</span></span>
<span data-ttu-id="0efe8-108">Cmdleten **Get-AzCosmosDBCassandraTable** skapar ett nytt eller uppdaterar ett befintligt CosmosDB-Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0efe8-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0efe8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0efe8-109">EXAMPLES</span></span>

### <span data-ttu-id="0efe8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0efe8-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="0efe8-111">{{Get-AzCosmosDBCassandraTable får egenskaperna för en befintlig CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="0efe8-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="0efe8-112">Du kan expandera resursen för att hämta DefaultTtl, schema, _etag, _ts _rid egenskaper.}}</span><span class="sxs-lookup"><span data-stu-id="0efe8-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="0efe8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0efe8-113">PARAMETERS</span></span>

### <span data-ttu-id="0efe8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0efe8-114">-AccountName</span></span>
<span data-ttu-id="0efe8-115">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="0efe8-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0efe8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efe8-116">-DefaultProfile</span></span>
<span data-ttu-id="0efe8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0efe8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0efe8-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="0efe8-118">-KeyspaceName</span></span>
<span data-ttu-id="0efe8-119">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="0efe8-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0efe8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0efe8-120">-Name</span></span>
<span data-ttu-id="0efe8-121">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="0efe8-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="0efe8-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0efe8-122">-ParentObject</span></span>
<span data-ttu-id="0efe8-123">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="0efe8-123">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0efe8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efe8-124">-ResourceGroupName</span></span>
<span data-ttu-id="0efe8-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0efe8-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0efe8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efe8-126">CommonParameters</span></span>
<span data-ttu-id="0efe8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efe8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efe8-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0efe8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efe8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0efe8-129">INPUTS</span></span>

### <span data-ttu-id="0efe8-130">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0efe8-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="0efe8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0efe8-131">OUTPUTS</span></span>

### <span data-ttu-id="0efe8-132">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="0efe8-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="0efe8-133">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0efe8-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0efe8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0efe8-134">NOTES</span></span>

## <span data-ttu-id="0efe8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0efe8-135">RELATED LINKS</span></span>