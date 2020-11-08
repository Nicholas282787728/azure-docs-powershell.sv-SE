---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: d1b0dcee6c4337a572f98a51cb03c3fcdcd6c84e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092166"
---
# <span data-ttu-id="1c4f5-101">Set-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="1c4f5-101">Set-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="1c4f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c4f5-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4f5-103">Anger CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-103">Sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1c4f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c4f5-104">SYNTAX</span></span>

### <span data-ttu-id="1c4f5-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1c4f5-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c4f5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c4f5-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c4f5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c4f5-107">DESCRIPTION</span></span>
<span data-ttu-id="1c4f5-108">Cmdleten **set-AzCosmosDBCassandraKeyspace** anger CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-108">The **Set-AzCosmosDBCassandraKeyspace** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1c4f5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c4f5-109">EXAMPLES</span></span>

### <span data-ttu-id="1c4f5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1c4f5-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraKeyspace -ResourceGroupName {rgName} -AccountName {accountName} -Name {keyspaceName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

<span data-ttu-id="1c4f5-111">Resurs objekt innehåller värdena för _rid _ts _etag egenskaper.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-111">Resource object contains the values of the _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="1c4f5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c4f5-112">PARAMETERS</span></span>

### <span data-ttu-id="1c4f5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1c4f5-113">-AccountName</span></span>
<span data-ttu-id="1c4f5-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1c4f5-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c4f5-115">-Confirm</span></span>
<span data-ttu-id="1c4f5-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c4f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4f5-117">-DefaultProfile</span></span>
<span data-ttu-id="1c4f5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c4f5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c4f5-119">-InputObject</span></span>
<span data-ttu-id="1c4f5-120">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1c4f5-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1c4f5-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c4f5-121">-Name</span></span>
<span data-ttu-id="1c4f5-122">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1c4f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c4f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c4f5-124">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-124">Name of resource group.</span></span>

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

### <span data-ttu-id="1c4f5-125">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="1c4f5-125">-Throughput</span></span>
<span data-ttu-id="1c4f5-126">Genomflödet av Cassandra-tecken (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1c4f5-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="1c4f5-127">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-127">Default value is 400.</span></span>

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

### <span data-ttu-id="1c4f5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c4f5-128">-WhatIf</span></span>
<span data-ttu-id="1c4f5-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c4f5-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c4f5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4f5-131">CommonParameters</span></span>
<span data-ttu-id="1c4f5-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c4f5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4f5-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c4f5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4f5-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c4f5-134">INPUTS</span></span>

### <span data-ttu-id="1c4f5-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1c4f5-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1c4f5-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c4f5-136">OUTPUTS</span></span>

### <span data-ttu-id="1c4f5-137">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="1c4f5-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="1c4f5-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c4f5-138">NOTES</span></span>

## <span data-ttu-id="1c4f5-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c4f5-139">RELATED LINKS</span></span>
