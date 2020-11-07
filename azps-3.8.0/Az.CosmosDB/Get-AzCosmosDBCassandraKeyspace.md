---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926221"
---
# <span data-ttu-id="d9ab4-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="d9ab4-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="d9ab4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ab4-103">Hämtar ett CosmosDB Cassandra-tecken.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d9ab4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9ab4-104">SYNTAX</span></span>

### <span data-ttu-id="d9ab4-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d9ab4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9ab4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9ab4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9ab4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9ab4-107">DESCRIPTION</span></span>
<span data-ttu-id="d9ab4-108">Cmdleten **Get-AzCosmosDBCassandraKeyspace** skapar ett nytt eller uppdaterar ett befintligt CosmosDB-Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d9ab4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9ab4-109">EXAMPLES</span></span>

### <span data-ttu-id="d9ab4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d9ab4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="d9ab4-111">Get-AzCosmosDBCassandraKeyspace får egenskaperna för en befintlig CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="d9ab4-112">Du kan expandera resursen för att få _etag _ts _rid egenskaper.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="d9ab4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9ab4-113">PARAMETERS</span></span>

### <span data-ttu-id="d9ab4-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d9ab4-114">-AccountName</span></span>
<span data-ttu-id="d9ab4-115">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d9ab4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ab4-116">-DefaultProfile</span></span>
<span data-ttu-id="d9ab4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9ab4-118">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="d9ab4-118">-Detailed</span></span>
<span data-ttu-id="d9ab4-119">Om den anges returnerar cmdleten det tecken som har motsvarande genomflöde.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="d9ab4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9ab4-120">-InputObject</span></span>
<span data-ttu-id="d9ab4-121">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d9ab4-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ab4-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9ab4-122">-Name</span></span>
<span data-ttu-id="d9ab4-123">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d9ab4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ab4-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9ab4-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-125">Name of resource group.</span></span>

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

### <span data-ttu-id="d9ab4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ab4-126">CommonParameters</span></span>
<span data-ttu-id="d9ab4-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ab4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ab4-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9ab4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ab4-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9ab4-129">INPUTS</span></span>

### <span data-ttu-id="d9ab4-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d9ab4-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d9ab4-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9ab4-131">OUTPUTS</span></span>

### <span data-ttu-id="d9ab4-132">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="d9ab4-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="d9ab4-133">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d9ab4-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d9ab4-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9ab4-134">NOTES</span></span>

## <span data-ttu-id="d9ab4-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9ab4-135">RELATED LINKS</span></span>
