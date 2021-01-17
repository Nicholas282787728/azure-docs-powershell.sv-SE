---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: e2f1449536f9b4db5b743c1a1e352e427ae86821
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400104"
---
# <span data-ttu-id="82421-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="82421-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="82421-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82421-102">SYNOPSIS</span></span>
<span data-ttu-id="82421-103">Använd det här alternativet om du vill migrera AutoScale-genomströmning till manuell genomflöde och vice versa.</span><span class="sxs-lookup"><span data-stu-id="82421-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="82421-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82421-104">SYNTAX</span></span>

### <span data-ttu-id="82421-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="82421-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82421-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82421-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82421-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82421-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82421-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82421-108">DESCRIPTION</span></span>
<span data-ttu-id="82421-109">ThroughpyteType parameter definierar den genomflöde som du vill migrera till.</span><span class="sxs-lookup"><span data-stu-id="82421-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="82421-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82421-110">EXAMPLES</span></span>

### <span data-ttu-id="82421-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82421-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```


## <span data-ttu-id="82421-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82421-112">PARAMETERS</span></span>

### <span data-ttu-id="82421-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82421-113">-AccountName</span></span>
<span data-ttu-id="82421-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="82421-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="82421-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82421-115">-Confirm</span></span>
<span data-ttu-id="82421-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82421-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82421-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="82421-117">-DatabaseName</span></span>
<span data-ttu-id="82421-118">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="82421-118">Database name.</span></span>

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

### <span data-ttu-id="82421-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82421-119">-DefaultProfile</span></span>
<span data-ttu-id="82421-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82421-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82421-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82421-121">-InputObject</span></span>
<span data-ttu-id="82421-122">Mongo.</span><span class="sxs-lookup"><span data-stu-id="82421-122">Mongo Collection object.</span></span>

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

### <span data-ttu-id="82421-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="82421-123">-Name</span></span>
<span data-ttu-id="82421-124">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="82421-124">Collection name.</span></span>

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

### <span data-ttu-id="82421-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="82421-125">-ParentObject</span></span>
<span data-ttu-id="82421-126">Mongo.</span><span class="sxs-lookup"><span data-stu-id="82421-126">Mongo Database object.</span></span>

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

### <span data-ttu-id="82421-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82421-127">-ResourceGroupName</span></span>
<span data-ttu-id="82421-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="82421-128">Name of resource group.</span></span>

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

### <span data-ttu-id="82421-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="82421-129">-ThroughputType</span></span>
<span data-ttu-id="82421-130">Data flödes typ att migrera till.</span><span class="sxs-lookup"><span data-stu-id="82421-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="82421-131">Möjliga värden är: Autoskala, manuell.</span><span class="sxs-lookup"><span data-stu-id="82421-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="82421-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82421-132">-WhatIf</span></span>
<span data-ttu-id="82421-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82421-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82421-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82421-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82421-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82421-135">CommonParameters</span></span>
<span data-ttu-id="82421-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82421-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82421-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82421-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82421-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82421-138">INPUTS</span></span>

### <span data-ttu-id="82421-139">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="82421-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="82421-140">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="82421-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="82421-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82421-141">OUTPUTS</span></span>

### <span data-ttu-id="82421-142">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="82421-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="82421-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82421-143">NOTES</span></span>

## <span data-ttu-id="82421-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82421-144">RELATED LINKS</span></span>
