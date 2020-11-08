---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262803"
---
# <span data-ttu-id="8d09d-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="8d09d-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="8d09d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d09d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d09d-103">Uppdaterar CosmosDB Gremlin-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="8d09d-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="8d09d-104">Utför en klient uppdaterings åtgärd genom att läsa det befintliga diagrammet.</span><span class="sxs-lookup"><span data-stu-id="8d09d-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="8d09d-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d09d-105">SYNTAX</span></span>

### <span data-ttu-id="8d09d-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8d09d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d09d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d09d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d09d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d09d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d09d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d09d-109">DESCRIPTION</span></span>
<span data-ttu-id="8d09d-110">Uppdaterar CosmosDB Gremlin-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="8d09d-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="8d09d-111">Utför en klient uppdaterings åtgärd genom att läsa det befintliga diagrammet.</span><span class="sxs-lookup"><span data-stu-id="8d09d-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="8d09d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d09d-112">EXAMPLES</span></span>

### <span data-ttu-id="8d09d-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8d09d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="8d09d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d09d-114">PARAMETERS</span></span>

### <span data-ttu-id="8d09d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d09d-115">-AccountName</span></span>
<span data-ttu-id="8d09d-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="8d09d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8d09d-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8d09d-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8d09d-118">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="8d09d-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8d09d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d09d-119">-Confirm</span></span>
<span data-ttu-id="8d09d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d09d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d09d-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d09d-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="8d09d-122">ConflictResolutionPolicy-objekt av typen PSConflictResolutionPolicy om det här är angivet som ConflictResolutionPolicy för behållaren.</span><span class="sxs-lookup"><span data-stu-id="8d09d-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="8d09d-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="8d09d-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="8d09d-124">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="8d09d-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="8d09d-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="8d09d-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="8d09d-126">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="8d09d-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="8d09d-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="8d09d-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="8d09d-128">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="8d09d-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="8d09d-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d09d-129">-DatabaseName</span></span>
<span data-ttu-id="8d09d-130">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="8d09d-130">Database name.</span></span>

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

### <span data-ttu-id="8d09d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d09d-131">-DefaultProfile</span></span>
<span data-ttu-id="8d09d-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d09d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d09d-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="8d09d-133">-IndexingPolicy</span></span>
<span data-ttu-id="8d09d-134">Indexerings princip objekt av typen Microsoft. Azure. commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d09d-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="8d09d-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d09d-135">-InputObject</span></span>
<span data-ttu-id="8d09d-136">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8d09d-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d09d-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d09d-137">-Name</span></span>
<span data-ttu-id="8d09d-138">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="8d09d-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="8d09d-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8d09d-139">-ParentObject</span></span>
<span data-ttu-id="8d09d-140">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8d09d-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="8d09d-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="8d09d-141">-PartitionKeyKind</span></span>
<span data-ttu-id="8d09d-142">Den typ av algoritm som används för att partitionera.</span><span class="sxs-lookup"><span data-stu-id="8d09d-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="8d09d-143">Möjliga värden är: ' hash ', ' område '</span><span class="sxs-lookup"><span data-stu-id="8d09d-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="8d09d-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="8d09d-144">-PartitionKeyPath</span></span>
<span data-ttu-id="8d09d-145">Sökväg till partitionsnyckel, till exempel "/Address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="8d09d-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d09d-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="8d09d-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="8d09d-147">Versionen av partitionsnyckel-definitionen</span><span class="sxs-lookup"><span data-stu-id="8d09d-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="8d09d-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d09d-148">-ResourceGroupName</span></span>
<span data-ttu-id="8d09d-149">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8d09d-149">Name of resource group.</span></span>

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

### <span data-ttu-id="8d09d-150">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="8d09d-150">-Throughput</span></span>
<span data-ttu-id="8d09d-151">Genomflödet i Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8d09d-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="8d09d-152">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="8d09d-152">Default value is 400.</span></span>

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

### <span data-ttu-id="8d09d-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="8d09d-153">-TtlInSeconds</span></span>
<span data-ttu-id="8d09d-154">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="8d09d-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="8d09d-155">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="8d09d-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="8d09d-156">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="8d09d-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="8d09d-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="8d09d-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="8d09d-158">UniqueKeyPolicy-objekt av typen Microsoft. Azure. commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d09d-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="8d09d-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d09d-159">-WhatIf</span></span>
<span data-ttu-id="8d09d-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d09d-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d09d-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d09d-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d09d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d09d-162">CommonParameters</span></span>
<span data-ttu-id="8d09d-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d09d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d09d-164">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d09d-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d09d-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d09d-165">INPUTS</span></span>

### <span data-ttu-id="8d09d-166">Microsoft. Azure. commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="8d09d-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="8d09d-167">Microsoft. Azure. commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="8d09d-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="8d09d-168">Microsoft. Azure. commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d09d-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="8d09d-169">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8d09d-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="8d09d-170">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="8d09d-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="8d09d-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d09d-171">OUTPUTS</span></span>

### <span data-ttu-id="8d09d-172">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="8d09d-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="8d09d-173">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8d09d-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="8d09d-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d09d-174">NOTES</span></span>

## <span data-ttu-id="8d09d-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d09d-175">RELATED LINKS</span></span>
