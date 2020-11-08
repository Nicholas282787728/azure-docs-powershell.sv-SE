---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092149"
---
# <span data-ttu-id="24043-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="24043-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="24043-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24043-102">SYNOPSIS</span></span>
<span data-ttu-id="24043-103">Uppdaterar genomflödet för en CosmosDB Cassandra-tabell.</span><span class="sxs-lookup"><span data-stu-id="24043-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="24043-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24043-104">SYNTAX</span></span>

### <span data-ttu-id="24043-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="24043-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24043-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24043-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24043-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24043-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24043-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24043-108">EXAMPLES</span></span>

### <span data-ttu-id="24043-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="24043-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="24043-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24043-110">PARAMETERS</span></span>

### <span data-ttu-id="24043-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24043-111">-AccountName</span></span>
<span data-ttu-id="24043-112">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="24043-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24043-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24043-113">-Confirm</span></span>
<span data-ttu-id="24043-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24043-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24043-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24043-115">-DefaultProfile</span></span>
<span data-ttu-id="24043-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24043-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24043-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24043-117">-InputObject</span></span>
<span data-ttu-id="24043-118">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="24043-118">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24043-119">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="24043-119">-KeyspaceName</span></span>
<span data-ttu-id="24043-120">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="24043-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="24043-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="24043-121">-Name</span></span>
<span data-ttu-id="24043-122">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="24043-122">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="24043-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="24043-123">-ParentObject</span></span>
<span data-ttu-id="24043-124">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="24043-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="24043-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24043-125">-ResourceGroupName</span></span>
<span data-ttu-id="24043-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="24043-126">Name of resource group.</span></span>

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

### <span data-ttu-id="24043-127">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="24043-127">-Throughput</span></span>
<span data-ttu-id="24043-128">Genomflödet av Cassandra-tecken (RU/s).</span><span class="sxs-lookup"><span data-stu-id="24043-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="24043-129">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="24043-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24043-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24043-130">-WhatIf</span></span>
<span data-ttu-id="24043-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24043-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24043-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24043-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24043-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24043-133">CommonParameters</span></span>
<span data-ttu-id="24043-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24043-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24043-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24043-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24043-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24043-136">INPUTS</span></span>

### <span data-ttu-id="24043-137">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="24043-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="24043-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24043-138">OUTPUTS</span></span>

### <span data-ttu-id="24043-139">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="24043-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="24043-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24043-140">NOTES</span></span>

## <span data-ttu-id="24043-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24043-141">RELATED LINKS</span></span>
