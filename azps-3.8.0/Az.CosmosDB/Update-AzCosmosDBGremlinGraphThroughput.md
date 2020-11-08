---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089909"
---
# <span data-ttu-id="ddc5a-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="ddc5a-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="ddc5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc5a-103">Uppdaterar genomflödet för ett CosmosDB Gremlin-diagram.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="ddc5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddc5a-104">SYNTAX</span></span>

### <span data-ttu-id="ddc5a-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ddc5a-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc5a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddc5a-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddc5a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddc5a-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddc5a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddc5a-108">EXAMPLES</span></span>

### <span data-ttu-id="ddc5a-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ddc5a-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ddc5a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddc5a-110">PARAMETERS</span></span>

### <span data-ttu-id="ddc5a-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ddc5a-111">-AccountName</span></span>
<span data-ttu-id="ddc5a-112">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ddc5a-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddc5a-113">-Confirm</span></span>
<span data-ttu-id="ddc5a-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc5a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ddc5a-115">-DatabaseName</span></span>
<span data-ttu-id="ddc5a-116">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-116">Database name.</span></span>

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

### <span data-ttu-id="ddc5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc5a-117">-DefaultProfile</span></span>
<span data-ttu-id="ddc5a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc5a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddc5a-119">-InputObject</span></span>
<span data-ttu-id="ddc5a-120">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="ddc5a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ddc5a-121">-Name</span></span>
<span data-ttu-id="ddc5a-122">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="ddc5a-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ddc5a-123">-ParentObject</span></span>
<span data-ttu-id="ddc5a-124">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="ddc5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="ddc5a-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-126">Name of resource group.</span></span>

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

### <span data-ttu-id="ddc5a-127">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="ddc5a-127">-Throughput</span></span>
<span data-ttu-id="ddc5a-128">Genomflödet i Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ddc5a-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="ddc5a-129">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc5a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc5a-130">-WhatIf</span></span>
<span data-ttu-id="ddc5a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc5a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc5a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc5a-133">CommonParameters</span></span>
<span data-ttu-id="ddc5a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc5a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc5a-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddc5a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc5a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddc5a-136">INPUTS</span></span>

### <span data-ttu-id="ddc5a-137">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ddc5a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="ddc5a-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddc5a-138">OUTPUTS</span></span>

### <span data-ttu-id="ddc5a-139">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ddc5a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ddc5a-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddc5a-140">NOTES</span></span>

## <span data-ttu-id="ddc5a-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddc5a-141">RELATED LINKS</span></span>
