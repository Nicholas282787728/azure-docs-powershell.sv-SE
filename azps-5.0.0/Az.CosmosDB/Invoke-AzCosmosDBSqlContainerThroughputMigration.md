---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321619"
---
# <span data-ttu-id="2a286-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="2a286-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="2a286-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a286-102">SYNOPSIS</span></span>
<span data-ttu-id="2a286-103">Använd det här alternativet om du vill migrera AutoScale-genomströmning till manuell genomflöde och vice versa.</span><span class="sxs-lookup"><span data-stu-id="2a286-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="2a286-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a286-104">SYNTAX</span></span>

### <span data-ttu-id="2a286-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2a286-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a286-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a286-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a286-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a286-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a286-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a286-108">DESCRIPTION</span></span>
<span data-ttu-id="2a286-109">ThroughpyteType parameter definierar den genomflöde som du vill migrera till.</span><span class="sxs-lookup"><span data-stu-id="2a286-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="2a286-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a286-110">EXAMPLES</span></span>

### <span data-ttu-id="2a286-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a286-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="2a286-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a286-112">PARAMETERS</span></span>

### <span data-ttu-id="2a286-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2a286-113">-AccountName</span></span>
<span data-ttu-id="2a286-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="2a286-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2a286-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a286-115">-Confirm</span></span>
<span data-ttu-id="2a286-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a286-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a286-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a286-117">-DatabaseName</span></span>
<span data-ttu-id="2a286-118">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="2a286-118">Database name.</span></span>

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

### <span data-ttu-id="2a286-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a286-119">-DefaultProfile</span></span>
<span data-ttu-id="2a286-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a286-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a286-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a286-121">-InputObject</span></span>
<span data-ttu-id="2a286-122">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="2a286-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a286-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a286-123">-Name</span></span>
<span data-ttu-id="2a286-124">Container namn.</span><span class="sxs-lookup"><span data-stu-id="2a286-124">Container name.</span></span>

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

### <span data-ttu-id="2a286-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2a286-125">-ParentObject</span></span>
<span data-ttu-id="2a286-126">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="2a286-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a286-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a286-127">-ResourceGroupName</span></span>
<span data-ttu-id="2a286-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2a286-128">Name of resource group.</span></span>

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

### <span data-ttu-id="2a286-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="2a286-129">-ThroughputType</span></span>
<span data-ttu-id="2a286-130">Data flödes typ att migrera till.</span><span class="sxs-lookup"><span data-stu-id="2a286-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="2a286-131">Möjliga värden är: Autoskala, manuell.</span><span class="sxs-lookup"><span data-stu-id="2a286-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="2a286-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a286-132">-WhatIf</span></span>
<span data-ttu-id="2a286-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a286-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a286-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a286-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a286-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a286-135">CommonParameters</span></span>
<span data-ttu-id="2a286-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a286-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a286-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a286-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a286-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a286-138">INPUTS</span></span>

### <span data-ttu-id="2a286-139">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2a286-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="2a286-140">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2a286-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="2a286-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a286-141">OUTPUTS</span></span>

### <span data-ttu-id="2a286-142">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2a286-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2a286-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a286-143">NOTES</span></span>

## <span data-ttu-id="2a286-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a286-144">RELATED LINKS</span></span>
