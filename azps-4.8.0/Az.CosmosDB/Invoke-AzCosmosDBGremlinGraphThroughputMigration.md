---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262817"
---
# <span data-ttu-id="1d1c6-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="1d1c6-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="1d1c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d1c6-103">Använd det här alternativet om du vill migrera AutoScale-genomströmning till manuell genomflöde och vice versa.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="1d1c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d1c6-104">SYNTAX</span></span>

### <span data-ttu-id="1d1c6-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d1c6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d1c6-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d1c6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d1c6-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d1c6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d1c6-108">DESCRIPTION</span></span>
<span data-ttu-id="1d1c6-109">ThroughpyteType parameter definierar den genomflöde som du vill migrera till.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="1d1c6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d1c6-110">EXAMPLES</span></span>

### <span data-ttu-id="1d1c6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1d1c6-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="1d1c6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d1c6-112">PARAMETERS</span></span>

### <span data-ttu-id="1d1c6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d1c6-113">-AccountName</span></span>
<span data-ttu-id="1d1c6-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d1c6-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d1c6-115">-Confirm</span></span>
<span data-ttu-id="1d1c6-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d1c6-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d1c6-117">-DatabaseName</span></span>
<span data-ttu-id="1d1c6-118">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-118">Database name.</span></span>

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

### <span data-ttu-id="1d1c6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d1c6-119">-DefaultProfile</span></span>
<span data-ttu-id="1d1c6-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d1c6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d1c6-121">-InputObject</span></span>
<span data-ttu-id="1d1c6-122">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="1d1c6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d1c6-123">-Name</span></span>
<span data-ttu-id="1d1c6-124">Gremlin diagram namn.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="1d1c6-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1d1c6-125">-ParentObject</span></span>
<span data-ttu-id="1d1c6-126">Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="1d1c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d1c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="1d1c6-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-128">Name of resource group.</span></span>

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

### <span data-ttu-id="1d1c6-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="1d1c6-129">-ThroughputType</span></span>
<span data-ttu-id="1d1c6-130">Data flödes typ att migrera till.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="1d1c6-131">Möjliga värden är: Autoskala, manuell.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="1d1c6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d1c6-132">-WhatIf</span></span>
<span data-ttu-id="1d1c6-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d1c6-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d1c6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d1c6-135">CommonParameters</span></span>
<span data-ttu-id="1d1c6-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d1c6-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d1c6-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d1c6-138">INPUTS</span></span>

### <span data-ttu-id="1d1c6-139">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1d1c6-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="1d1c6-140">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="1d1c6-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="1d1c6-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d1c6-141">OUTPUTS</span></span>

### <span data-ttu-id="1d1c6-142">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1d1c6-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1d1c6-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d1c6-143">NOTES</span></span>

## <span data-ttu-id="1d1c6-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d1c6-144">RELATED LINKS</span></span>
