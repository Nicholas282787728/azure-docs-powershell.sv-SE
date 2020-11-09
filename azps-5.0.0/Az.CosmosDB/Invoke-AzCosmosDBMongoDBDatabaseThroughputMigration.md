---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321620"
---
# <span data-ttu-id="3ed4e-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="3ed4e-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="3ed4e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ed4e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed4e-103">Använd det här alternativet om du vill migrera AutoScale-genomströmning till manuell genomflöde och vice versa.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="3ed4e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ed4e-104">SYNTAX</span></span>

### <span data-ttu-id="3ed4e-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ed4e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ed4e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed4e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ed4e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ed4e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ed4e-108">DESCRIPTION</span></span>
<span data-ttu-id="3ed4e-109">ThroughpyteType parameter definierar den genomflöde som du vill migrera till.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="3ed4e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ed4e-110">EXAMPLES</span></span>

### <span data-ttu-id="3ed4e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3ed4e-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="3ed4e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ed4e-112">PARAMETERS</span></span>

### <span data-ttu-id="3ed4e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3ed4e-113">-AccountName</span></span>
<span data-ttu-id="3ed4e-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3ed4e-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ed4e-115">-Confirm</span></span>
<span data-ttu-id="3ed4e-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ed4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed4e-117">-DefaultProfile</span></span>
<span data-ttu-id="3ed4e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ed4e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ed4e-119">-InputObject</span></span>
<span data-ttu-id="3ed4e-120">Mongo.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="3ed4e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ed4e-121">-Name</span></span>
<span data-ttu-id="3ed4e-122">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-122">Database name.</span></span>

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

### <span data-ttu-id="3ed4e-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3ed4e-123">-ParentObject</span></span>
<span data-ttu-id="3ed4e-124">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="3ed4e-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3ed4e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed4e-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ed4e-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="3ed4e-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="3ed4e-127">-ThroughputType</span></span>
<span data-ttu-id="3ed4e-128">Data flödes typ att migrera till.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="3ed4e-129">Möjliga värden är: Autoskala, manuell.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="3ed4e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed4e-130">-WhatIf</span></span>
<span data-ttu-id="3ed4e-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ed4e-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ed4e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed4e-133">CommonParameters</span></span>
<span data-ttu-id="3ed4e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed4e-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ed4e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed4e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ed4e-136">INPUTS</span></span>

### <span data-ttu-id="3ed4e-137">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3ed4e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="3ed4e-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ed4e-138">OUTPUTS</span></span>

### <span data-ttu-id="3ed4e-139">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3ed4e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3ed4e-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ed4e-140">NOTES</span></span>

## <span data-ttu-id="3ed4e-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ed4e-141">RELATED LINKS</span></span>
