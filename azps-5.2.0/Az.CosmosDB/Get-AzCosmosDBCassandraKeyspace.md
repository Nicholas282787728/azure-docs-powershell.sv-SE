---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396435"
---
# <span data-ttu-id="67c4d-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="67c4d-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="67c4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="67c4d-103">Hämtar ett CosmosDB Cassandra-tecken.</span><span class="sxs-lookup"><span data-stu-id="67c4d-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="67c4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67c4d-104">SYNTAX</span></span>

### <span data-ttu-id="67c4d-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="67c4d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67c4d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67c4d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67c4d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67c4d-107">DESCRIPTION</span></span>
<span data-ttu-id="67c4d-108">Cmdleten **Get-AzCosmosDBCassandraKeyspace** skapar ett nytt eller uppdaterar ett befintligt CosmosDB-Cassandra.</span><span class="sxs-lookup"><span data-stu-id="67c4d-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="67c4d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67c4d-109">EXAMPLES</span></span>

### <span data-ttu-id="67c4d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="67c4d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="67c4d-111">Get-AzCosmosDBCassandraKeyspace får egenskaperna för en befintlig CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="67c4d-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="67c4d-112">Du kan expandera resursen för att få _etag _ts _rid egenskaper.</span><span class="sxs-lookup"><span data-stu-id="67c4d-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="67c4d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67c4d-113">PARAMETERS</span></span>

### <span data-ttu-id="67c4d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67c4d-114">-AccountName</span></span>
<span data-ttu-id="67c4d-115">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="67c4d-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="67c4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c4d-116">-DefaultProfile</span></span>
<span data-ttu-id="67c4d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67c4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67c4d-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="67c4d-118">-Name</span></span>
<span data-ttu-id="67c4d-119">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="67c4d-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="67c4d-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="67c4d-120">-ParentObject</span></span>
<span data-ttu-id="67c4d-121">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="67c4d-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67c4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="67c4d-123">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="67c4d-123">Name of resource group.</span></span>

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

### <span data-ttu-id="67c4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c4d-124">CommonParameters</span></span>
<span data-ttu-id="67c4d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67c4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c4d-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67c4d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c4d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67c4d-127">INPUTS</span></span>

### <span data-ttu-id="67c4d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="67c4d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="67c4d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67c4d-129">OUTPUTS</span></span>

### <span data-ttu-id="67c4d-130">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="67c4d-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="67c4d-131">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="67c4d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="67c4d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67c4d-132">NOTES</span></span>

## <span data-ttu-id="67c4d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67c4d-133">RELATED LINKS</span></span>
