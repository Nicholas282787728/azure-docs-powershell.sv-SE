---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390756"
---
# <span data-ttu-id="81f20-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="81f20-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="81f20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81f20-102">SYNOPSIS</span></span>
<span data-ttu-id="81f20-103">Uppdaterar CosmosDB Gremlin-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="81f20-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="81f20-104">Utför en klient uppdaterings åtgärd genom att läsa det befintliga diagrammet.</span><span class="sxs-lookup"><span data-stu-id="81f20-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="81f20-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81f20-105">SYNTAX</span></span>

### <span data-ttu-id="81f20-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="81f20-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81f20-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81f20-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81f20-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81f20-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81f20-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81f20-109">DESCRIPTION</span></span>
<span data-ttu-id="81f20-110">Uppdaterar CosmosDB Gremlin-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="81f20-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="81f20-111">Utför en klient uppdaterings åtgärd genom att läsa det befintliga diagrammet.</span><span class="sxs-lookup"><span data-stu-id="81f20-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="81f20-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81f20-112">EXAMPLES</span></span>

### <span data-ttu-id="81f20-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="81f20-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="81f20-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81f20-114">PARAMETERS</span></span>

### <span data-ttu-id="81f20-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="81f20-115">-AccountName</span></span>
<span data-ttu-id="81f20-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="81f20-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="81f20-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="81f20-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="81f20-118">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="81f20-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="81f20-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81f20-119">-Confirm</span></span>
<span data-ttu-id="81f20-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81f20-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81f20-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="81f20-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="81f20-122">ConflictResolutionPolicy-objekt av typen PSConflictResolutionPolicy om det här är angivet som ConflictResolutionPolicy för behållaren.</span><span class="sxs-lookup"><span data-stu-id="81f20-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="81f20-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="81f20-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="81f20-124">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="81f20-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="81f20-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="81f20-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="81f20-126">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="81f20-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="81f20-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="81f20-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="81f20-128">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="81f20-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="81f20-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81f20-129">-DatabaseName</span></span>
<span data-ttu-id="81f20-130">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="81f20-130">Database name.</span></span>

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

### <span data-ttu-id="81f20-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f20-131">-DefaultProfile</span></span>
<span data-ttu-id="81f20-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81f20-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81f20-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="81f20-133">-IndexingPolicy</span></span>
<span data-ttu-id="81f20-134">Indexerings princip objekt av typen Microsoft. Azure. commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="81f20-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="81f20-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81f20-135">-InputObject</span></span>
<span data-ttu-id="81f20-136">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="81f20-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="81f20-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="81f20-137">-Name</span></span>
<span data-ttu-id="81f20-138">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="81f20-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="81f20-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="81f20-139">-ParentObject</span></span>
<span data-ttu-id="81f20-140">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="81f20-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="81f20-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="81f20-141">-PartitionKeyKind</span></span>
<span data-ttu-id="81f20-142">Den typ av algoritm som används för att partitionera.</span><span class="sxs-lookup"><span data-stu-id="81f20-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="81f20-143">Möjliga värden är: ' hash ', ' område '</span><span class="sxs-lookup"><span data-stu-id="81f20-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="81f20-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="81f20-144">-PartitionKeyPath</span></span>
<span data-ttu-id="81f20-145">Sökväg till partitionsnyckel, till exempel "/Address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="81f20-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="81f20-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="81f20-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="81f20-147">Versionen av partitionsnyckel-definitionen</span><span class="sxs-lookup"><span data-stu-id="81f20-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="81f20-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81f20-148">-ResourceGroupName</span></span>
<span data-ttu-id="81f20-149">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="81f20-149">Name of resource group.</span></span>

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

### <span data-ttu-id="81f20-150">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="81f20-150">-Throughput</span></span>
<span data-ttu-id="81f20-151">Genomflödet i Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="81f20-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="81f20-152">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="81f20-152">Default value is 400.</span></span>

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

### <span data-ttu-id="81f20-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="81f20-153">-TtlInSeconds</span></span>
<span data-ttu-id="81f20-154">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="81f20-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="81f20-155">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="81f20-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="81f20-156">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="81f20-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="81f20-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="81f20-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="81f20-158">UniqueKeyPolicy-objekt av typen Microsoft. Azure. commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="81f20-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="81f20-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81f20-159">-WhatIf</span></span>
<span data-ttu-id="81f20-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81f20-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81f20-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81f20-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81f20-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f20-162">CommonParameters</span></span>
<span data-ttu-id="81f20-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f20-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f20-164">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81f20-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f20-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81f20-165">INPUTS</span></span>

### <span data-ttu-id="81f20-166">Microsoft. Azure. commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="81f20-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="81f20-167">Microsoft. Azure. commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="81f20-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="81f20-168">Microsoft. Azure. commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="81f20-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="81f20-169">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="81f20-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="81f20-170">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="81f20-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="81f20-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81f20-171">OUTPUTS</span></span>

### <span data-ttu-id="81f20-172">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="81f20-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="81f20-173">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="81f20-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="81f20-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81f20-174">NOTES</span></span>

## <span data-ttu-id="81f20-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81f20-175">RELATED LINKS</span></span>
