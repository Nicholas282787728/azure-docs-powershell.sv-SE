---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524380"
---
# <span data-ttu-id="82cc7-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="82cc7-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="82cc7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="82cc7-103">Hämtar data flödet för ett CosmosDB Gremlin-diagram.</span><span class="sxs-lookup"><span data-stu-id="82cc7-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="82cc7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82cc7-104">SYNTAX</span></span>

### <span data-ttu-id="82cc7-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="82cc7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cc7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82cc7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82cc7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82cc7-107">DESCRIPTION</span></span>
<span data-ttu-id="82cc7-108">Cmdleten **Get-AzCosmosDBGremlinGraphThroughput** hämtar genomflödet för ett CosmosDB-Gremlin-diagram.</span><span class="sxs-lookup"><span data-stu-id="82cc7-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="82cc7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82cc7-109">EXAMPLES</span></span>

### <span data-ttu-id="82cc7-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82cc7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="82cc7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82cc7-111">PARAMETERS</span></span>

### <span data-ttu-id="82cc7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82cc7-112">-AccountName</span></span>
<span data-ttu-id="82cc7-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="82cc7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="82cc7-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82cc7-114">-Confirm</span></span>
<span data-ttu-id="82cc7-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82cc7-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82cc7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="82cc7-116">-DatabaseName</span></span>
<span data-ttu-id="82cc7-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="82cc7-117">Database name.</span></span>

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

### <span data-ttu-id="82cc7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82cc7-118">-DefaultProfile</span></span>
<span data-ttu-id="82cc7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82cc7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82cc7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82cc7-120">-InputObject</span></span>
<span data-ttu-id="82cc7-121">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="82cc7-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82cc7-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="82cc7-122">-Name</span></span>
<span data-ttu-id="82cc7-123">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="82cc7-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="82cc7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82cc7-124">-ResourceGroupName</span></span>
<span data-ttu-id="82cc7-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="82cc7-125">Name of resource group.</span></span>

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

### <span data-ttu-id="82cc7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82cc7-126">-WhatIf</span></span>
<span data-ttu-id="82cc7-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82cc7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82cc7-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82cc7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82cc7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82cc7-129">CommonParameters</span></span>
<span data-ttu-id="82cc7-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82cc7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82cc7-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82cc7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82cc7-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82cc7-132">INPUTS</span></span>

### <span data-ttu-id="82cc7-133">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="82cc7-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="82cc7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82cc7-134">OUTPUTS</span></span>

### <span data-ttu-id="82cc7-135">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="82cc7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="82cc7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82cc7-136">NOTES</span></span>

## <span data-ttu-id="82cc7-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82cc7-137">RELATED LINKS</span></span>
