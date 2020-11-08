---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: ca78194e0e47b07d2d0d061829bf4db38d85632a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091853"
---
# <span data-ttu-id="0e5ec-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="0e5ec-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="0e5ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5ec-103">Hämtar en CosmosDB Cassandra-tabell.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="0e5ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e5ec-104">SYNTAX</span></span>

### <span data-ttu-id="0e5ec-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0e5ec-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e5ec-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e5ec-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e5ec-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e5ec-107">DESCRIPTION</span></span>
<span data-ttu-id="0e5ec-108">Cmdleten **Get-AzCosmosDBCassandraTable** skapar ett nytt eller uppdaterar ett befintligt CosmosDB-Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0e5ec-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e5ec-109">EXAMPLES</span></span>

### <span data-ttu-id="0e5ec-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e5ec-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="0e5ec-111">{{Get-AzCosmosDBCassandraTable får egenskaperna för en befintlig CassandraKeyspace.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="0e5ec-112">Du kan expandera resursen för att hämta DefaultTtl, schema, _etag, _ts _rid egenskaper.}}</span><span class="sxs-lookup"><span data-stu-id="0e5ec-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="0e5ec-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e5ec-113">PARAMETERS</span></span>

### <span data-ttu-id="0e5ec-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0e5ec-114">-AccountName</span></span>
<span data-ttu-id="0e5ec-115">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0e5ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5ec-116">-DefaultProfile</span></span>
<span data-ttu-id="0e5ec-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e5ec-118">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="0e5ec-118">-Detailed</span></span>
<span data-ttu-id="0e5ec-119">Om den anges returnerar cmdleten Cassandra-tabellen med motsvarande genomflöde-värde.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-119">If provided then, the cmdlet returns the Cassandra Table with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="0e5ec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e5ec-120">-InputObject</span></span>
<span data-ttu-id="0e5ec-121">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-121">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="0e5ec-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="0e5ec-122">-KeyspaceName</span></span>
<span data-ttu-id="0e5ec-123">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0e5ec-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e5ec-124">-Name</span></span>
<span data-ttu-id="0e5ec-125">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="0e5ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e5ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="0e5ec-127">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-127">Name of resource group.</span></span>

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

### <span data-ttu-id="0e5ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5ec-128">CommonParameters</span></span>
<span data-ttu-id="0e5ec-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e5ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5ec-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e5ec-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5ec-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e5ec-131">INPUTS</span></span>

### <span data-ttu-id="0e5ec-132">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0e5ec-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="0e5ec-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e5ec-133">OUTPUTS</span></span>

### <span data-ttu-id="0e5ec-134">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="0e5ec-134">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="0e5ec-135">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0e5ec-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0e5ec-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e5ec-136">NOTES</span></span>

## <span data-ttu-id="0e5ec-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e5ec-137">RELATED LINKS</span></span>
