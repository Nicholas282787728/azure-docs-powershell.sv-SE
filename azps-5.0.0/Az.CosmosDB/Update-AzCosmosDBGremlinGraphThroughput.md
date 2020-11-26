---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321363"
---
# <span data-ttu-id="d44c0-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="d44c0-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="d44c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d44c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d44c0-103">Uppdaterar genomflödet för ett CosmosDB Gremlin-diagram.</span><span class="sxs-lookup"><span data-stu-id="d44c0-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="d44c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d44c0-104">SYNTAX</span></span>

### <span data-ttu-id="d44c0-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d44c0-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44c0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d44c0-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44c0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d44c0-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d44c0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d44c0-108">DESCRIPTION</span></span>
<span data-ttu-id="d44c0-109">Uppdaterar genomflödet för ett CosmosDB Gremlin-diagram.</span><span class="sxs-lookup"><span data-stu-id="d44c0-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="d44c0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d44c0-110">EXAMPLES</span></span>

### <span data-ttu-id="d44c0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d44c0-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="d44c0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d44c0-112">PARAMETERS</span></span>

### <span data-ttu-id="d44c0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d44c0-113">-AccountName</span></span>
<span data-ttu-id="d44c0-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="d44c0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d44c0-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d44c0-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d44c0-116">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="d44c0-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d44c0-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d44c0-117">-Confirm</span></span>
<span data-ttu-id="d44c0-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d44c0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d44c0-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d44c0-119">-DatabaseName</span></span>
<span data-ttu-id="d44c0-120">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="d44c0-120">Database name.</span></span>

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

### <span data-ttu-id="d44c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d44c0-121">-DefaultProfile</span></span>
<span data-ttu-id="d44c0-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d44c0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d44c0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d44c0-123">-InputObject</span></span>
<span data-ttu-id="d44c0-124">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d44c0-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="d44c0-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d44c0-125">-Name</span></span>
<span data-ttu-id="d44c0-126">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="d44c0-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="d44c0-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d44c0-127">-ParentObject</span></span>
<span data-ttu-id="d44c0-128">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d44c0-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="d44c0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d44c0-129">-ResourceGroupName</span></span>
<span data-ttu-id="d44c0-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d44c0-130">Name of resource group.</span></span>

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

### <span data-ttu-id="d44c0-131">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="d44c0-131">-Throughput</span></span>
<span data-ttu-id="d44c0-132">Genomflödet i Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d44c0-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="d44c0-133">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="d44c0-133">Default value is 400.</span></span>

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

### <span data-ttu-id="d44c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d44c0-134">-WhatIf</span></span>
<span data-ttu-id="d44c0-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d44c0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d44c0-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d44c0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d44c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d44c0-137">CommonParameters</span></span>
<span data-ttu-id="d44c0-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d44c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d44c0-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d44c0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d44c0-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d44c0-140">INPUTS</span></span>

### <span data-ttu-id="d44c0-141">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d44c0-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="d44c0-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d44c0-142">OUTPUTS</span></span>

### <span data-ttu-id="d44c0-143">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d44c0-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d44c0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d44c0-144">NOTES</span></span>

## <span data-ttu-id="d44c0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d44c0-145">RELATED LINKS</span></span>