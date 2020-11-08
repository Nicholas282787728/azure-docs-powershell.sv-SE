---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260596"
---
# <span data-ttu-id="dded9-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="dded9-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="dded9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dded9-102">SYNOPSIS</span></span>
<span data-ttu-id="dded9-103">Skapar ett nytt CosmosDB Gremlin-diagram.</span><span class="sxs-lookup"><span data-stu-id="dded9-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="dded9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dded9-104">SYNTAX</span></span>

### <span data-ttu-id="dded9-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dded9-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dded9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dded9-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dded9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dded9-107">DESCRIPTION</span></span>
<span data-ttu-id="dded9-108">Skapar ett nytt CosmosDB Gremlin-diagram.</span><span class="sxs-lookup"><span data-stu-id="dded9-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="dded9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dded9-109">EXAMPLES</span></span>

### <span data-ttu-id="dded9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dded9-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="dded9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dded9-111">PARAMETERS</span></span>

### <span data-ttu-id="dded9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dded9-112">-AccountName</span></span>
<span data-ttu-id="dded9-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="dded9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dded9-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="dded9-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="dded9-115">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="dded9-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="dded9-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dded9-116">-Confirm</span></span>
<span data-ttu-id="dded9-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dded9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dded9-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="dded9-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="dded9-119">ConflictResolutionPolicy-objekt av typen PSConflictResolutionPolicy om det här är angivet som ConflictResolutionPolicy för behållaren.</span><span class="sxs-lookup"><span data-stu-id="dded9-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="dded9-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="dded9-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="dded9-121">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="dded9-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="dded9-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="dded9-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="dded9-123">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="dded9-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="dded9-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="dded9-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="dded9-125">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="dded9-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="dded9-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dded9-126">-DatabaseName</span></span>
<span data-ttu-id="dded9-127">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="dded9-127">Database name.</span></span>

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

### <span data-ttu-id="dded9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dded9-128">-DefaultProfile</span></span>
<span data-ttu-id="dded9-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dded9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dded9-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="dded9-130">-IndexingPolicy</span></span>
<span data-ttu-id="dded9-131">Indexerings princip objekt av typen Microsoft. Azure. commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="dded9-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="dded9-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="dded9-132">-Name</span></span>
<span data-ttu-id="dded9-133">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="dded9-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="dded9-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dded9-134">-ParentObject</span></span>
<span data-ttu-id="dded9-135">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="dded9-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="dded9-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="dded9-136">-PartitionKeyKind</span></span>
<span data-ttu-id="dded9-137">Den typ av algoritm som används för att partitionera.</span><span class="sxs-lookup"><span data-stu-id="dded9-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="dded9-138">Möjliga värden är: ' hash ', ' område '</span><span class="sxs-lookup"><span data-stu-id="dded9-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="dded9-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="dded9-139">-PartitionKeyPath</span></span>
<span data-ttu-id="dded9-140">Sökväg till partitionsnyckel, till exempel "/Address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="dded9-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="dded9-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="dded9-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="dded9-142">Versionen av partitionsnyckel-definitionen</span><span class="sxs-lookup"><span data-stu-id="dded9-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="dded9-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dded9-143">-ResourceGroupName</span></span>
<span data-ttu-id="dded9-144">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dded9-144">Name of resource group.</span></span>

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

### <span data-ttu-id="dded9-145">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="dded9-145">-Throughput</span></span>
<span data-ttu-id="dded9-146">Genomflödet i Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="dded9-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="dded9-147">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="dded9-147">Default value is 400.</span></span>

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

### <span data-ttu-id="dded9-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="dded9-148">-TtlInSeconds</span></span>
<span data-ttu-id="dded9-149">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="dded9-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="dded9-150">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="dded9-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="dded9-151">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="dded9-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="dded9-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="dded9-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="dded9-153">UniqueKeyPolicy-objekt av typen Microsoft. Azure. commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="dded9-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="dded9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dded9-154">-WhatIf</span></span>
<span data-ttu-id="dded9-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dded9-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dded9-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dded9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dded9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dded9-157">CommonParameters</span></span>
<span data-ttu-id="dded9-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dded9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dded9-159">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dded9-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dded9-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dded9-160">INPUTS</span></span>

### <span data-ttu-id="dded9-161">Microsoft. Azure. commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="dded9-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="dded9-162">Microsoft. Azure. commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="dded9-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="dded9-163">Microsoft. Azure. commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="dded9-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="dded9-164">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="dded9-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="dded9-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dded9-165">OUTPUTS</span></span>

### <span data-ttu-id="dded9-166">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="dded9-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="dded9-167">System. Exception</span><span class="sxs-lookup"><span data-stu-id="dded9-167">System.Exception</span></span>

## <span data-ttu-id="dded9-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dded9-168">NOTES</span></span>

## <span data-ttu-id="dded9-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dded9-169">RELATED LINKS</span></span>
