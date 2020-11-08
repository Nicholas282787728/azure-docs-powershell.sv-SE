---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092164"
---
# <span data-ttu-id="40b1f-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="40b1f-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="40b1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="40b1f-103">Anger diagrammet CosmosDB-Gremlin.</span><span class="sxs-lookup"><span data-stu-id="40b1f-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="40b1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40b1f-104">SYNTAX</span></span>

### <span data-ttu-id="40b1f-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="40b1f-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b1f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40b1f-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b1f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40b1f-107">DESCRIPTION</span></span>
<span data-ttu-id="40b1f-108">Cmdleten **set-AzCosmosDBGremlinGraph** anger ett CosmosDB-Gremlin-diagram.</span><span class="sxs-lookup"><span data-stu-id="40b1f-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="40b1f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40b1f-109">EXAMPLES</span></span>

### <span data-ttu-id="40b1f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40b1f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="40b1f-111">Resource-objekt innehåller IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="40b1f-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="40b1f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40b1f-112">PARAMETERS</span></span>

### <span data-ttu-id="40b1f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40b1f-113">-AccountName</span></span>
<span data-ttu-id="40b1f-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="40b1f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40b1f-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40b1f-115">-Confirm</span></span>
<span data-ttu-id="40b1f-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40b1f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b1f-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="40b1f-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="40b1f-118">ConflictResolutionPolicy-objekt av typen PSConflictResolutionPolicy om det här är angivet som ConflictResolutionPolicy för behållaren.</span><span class="sxs-lookup"><span data-stu-id="40b1f-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40b1f-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="40b1f-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="40b1f-120">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="40b1f-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="40b1f-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="40b1f-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="40b1f-122">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="40b1f-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="40b1f-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="40b1f-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="40b1f-124">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="40b1f-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="40b1f-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40b1f-125">-DatabaseName</span></span>
<span data-ttu-id="40b1f-126">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="40b1f-126">Database name.</span></span>

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

### <span data-ttu-id="40b1f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b1f-127">-DefaultProfile</span></span>
<span data-ttu-id="40b1f-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40b1f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b1f-129">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="40b1f-129">-IndexingPolicy</span></span>
<span data-ttu-id="40b1f-130">Indexerings princip objekt av typen Microsoft. Azure. commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="40b1f-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40b1f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40b1f-131">-InputObject</span></span>
<span data-ttu-id="40b1f-132">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="40b1f-132">Gremlin Database object.</span></span>

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

### <span data-ttu-id="40b1f-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="40b1f-133">-Name</span></span>
<span data-ttu-id="40b1f-134">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="40b1f-134">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="40b1f-135">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="40b1f-135">-PartitionKeyKind</span></span>
<span data-ttu-id="40b1f-136">Den typ av algoritm som används för att partitionera.</span><span class="sxs-lookup"><span data-stu-id="40b1f-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="40b1f-137">Möjliga värden är: ' hash ', ' område '</span><span class="sxs-lookup"><span data-stu-id="40b1f-137">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="40b1f-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="40b1f-138">-PartitionKeyPath</span></span>
<span data-ttu-id="40b1f-139">Sökväg till partitionsnyckel, till exempel "/Address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="40b1f-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b1f-140">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="40b1f-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="40b1f-141">Versionen av partitionsnyckel-definitionen</span><span class="sxs-lookup"><span data-stu-id="40b1f-141">The version of the partition key definition</span></span>

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

### <span data-ttu-id="40b1f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b1f-142">-ResourceGroupName</span></span>
<span data-ttu-id="40b1f-143">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="40b1f-143">Name of resource group.</span></span>

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

### <span data-ttu-id="40b1f-144">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="40b1f-144">-Throughput</span></span>
<span data-ttu-id="40b1f-145">Genomflödet i Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="40b1f-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="40b1f-146">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="40b1f-146">Default value is 400.</span></span>

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

### <span data-ttu-id="40b1f-147">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="40b1f-147">-TtlInSeconds</span></span>
<span data-ttu-id="40b1f-148">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="40b1f-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="40b1f-149">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="40b1f-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="40b1f-150">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="40b1f-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="40b1f-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="40b1f-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="40b1f-152">UniqueKeyPolicy-objekt av typen Microsoft. Azure. commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="40b1f-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40b1f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b1f-153">-WhatIf</span></span>
<span data-ttu-id="40b1f-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40b1f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b1f-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40b1f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b1f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b1f-156">CommonParameters</span></span>
<span data-ttu-id="40b1f-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b1f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b1f-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40b1f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b1f-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40b1f-159">INPUTS</span></span>

### <span data-ttu-id="40b1f-160">Microsoft. Azure. commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="40b1f-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="40b1f-161">Microsoft. Azure. commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="40b1f-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="40b1f-162">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="40b1f-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="40b1f-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40b1f-163">OUTPUTS</span></span>

### <span data-ttu-id="40b1f-164">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="40b1f-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="40b1f-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40b1f-165">NOTES</span></span>

## <span data-ttu-id="40b1f-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40b1f-166">RELATED LINKS</span></span>
