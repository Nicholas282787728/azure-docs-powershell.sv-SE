---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321387"
---
# <span data-ttu-id="42af6-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="42af6-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="42af6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42af6-102">SYNOPSIS</span></span>
<span data-ttu-id="42af6-103">Uppdaterar genomflödet för en CosmosDB Cassandra-tabell.</span><span class="sxs-lookup"><span data-stu-id="42af6-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="42af6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42af6-104">SYNTAX</span></span>

### <span data-ttu-id="42af6-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="42af6-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42af6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42af6-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42af6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42af6-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42af6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42af6-108">DESCRIPTION</span></span>
<span data-ttu-id="42af6-109">Uppdaterar genomflödet för en CosmosDB Cassandra-tabell.</span><span class="sxs-lookup"><span data-stu-id="42af6-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="42af6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42af6-110">EXAMPLES</span></span>

### <span data-ttu-id="42af6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42af6-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="42af6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42af6-112">PARAMETERS</span></span>

### <span data-ttu-id="42af6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42af6-113">-AccountName</span></span>
<span data-ttu-id="42af6-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="42af6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="42af6-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="42af6-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="42af6-116">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="42af6-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="42af6-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42af6-117">-Confirm</span></span>
<span data-ttu-id="42af6-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42af6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42af6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42af6-119">-DefaultProfile</span></span>
<span data-ttu-id="42af6-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42af6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42af6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42af6-121">-InputObject</span></span>
<span data-ttu-id="42af6-122">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="42af6-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="42af6-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="42af6-123">-KeyspaceName</span></span>
<span data-ttu-id="42af6-124">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="42af6-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="42af6-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="42af6-125">-Name</span></span>
<span data-ttu-id="42af6-126">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="42af6-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="42af6-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="42af6-127">-ParentObject</span></span>
<span data-ttu-id="42af6-128">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="42af6-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="42af6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42af6-129">-ResourceGroupName</span></span>
<span data-ttu-id="42af6-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="42af6-130">Name of resource group.</span></span>

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

### <span data-ttu-id="42af6-131">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="42af6-131">-Throughput</span></span>
<span data-ttu-id="42af6-132">Genomflödet av Cassandra-tecken (RU/s).</span><span class="sxs-lookup"><span data-stu-id="42af6-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="42af6-133">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="42af6-133">Default value is 400.</span></span>

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

### <span data-ttu-id="42af6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42af6-134">-WhatIf</span></span>
<span data-ttu-id="42af6-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42af6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42af6-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42af6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42af6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42af6-137">CommonParameters</span></span>
<span data-ttu-id="42af6-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42af6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42af6-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42af6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42af6-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42af6-140">INPUTS</span></span>

### <span data-ttu-id="42af6-141">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="42af6-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="42af6-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42af6-142">OUTPUTS</span></span>

### <span data-ttu-id="42af6-143">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="42af6-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="42af6-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42af6-144">NOTES</span></span>

## <span data-ttu-id="42af6-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42af6-145">RELATED LINKS</span></span>
