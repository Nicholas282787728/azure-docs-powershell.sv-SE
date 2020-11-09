---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321391"
---
# <span data-ttu-id="fb3d2-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="fb3d2-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="fb3d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3d2-103">Uppdaterar genomflödet för ett CosmosDB Cassandra-par.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="fb3d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb3d2-104">SYNTAX</span></span>

### <span data-ttu-id="fb3d2-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fb3d2-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb3d2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3d2-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb3d2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3d2-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3d2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb3d2-108">DESCRIPTION</span></span>
<span data-ttu-id="fb3d2-109">Uppdaterar genomflödet för ett CosmosDB Cassandra-par.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="fb3d2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb3d2-110">EXAMPLES</span></span>

### <span data-ttu-id="fb3d2-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fb3d2-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="fb3d2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb3d2-112">PARAMETERS</span></span>

### <span data-ttu-id="fb3d2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb3d2-113">-AccountName</span></span>
<span data-ttu-id="fb3d2-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fb3d2-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="fb3d2-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="fb3d2-116">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="fb3d2-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb3d2-117">-Confirm</span></span>
<span data-ttu-id="fb3d2-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb3d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3d2-119">-DefaultProfile</span></span>
<span data-ttu-id="fb3d2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb3d2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb3d2-121">-InputObject</span></span>
<span data-ttu-id="fb3d2-122">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fb3d2-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fb3d2-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb3d2-123">-Name</span></span>
<span data-ttu-id="fb3d2-124">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="fb3d2-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fb3d2-125">-ParentObject</span></span>
<span data-ttu-id="fb3d2-126">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fb3d2-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fb3d2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3d2-127">-ResourceGroupName</span></span>
<span data-ttu-id="fb3d2-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-128">Name of resource group.</span></span>

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

### <span data-ttu-id="fb3d2-129">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="fb3d2-129">-Throughput</span></span>
<span data-ttu-id="fb3d2-130">Genomflödet av Cassandra-tecken (RU/s).</span><span class="sxs-lookup"><span data-stu-id="fb3d2-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="fb3d2-131">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-131">Default value is 400.</span></span>

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

### <span data-ttu-id="fb3d2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3d2-132">-WhatIf</span></span>
<span data-ttu-id="fb3d2-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3d2-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb3d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3d2-135">CommonParameters</span></span>
<span data-ttu-id="fb3d2-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3d2-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb3d2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3d2-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb3d2-138">INPUTS</span></span>

### <span data-ttu-id="fb3d2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fb3d2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="fb3d2-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb3d2-140">OUTPUTS</span></span>

### <span data-ttu-id="fb3d2-141">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fb3d2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fb3d2-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb3d2-142">NOTES</span></span>

## <span data-ttu-id="fb3d2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb3d2-143">RELATED LINKS</span></span>
