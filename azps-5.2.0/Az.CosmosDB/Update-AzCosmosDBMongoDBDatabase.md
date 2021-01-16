---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412579"
---
# <span data-ttu-id="5ce23-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="5ce23-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="5ce23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ce23-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce23-103">Uppdaterar CosmosDB MongoDB-databasen.</span><span class="sxs-lookup"><span data-stu-id="5ce23-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="5ce23-104">Utför en klient uppdaterings åtgärd genom att läsa den befintliga databasen.</span><span class="sxs-lookup"><span data-stu-id="5ce23-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="5ce23-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ce23-105">SYNTAX</span></span>

### <span data-ttu-id="5ce23-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5ce23-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce23-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ce23-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce23-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ce23-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ce23-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ce23-109">DESCRIPTION</span></span>
<span data-ttu-id="5ce23-110">Uppdaterar CosmosDB MongoDB-databasen.</span><span class="sxs-lookup"><span data-stu-id="5ce23-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="5ce23-111">Utför en klient uppdaterings åtgärd genom att läsa den befintliga databasen.</span><span class="sxs-lookup"><span data-stu-id="5ce23-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="5ce23-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ce23-112">EXAMPLES</span></span>

### <span data-ttu-id="5ce23-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5ce23-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="5ce23-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ce23-114">PARAMETERS</span></span>

### <span data-ttu-id="5ce23-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5ce23-115">-AccountName</span></span>
<span data-ttu-id="5ce23-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="5ce23-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5ce23-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5ce23-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5ce23-118">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="5ce23-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5ce23-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ce23-119">-Confirm</span></span>
<span data-ttu-id="5ce23-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ce23-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce23-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce23-121">-DefaultProfile</span></span>
<span data-ttu-id="5ce23-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce23-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce23-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ce23-123">-InputObject</span></span>
<span data-ttu-id="5ce23-124">Mongo.</span><span class="sxs-lookup"><span data-stu-id="5ce23-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce23-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ce23-125">-Name</span></span>
<span data-ttu-id="5ce23-126">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="5ce23-126">Database name.</span></span>

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

### <span data-ttu-id="5ce23-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5ce23-127">-ParentObject</span></span>
<span data-ttu-id="5ce23-128">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5ce23-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce23-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce23-129">-ResourceGroupName</span></span>
<span data-ttu-id="5ce23-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ce23-130">Name of resource group.</span></span>

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

### <span data-ttu-id="5ce23-131">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="5ce23-131">-Throughput</span></span>
<span data-ttu-id="5ce23-132">Genomflödet i Mongo databas (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5ce23-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="5ce23-133">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="5ce23-133">Default value is 400.</span></span>

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

### <span data-ttu-id="5ce23-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce23-134">-WhatIf</span></span>
<span data-ttu-id="5ce23-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ce23-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce23-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ce23-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce23-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce23-137">CommonParameters</span></span>
<span data-ttu-id="5ce23-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce23-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce23-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ce23-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce23-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ce23-140">INPUTS</span></span>

### <span data-ttu-id="5ce23-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="5ce23-141">None</span></span>

## <span data-ttu-id="5ce23-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ce23-142">OUTPUTS</span></span>

### <span data-ttu-id="5ce23-143">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5ce23-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="5ce23-144">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="5ce23-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="5ce23-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ce23-145">NOTES</span></span>

## <span data-ttu-id="5ce23-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ce23-146">RELATED LINKS</span></span>
