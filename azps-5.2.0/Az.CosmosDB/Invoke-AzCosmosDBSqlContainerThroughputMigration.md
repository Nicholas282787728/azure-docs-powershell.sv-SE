---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411480"
---
# <span data-ttu-id="54165-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="54165-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="54165-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54165-102">SYNOPSIS</span></span>
<span data-ttu-id="54165-103">Använd det här alternativet om du vill migrera AutoScale-genomströmning till manuell genomflöde och vice versa.</span><span class="sxs-lookup"><span data-stu-id="54165-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="54165-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54165-104">SYNTAX</span></span>

### <span data-ttu-id="54165-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="54165-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54165-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54165-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54165-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54165-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54165-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54165-108">DESCRIPTION</span></span>
<span data-ttu-id="54165-109">ThroughpyteType parameter definierar den genomflöde som du vill migrera till.</span><span class="sxs-lookup"><span data-stu-id="54165-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="54165-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54165-110">EXAMPLES</span></span>

### <span data-ttu-id="54165-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54165-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="54165-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54165-112">PARAMETERS</span></span>

### <span data-ttu-id="54165-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54165-113">-AccountName</span></span>
<span data-ttu-id="54165-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="54165-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="54165-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54165-115">-Confirm</span></span>
<span data-ttu-id="54165-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54165-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54165-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="54165-117">-DatabaseName</span></span>
<span data-ttu-id="54165-118">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="54165-118">Database name.</span></span>

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

### <span data-ttu-id="54165-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54165-119">-DefaultProfile</span></span>
<span data-ttu-id="54165-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54165-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54165-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54165-121">-InputObject</span></span>
<span data-ttu-id="54165-122">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="54165-122">Sql Container object.</span></span>

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

### <span data-ttu-id="54165-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="54165-123">-Name</span></span>
<span data-ttu-id="54165-124">Container namn.</span><span class="sxs-lookup"><span data-stu-id="54165-124">Container name.</span></span>

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

### <span data-ttu-id="54165-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="54165-125">-ParentObject</span></span>
<span data-ttu-id="54165-126">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="54165-126">Sql Database object.</span></span>

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

### <span data-ttu-id="54165-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54165-127">-ResourceGroupName</span></span>
<span data-ttu-id="54165-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="54165-128">Name of resource group.</span></span>

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

### <span data-ttu-id="54165-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="54165-129">-ThroughputType</span></span>
<span data-ttu-id="54165-130">Data flödes typ att migrera till.</span><span class="sxs-lookup"><span data-stu-id="54165-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="54165-131">Möjliga värden är: Autoskala, manuell.</span><span class="sxs-lookup"><span data-stu-id="54165-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="54165-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54165-132">-WhatIf</span></span>
<span data-ttu-id="54165-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54165-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54165-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54165-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54165-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54165-135">CommonParameters</span></span>
<span data-ttu-id="54165-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54165-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54165-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54165-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54165-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54165-138">INPUTS</span></span>

### <span data-ttu-id="54165-139">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="54165-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="54165-140">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="54165-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="54165-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54165-141">OUTPUTS</span></span>

### <span data-ttu-id="54165-142">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="54165-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="54165-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54165-143">NOTES</span></span>

## <span data-ttu-id="54165-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54165-144">RELATED LINKS</span></span>
