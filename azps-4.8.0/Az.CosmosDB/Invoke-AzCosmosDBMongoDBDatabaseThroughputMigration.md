---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262358"
---
# <span data-ttu-id="8d958-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="8d958-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="8d958-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d958-102">SYNOPSIS</span></span>
<span data-ttu-id="8d958-103">Använd det här alternativet om du vill migrera AutoScale-genomströmning till manuell genomflöde och vice versa.</span><span class="sxs-lookup"><span data-stu-id="8d958-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="8d958-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d958-104">SYNTAX</span></span>

### <span data-ttu-id="8d958-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8d958-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d958-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d958-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d958-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d958-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d958-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d958-108">DESCRIPTION</span></span>
<span data-ttu-id="8d958-109">ThroughpyteType parameter definierar den genomflöde som du vill migrera till.</span><span class="sxs-lookup"><span data-stu-id="8d958-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="8d958-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d958-110">EXAMPLES</span></span>

### <span data-ttu-id="8d958-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8d958-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="8d958-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d958-112">PARAMETERS</span></span>

### <span data-ttu-id="8d958-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d958-113">-AccountName</span></span>
<span data-ttu-id="8d958-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="8d958-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8d958-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d958-115">-Confirm</span></span>
<span data-ttu-id="8d958-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d958-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d958-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d958-117">-DefaultProfile</span></span>
<span data-ttu-id="8d958-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d958-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d958-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d958-119">-InputObject</span></span>
<span data-ttu-id="8d958-120">Mongo.</span><span class="sxs-lookup"><span data-stu-id="8d958-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d958-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d958-121">-Name</span></span>
<span data-ttu-id="8d958-122">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="8d958-122">Database name.</span></span>

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

### <span data-ttu-id="8d958-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8d958-123">-ParentObject</span></span>
<span data-ttu-id="8d958-124">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8d958-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8d958-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d958-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d958-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8d958-126">Name of resource group.</span></span>

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

### <span data-ttu-id="8d958-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="8d958-127">-ThroughputType</span></span>
<span data-ttu-id="8d958-128">Data flödes typ att migrera till.</span><span class="sxs-lookup"><span data-stu-id="8d958-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="8d958-129">Möjliga värden är: Autoskala, manuell.</span><span class="sxs-lookup"><span data-stu-id="8d958-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="8d958-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d958-130">-WhatIf</span></span>
<span data-ttu-id="8d958-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d958-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d958-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d958-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d958-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d958-133">CommonParameters</span></span>
<span data-ttu-id="8d958-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d958-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d958-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d958-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d958-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d958-136">INPUTS</span></span>

### <span data-ttu-id="8d958-137">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8d958-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="8d958-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d958-138">OUTPUTS</span></span>

### <span data-ttu-id="8d958-139">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8d958-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8d958-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d958-140">NOTES</span></span>

## <span data-ttu-id="8d958-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d958-141">RELATED LINKS</span></span>