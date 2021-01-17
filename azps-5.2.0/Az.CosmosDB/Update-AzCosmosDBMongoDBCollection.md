---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417848"
---
# <span data-ttu-id="931c5-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="931c5-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="931c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="931c5-102">SYNOPSIS</span></span>
<span data-ttu-id="931c5-103">Uppdaterar CosmosDB MongoDB-samlingen.</span><span class="sxs-lookup"><span data-stu-id="931c5-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="931c5-104">Utför en klient uppdaterings åtgärd genom att läsa den befintliga samlingen.</span><span class="sxs-lookup"><span data-stu-id="931c5-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="931c5-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="931c5-105">SYNTAX</span></span>

### <span data-ttu-id="931c5-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="931c5-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="931c5-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="931c5-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="931c5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="931c5-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="931c5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="931c5-109">DESCRIPTION</span></span>
<span data-ttu-id="931c5-110">Uppdaterar CosmosDB MongoDB-samlingen.</span><span class="sxs-lookup"><span data-stu-id="931c5-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="931c5-111">Utför en klient uppdaterings åtgärd genom att läsa den befintliga samlingen.</span><span class="sxs-lookup"><span data-stu-id="931c5-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="931c5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="931c5-112">EXAMPLES</span></span>

### <span data-ttu-id="931c5-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="931c5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="931c5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="931c5-114">PARAMETERS</span></span>

### <span data-ttu-id="931c5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="931c5-115">-AccountName</span></span>
<span data-ttu-id="931c5-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="931c5-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="931c5-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="931c5-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="931c5-118">TTL för analytisk lagring.</span><span class="sxs-lookup"><span data-stu-id="931c5-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="931c5-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="931c5-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="931c5-120">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="931c5-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="931c5-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="931c5-121">-Confirm</span></span>
<span data-ttu-id="931c5-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="931c5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="931c5-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="931c5-123">-DatabaseName</span></span>
<span data-ttu-id="931c5-124">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="931c5-124">Database name.</span></span>

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

### <span data-ttu-id="931c5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="931c5-125">-DefaultProfile</span></span>
<span data-ttu-id="931c5-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="931c5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="931c5-127">-Index</span><span class="sxs-lookup"><span data-stu-id="931c5-127">-Index</span></span>
<span data-ttu-id="931c5-128">Matris med PSMongoIndex-objekt.</span><span class="sxs-lookup"><span data-stu-id="931c5-128">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="931c5-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="931c5-129">-InputObject</span></span>
<span data-ttu-id="931c5-130">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="931c5-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="931c5-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="931c5-131">-Name</span></span>
<span data-ttu-id="931c5-132">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="931c5-132">Collection name.</span></span>

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

### <span data-ttu-id="931c5-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="931c5-133">-ParentObject</span></span>
<span data-ttu-id="931c5-134">Mongo.</span><span class="sxs-lookup"><span data-stu-id="931c5-134">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="931c5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="931c5-135">-ResourceGroupName</span></span>
<span data-ttu-id="931c5-136">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="931c5-136">Name of resource group.</span></span>

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

### <span data-ttu-id="931c5-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="931c5-137">-Shard</span></span>
<span data-ttu-id="931c5-138">Sharding nyckel Sök väg.</span><span class="sxs-lookup"><span data-stu-id="931c5-138">Sharding key path.</span></span>

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

### <span data-ttu-id="931c5-139">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="931c5-139">-Throughput</span></span>
<span data-ttu-id="931c5-140">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="931c5-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="931c5-141">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="931c5-141">Default value is 400.</span></span>

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

### <span data-ttu-id="931c5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="931c5-142">-WhatIf</span></span>
<span data-ttu-id="931c5-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="931c5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="931c5-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="931c5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="931c5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931c5-145">CommonParameters</span></span>
<span data-ttu-id="931c5-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="931c5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931c5-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="931c5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931c5-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="931c5-148">INPUTS</span></span>

### <span data-ttu-id="931c5-149">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="931c5-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="931c5-150">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="931c5-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="931c5-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="931c5-151">OUTPUTS</span></span>

### <span data-ttu-id="931c5-152">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="931c5-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="931c5-153">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="931c5-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="931c5-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="931c5-154">NOTES</span></span>

## <span data-ttu-id="931c5-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="931c5-155">RELATED LINKS</span></span>
