---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260280"
---
# <span data-ttu-id="353ab-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="353ab-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="353ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="353ab-102">SYNOPSIS</span></span>
<span data-ttu-id="353ab-103">Uppdaterar CosmosDB Gremlin-databasen.</span><span class="sxs-lookup"><span data-stu-id="353ab-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="353ab-104">Utför en klient uppdaterings åtgärd genom att läsa den befintliga databasen.</span><span class="sxs-lookup"><span data-stu-id="353ab-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="353ab-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="353ab-105">SYNTAX</span></span>

### <span data-ttu-id="353ab-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="353ab-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="353ab-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="353ab-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="353ab-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="353ab-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="353ab-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="353ab-109">DESCRIPTION</span></span>
<span data-ttu-id="353ab-110">Uppdaterar CosmosDB Gremlin-databasen.</span><span class="sxs-lookup"><span data-stu-id="353ab-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="353ab-111">Utför en klient uppdaterings åtgärd genom att läsa den befintliga databasen.</span><span class="sxs-lookup"><span data-stu-id="353ab-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="353ab-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="353ab-112">EXAMPLES</span></span>

### <span data-ttu-id="353ab-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="353ab-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="353ab-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="353ab-114">PARAMETERS</span></span>

### <span data-ttu-id="353ab-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="353ab-115">-AccountName</span></span>
<span data-ttu-id="353ab-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="353ab-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="353ab-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="353ab-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="353ab-118">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="353ab-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="353ab-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="353ab-119">-Confirm</span></span>
<span data-ttu-id="353ab-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="353ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="353ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353ab-121">-DefaultProfile</span></span>
<span data-ttu-id="353ab-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="353ab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="353ab-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="353ab-123">-InputObject</span></span>
<span data-ttu-id="353ab-124">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="353ab-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="353ab-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="353ab-125">-Name</span></span>
<span data-ttu-id="353ab-126">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="353ab-126">Database name.</span></span>

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

### <span data-ttu-id="353ab-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="353ab-127">-ParentObject</span></span>
<span data-ttu-id="353ab-128">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="353ab-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="353ab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="353ab-129">-ResourceGroupName</span></span>
<span data-ttu-id="353ab-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="353ab-130">Name of resource group.</span></span>

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

### <span data-ttu-id="353ab-131">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="353ab-131">-Throughput</span></span>
<span data-ttu-id="353ab-132">Genomflödet i Gremlin databas (RU/s).</span><span class="sxs-lookup"><span data-stu-id="353ab-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="353ab-133">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="353ab-133">Default value is 400.</span></span>

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

### <span data-ttu-id="353ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="353ab-134">-WhatIf</span></span>
<span data-ttu-id="353ab-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="353ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="353ab-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="353ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="353ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353ab-137">CommonParameters</span></span>
<span data-ttu-id="353ab-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353ab-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="353ab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353ab-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="353ab-140">INPUTS</span></span>

### <span data-ttu-id="353ab-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="353ab-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="353ab-142">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="353ab-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="353ab-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="353ab-143">OUTPUTS</span></span>

### <span data-ttu-id="353ab-144">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="353ab-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="353ab-145">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="353ab-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="353ab-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="353ab-146">NOTES</span></span>

## <span data-ttu-id="353ab-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="353ab-147">RELATED LINKS</span></span>
