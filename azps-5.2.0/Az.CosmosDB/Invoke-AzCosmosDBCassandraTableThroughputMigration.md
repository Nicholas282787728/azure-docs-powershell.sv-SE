---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401787"
---
# <span data-ttu-id="c0c94-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="c0c94-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="c0c94-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0c94-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c94-103">Använd det här alternativet om du vill migrera AutoScale-genomströmning till manuell genomflöde och vice versa.</span><span class="sxs-lookup"><span data-stu-id="c0c94-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="c0c94-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0c94-104">SYNTAX</span></span>

### <span data-ttu-id="c0c94-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c0c94-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c94-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0c94-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c94-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0c94-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c94-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0c94-108">DESCRIPTION</span></span>
<span data-ttu-id="c0c94-109">ThroughpyteType parameter definierar den genomflöde som du vill migrera till.</span><span class="sxs-lookup"><span data-stu-id="c0c94-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="c0c94-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0c94-110">EXAMPLES</span></span>

### <span data-ttu-id="c0c94-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0c94-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="c0c94-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0c94-112">PARAMETERS</span></span>

### <span data-ttu-id="c0c94-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0c94-113">-AccountName</span></span>
<span data-ttu-id="c0c94-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="c0c94-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c0c94-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0c94-115">-Confirm</span></span>
<span data-ttu-id="c0c94-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0c94-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c94-117">-DefaultProfile</span></span>
<span data-ttu-id="c0c94-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c94-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c94-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0c94-119">-InputObject</span></span>
<span data-ttu-id="c0c94-120">Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c0c94-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c94-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="c0c94-121">-KeyspaceName</span></span>
<span data-ttu-id="c0c94-122">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="c0c94-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c0c94-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0c94-123">-Name</span></span>
<span data-ttu-id="c0c94-124">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="c0c94-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="c0c94-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c0c94-125">-ParentObject</span></span>
<span data-ttu-id="c0c94-126">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="c0c94-126">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c94-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c94-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0c94-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c0c94-128">Name of resource group.</span></span>

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

### <span data-ttu-id="c0c94-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="c0c94-129">-ThroughputType</span></span>
<span data-ttu-id="c0c94-130">Data flödes typ att migrera till.</span><span class="sxs-lookup"><span data-stu-id="c0c94-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="c0c94-131">Möjliga värden är: Autoskala, manuell.</span><span class="sxs-lookup"><span data-stu-id="c0c94-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="c0c94-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c94-132">-WhatIf</span></span>
<span data-ttu-id="c0c94-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0c94-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c94-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0c94-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c94-135">CommonParameters</span></span>
<span data-ttu-id="c0c94-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c94-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0c94-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c94-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0c94-138">INPUTS</span></span>

### <span data-ttu-id="c0c94-139">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c0c94-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="c0c94-140">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="c0c94-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="c0c94-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0c94-141">OUTPUTS</span></span>

### <span data-ttu-id="c0c94-142">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c0c94-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c0c94-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0c94-143">NOTES</span></span>

## <span data-ttu-id="c0c94-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0c94-144">RELATED LINKS</span></span>
