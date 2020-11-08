---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092151"
---
# <span data-ttu-id="fd7a8-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="fd7a8-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="fd7a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd7a8-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7a8-103">Skapar en ny eller uppdaterar en befintlig CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="fd7a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd7a8-104">SYNTAX</span></span>

### <span data-ttu-id="fd7a8-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fd7a8-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7a8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd7a8-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd7a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd7a8-107">DESCRIPTION</span></span>
<span data-ttu-id="fd7a8-108">Cmdleten **set-AzCosmosDBSqlContainer** skapar en ny eller uppdaterar en befintlig CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="fd7a8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd7a8-109">EXAMPLES</span></span>

### <span data-ttu-id="fd7a8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fd7a8-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="fd7a8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd7a8-111">PARAMETERS</span></span>

### <span data-ttu-id="fd7a8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd7a8-112">-AccountName</span></span>
<span data-ttu-id="fd7a8-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fd7a8-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd7a8-114">-Confirm</span></span>
<span data-ttu-id="fd7a8-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7a8-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fd7a8-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="fd7a8-117">ConflictResolutionPolicy-objekt av typen PSSqlConflictResolutionPolicy om det här är angivet som ConflictResolutionPolicy för behållaren.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="fd7a8-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="fd7a8-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="fd7a8-119">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="fd7a8-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="fd7a8-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="fd7a8-121">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="fd7a8-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="fd7a8-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="fd7a8-123">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="fd7a8-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fd7a8-124">-DatabaseName</span></span>
<span data-ttu-id="fd7a8-125">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-125">Database name.</span></span>

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

### <span data-ttu-id="fd7a8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7a8-126">-DefaultProfile</span></span>
<span data-ttu-id="fd7a8-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd7a8-128">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="fd7a8-128">-IndexingPolicy</span></span>
<span data-ttu-id="fd7a8-129">Indexerings princip objekt av typen Microsoft. Azure. commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="fd7a8-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd7a8-130">-InputObject</span></span>
<span data-ttu-id="fd7a8-131">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-131">Sql Database object.</span></span>

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

### <span data-ttu-id="fd7a8-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="fd7a8-132">-Name</span></span>
<span data-ttu-id="fd7a8-133">Container namn.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-133">Container name.</span></span>

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

### <span data-ttu-id="fd7a8-134">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="fd7a8-134">-PartitionKeyKind</span></span>
<span data-ttu-id="fd7a8-135">Den typ av algoritm som används för att partitionera.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="fd7a8-136">Möjliga värden är: ' hash ', ' område '</span><span class="sxs-lookup"><span data-stu-id="fd7a8-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="fd7a8-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="fd7a8-137">-PartitionKeyPath</span></span>
<span data-ttu-id="fd7a8-138">Sökväg till partitionsnyckel, till exempel "/Address/zipcode".</span><span class="sxs-lookup"><span data-stu-id="fd7a8-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="fd7a8-139">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="fd7a8-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="fd7a8-140">Versionen av partitionsnyckel-definitionen</span><span class="sxs-lookup"><span data-stu-id="fd7a8-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="fd7a8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7a8-141">-ResourceGroupName</span></span>
<span data-ttu-id="fd7a8-142">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-142">Name of resource group.</span></span>

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

### <span data-ttu-id="fd7a8-143">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="fd7a8-143">-Throughput</span></span>
<span data-ttu-id="fd7a8-144">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="fd7a8-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="fd7a8-145">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-145">Default value is 400.</span></span>

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

### <span data-ttu-id="fd7a8-146">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="fd7a8-146">-TtlInSeconds</span></span>
<span data-ttu-id="fd7a8-147">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="fd7a8-148">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="fd7a8-149">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="fd7a8-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="fd7a8-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="fd7a8-151">UniqueKeyPolicy-objekt av typen Microsoft. Azure. commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="fd7a8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7a8-152">-WhatIf</span></span>
<span data-ttu-id="fd7a8-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd7a8-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd7a8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7a8-155">CommonParameters</span></span>
<span data-ttu-id="fd7a8-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd7a8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7a8-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd7a8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7a8-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd7a8-158">INPUTS</span></span>

### <span data-ttu-id="fd7a8-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="fd7a8-159">None</span></span>

## <span data-ttu-id="fd7a8-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd7a8-160">OUTPUTS</span></span>

### <span data-ttu-id="fd7a8-161">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fd7a8-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="fd7a8-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd7a8-162">NOTES</span></span>

## <span data-ttu-id="fd7a8-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd7a8-163">RELATED LINKS</span></span>
