---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321512"
---
# <span data-ttu-id="70fd2-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="70fd2-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="70fd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="70fd2-103">Skapar en ny CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="70fd2-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="70fd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70fd2-104">SYNTAX</span></span>

### <span data-ttu-id="70fd2-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="70fd2-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70fd2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70fd2-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70fd2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70fd2-107">DESCRIPTION</span></span>
<span data-ttu-id="70fd2-108">Skapar en ny CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="70fd2-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="70fd2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70fd2-109">EXAMPLES</span></span>

### <span data-ttu-id="70fd2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="70fd2-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="70fd2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70fd2-111">PARAMETERS</span></span>

### <span data-ttu-id="70fd2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="70fd2-112">-AccountName</span></span>
<span data-ttu-id="70fd2-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="70fd2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="70fd2-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="70fd2-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="70fd2-115">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="70fd2-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="70fd2-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70fd2-116">-Confirm</span></span>
<span data-ttu-id="70fd2-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70fd2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70fd2-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="70fd2-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="70fd2-119">ConflictResolutionPolicy-objekt av typen PSSqlConflictResolutionPolicy om det här är angivet som ConflictResolutionPolicy för behållaren.</span><span class="sxs-lookup"><span data-stu-id="70fd2-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="70fd2-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="70fd2-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="70fd2-121">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="70fd2-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="70fd2-122">Om det anges tillsammans med parametern ConflictResolutionPolicy ignoreras den.</span><span class="sxs-lookup"><span data-stu-id="70fd2-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="70fd2-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="70fd2-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="70fd2-124">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="70fd2-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="70fd2-125">Om det anges tillsammans med parametern ConflictResolutionPolicy ignoreras den.</span><span class="sxs-lookup"><span data-stu-id="70fd2-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="70fd2-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="70fd2-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="70fd2-127">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="70fd2-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="70fd2-128">Om det anges tillsammans med parametern ConflictResolutionPolicy ignoreras den.</span><span class="sxs-lookup"><span data-stu-id="70fd2-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="70fd2-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70fd2-129">-DatabaseName</span></span>
<span data-ttu-id="70fd2-130">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="70fd2-130">Database name.</span></span>

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

### <span data-ttu-id="70fd2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fd2-131">-DefaultProfile</span></span>
<span data-ttu-id="70fd2-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70fd2-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70fd2-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="70fd2-133">-IndexingPolicy</span></span>
<span data-ttu-id="70fd2-134">Indexerings princip objekt av typen Microsoft. Azure. commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="70fd2-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="70fd2-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="70fd2-135">-Name</span></span>
<span data-ttu-id="70fd2-136">Container namn.</span><span class="sxs-lookup"><span data-stu-id="70fd2-136">Container name.</span></span>

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

### <span data-ttu-id="70fd2-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="70fd2-137">-ParentObject</span></span>
<span data-ttu-id="70fd2-138">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="70fd2-138">Sql Database object.</span></span>

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

### <span data-ttu-id="70fd2-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="70fd2-139">-PartitionKeyKind</span></span>
<span data-ttu-id="70fd2-140">Den typ av algoritm som används för att partitionera.</span><span class="sxs-lookup"><span data-stu-id="70fd2-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="70fd2-141">Möjliga värden är: ' hash ', ' område '</span><span class="sxs-lookup"><span data-stu-id="70fd2-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="70fd2-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="70fd2-142">-PartitionKeyPath</span></span>
<span data-ttu-id="70fd2-143">Sökväg till partitionsnyckel, till exempel "/Address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="70fd2-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="70fd2-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="70fd2-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="70fd2-145">Versionen av partitionsnyckel-definitionen</span><span class="sxs-lookup"><span data-stu-id="70fd2-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="70fd2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70fd2-146">-ResourceGroupName</span></span>
<span data-ttu-id="70fd2-147">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70fd2-147">Name of resource group.</span></span>

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

### <span data-ttu-id="70fd2-148">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="70fd2-148">-Throughput</span></span>
<span data-ttu-id="70fd2-149">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="70fd2-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="70fd2-150">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="70fd2-150">Default value is 400.</span></span>

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

### <span data-ttu-id="70fd2-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="70fd2-151">-TtlInSeconds</span></span>
<span data-ttu-id="70fd2-152">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="70fd2-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="70fd2-153">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="70fd2-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="70fd2-154">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="70fd2-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="70fd2-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="70fd2-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="70fd2-156">UniqueKeyPolicy-objekt av typen Microsoft. Azure. commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="70fd2-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="70fd2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70fd2-157">-WhatIf</span></span>
<span data-ttu-id="70fd2-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70fd2-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70fd2-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70fd2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70fd2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fd2-160">CommonParameters</span></span>
<span data-ttu-id="70fd2-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70fd2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fd2-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70fd2-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fd2-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70fd2-163">INPUTS</span></span>

### <span data-ttu-id="70fd2-164">Microsoft. Azure. commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="70fd2-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="70fd2-165">Microsoft. Azure. commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="70fd2-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="70fd2-166">Microsoft. Azure. commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="70fd2-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="70fd2-167">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="70fd2-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="70fd2-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70fd2-168">OUTPUTS</span></span>

### <span data-ttu-id="70fd2-169">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="70fd2-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="70fd2-170">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="70fd2-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="70fd2-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70fd2-171">NOTES</span></span>

## <span data-ttu-id="70fd2-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70fd2-172">RELATED LINKS</span></span>
