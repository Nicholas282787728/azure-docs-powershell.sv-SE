---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321344"
---
# <span data-ttu-id="c0be1-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="c0be1-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="c0be1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0be1-102">SYNOPSIS</span></span>
<span data-ttu-id="c0be1-103">Uppdaterar SQL-containern för CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c0be1-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="c0be1-104">Utför en klient uppdaterings åtgärd genom att läsa den befintliga behållaren.</span><span class="sxs-lookup"><span data-stu-id="c0be1-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="c0be1-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0be1-105">SYNTAX</span></span>

### <span data-ttu-id="c0be1-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c0be1-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0be1-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0be1-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0be1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0be1-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0be1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0be1-109">DESCRIPTION</span></span>
<span data-ttu-id="c0be1-110">Uppdaterar SQL-containern för CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c0be1-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="c0be1-111">Utför en klient uppdaterings åtgärd genom att läsa den befintliga behållaren.</span><span class="sxs-lookup"><span data-stu-id="c0be1-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="c0be1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0be1-112">EXAMPLES</span></span>

### <span data-ttu-id="c0be1-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0be1-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="c0be1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0be1-114">PARAMETERS</span></span>

### <span data-ttu-id="c0be1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0be1-115">-AccountName</span></span>
<span data-ttu-id="c0be1-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="c0be1-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c0be1-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c0be1-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c0be1-118">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="c0be1-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c0be1-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0be1-119">-Confirm</span></span>
<span data-ttu-id="c0be1-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0be1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0be1-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c0be1-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="c0be1-122">ConflictResolutionPolicy-objekt av typen PSSqlConflictResolutionPolicy om det här är angivet som ConflictResolutionPolicy för behållaren.</span><span class="sxs-lookup"><span data-stu-id="c0be1-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0be1-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="c0be1-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="c0be1-124">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="c0be1-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="c0be1-125">Om det anges tillsammans med parametern ConflictResolutionPolicy ignoreras den.</span><span class="sxs-lookup"><span data-stu-id="c0be1-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c0be1-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="c0be1-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="c0be1-127">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="c0be1-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="c0be1-128">Om det anges tillsammans med parametern ConflictResolutionPolicy ignoreras den.</span><span class="sxs-lookup"><span data-stu-id="c0be1-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c0be1-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="c0be1-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="c0be1-130">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="c0be1-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="c0be1-131">Om det anges tillsammans med parametern ConflictResolutionPolicy ignoreras den.</span><span class="sxs-lookup"><span data-stu-id="c0be1-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c0be1-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0be1-132">-DatabaseName</span></span>
<span data-ttu-id="c0be1-133">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="c0be1-133">Database name.</span></span>

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

### <span data-ttu-id="c0be1-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0be1-134">-DefaultProfile</span></span>
<span data-ttu-id="c0be1-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0be1-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0be1-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c0be1-136">-IndexingPolicy</span></span>
<span data-ttu-id="c0be1-137">Indexerings princip objekt av typen Microsoft. Azure. commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="c0be1-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0be1-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0be1-138">-InputObject</span></span>
<span data-ttu-id="c0be1-139">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="c0be1-139">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0be1-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0be1-140">-Name</span></span>
<span data-ttu-id="c0be1-141">Container namn.</span><span class="sxs-lookup"><span data-stu-id="c0be1-141">Container name.</span></span>

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

### <span data-ttu-id="c0be1-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c0be1-142">-ParentObject</span></span>
<span data-ttu-id="c0be1-143">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="c0be1-143">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0be1-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="c0be1-144">-PartitionKeyKind</span></span>
<span data-ttu-id="c0be1-145">Den typ av algoritm som används för att partitionera.</span><span class="sxs-lookup"><span data-stu-id="c0be1-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="c0be1-146">Möjliga värden är: ' hash ', ' område '</span><span class="sxs-lookup"><span data-stu-id="c0be1-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="c0be1-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="c0be1-147">-PartitionKeyPath</span></span>
<span data-ttu-id="c0be1-148">Sökväg till partitionsnyckel, till exempel "/Address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="c0be1-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="c0be1-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c0be1-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="c0be1-150">Versionen av partitionsnyckel-definitionen</span><span class="sxs-lookup"><span data-stu-id="c0be1-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="c0be1-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0be1-151">-ResourceGroupName</span></span>
<span data-ttu-id="c0be1-152">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c0be1-152">Name of resource group.</span></span>

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

### <span data-ttu-id="c0be1-153">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="c0be1-153">-Throughput</span></span>
<span data-ttu-id="c0be1-154">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c0be1-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="c0be1-155">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="c0be1-155">Default value is 400.</span></span>

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

### <span data-ttu-id="c0be1-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c0be1-156">-TtlInSeconds</span></span>
<span data-ttu-id="c0be1-157">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="c0be1-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="c0be1-158">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="c0be1-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="c0be1-159">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="c0be1-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="c0be1-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c0be1-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="c0be1-161">UniqueKeyPolicy-objekt av typen Microsoft. Azure. commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c0be1-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0be1-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0be1-162">-WhatIf</span></span>
<span data-ttu-id="c0be1-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0be1-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0be1-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0be1-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0be1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0be1-165">CommonParameters</span></span>
<span data-ttu-id="c0be1-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0be1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0be1-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0be1-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0be1-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0be1-168">INPUTS</span></span>

### <span data-ttu-id="c0be1-169">Microsoft. Azure. commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c0be1-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="c0be1-170">Microsoft. Azure. commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c0be1-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="c0be1-171">Microsoft. Azure. commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c0be1-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="c0be1-172">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c0be1-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="c0be1-173">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="c0be1-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="c0be1-174">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0be1-174">OUTPUTS</span></span>

### <span data-ttu-id="c0be1-175">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c0be1-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="c0be1-176">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c0be1-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="c0be1-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0be1-177">NOTES</span></span>

## <span data-ttu-id="c0be1-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0be1-178">RELATED LINKS</span></span>