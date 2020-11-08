---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261925"
---
# <span data-ttu-id="9eba1-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="9eba1-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="9eba1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9eba1-102">SYNOPSIS</span></span>
<span data-ttu-id="9eba1-103">Använd det här alternativet om du vill migrera AutoScale-genomströmning till manuell genomflöde och vice versa.</span><span class="sxs-lookup"><span data-stu-id="9eba1-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="9eba1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9eba1-104">SYNTAX</span></span>

### <span data-ttu-id="9eba1-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9eba1-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eba1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eba1-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eba1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eba1-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eba1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9eba1-108">DESCRIPTION</span></span>
<span data-ttu-id="9eba1-109">ThroughpyteType parameter definierar den genomflöde som du vill migrera till.</span><span class="sxs-lookup"><span data-stu-id="9eba1-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="9eba1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9eba1-110">EXAMPLES</span></span>

### <span data-ttu-id="9eba1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9eba1-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="9eba1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9eba1-112">PARAMETERS</span></span>

### <span data-ttu-id="9eba1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9eba1-113">-AccountName</span></span>
<span data-ttu-id="9eba1-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="9eba1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9eba1-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9eba1-115">-Confirm</span></span>
<span data-ttu-id="9eba1-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9eba1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eba1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eba1-117">-DefaultProfile</span></span>
<span data-ttu-id="9eba1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9eba1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eba1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9eba1-119">-InputObject</span></span>
<span data-ttu-id="9eba1-120">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="9eba1-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba1-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9eba1-121">-Name</span></span>
<span data-ttu-id="9eba1-122">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="9eba1-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9eba1-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9eba1-123">-ParentObject</span></span>
<span data-ttu-id="9eba1-124">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="9eba1-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eba1-125">-ResourceGroupName</span></span>
<span data-ttu-id="9eba1-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9eba1-126">Name of resource group.</span></span>

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

### <span data-ttu-id="9eba1-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="9eba1-127">-ThroughputType</span></span>
<span data-ttu-id="9eba1-128">Data flödes typ att migrera till.</span><span class="sxs-lookup"><span data-stu-id="9eba1-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="9eba1-129">Möjliga värden är: Autoskala, manuell.</span><span class="sxs-lookup"><span data-stu-id="9eba1-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="9eba1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eba1-130">-WhatIf</span></span>
<span data-ttu-id="9eba1-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9eba1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eba1-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9eba1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eba1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eba1-133">CommonParameters</span></span>
<span data-ttu-id="9eba1-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eba1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eba1-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9eba1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eba1-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9eba1-136">INPUTS</span></span>

### <span data-ttu-id="9eba1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="9eba1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="9eba1-138">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9eba1-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="9eba1-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9eba1-139">OUTPUTS</span></span>

### <span data-ttu-id="9eba1-140">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9eba1-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9eba1-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9eba1-141">NOTES</span></span>

## <span data-ttu-id="9eba1-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9eba1-142">RELATED LINKS</span></span>
