---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260098"
---
# <span data-ttu-id="d1897-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="d1897-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="d1897-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1897-102">SYNOPSIS</span></span>
<span data-ttu-id="d1897-103">Uppdaterar CosmosDB Cassandra-tecken.</span><span class="sxs-lookup"><span data-stu-id="d1897-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="d1897-104">Utför en klient uppdaterings åtgärd genom att läsa det befintliga.</span><span class="sxs-lookup"><span data-stu-id="d1897-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="d1897-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1897-105">SYNTAX</span></span>

### <span data-ttu-id="d1897-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d1897-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1897-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1897-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1897-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1897-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1897-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1897-109">DESCRIPTION</span></span>
<span data-ttu-id="d1897-110">Uppdaterar CosmosDB Cassandra-tecken.</span><span class="sxs-lookup"><span data-stu-id="d1897-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="d1897-111">Utför en klient uppdaterings åtgärd genom att läsa det befintliga.</span><span class="sxs-lookup"><span data-stu-id="d1897-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="d1897-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1897-112">EXAMPLES</span></span>

### <span data-ttu-id="d1897-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1897-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="d1897-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1897-114">PARAMETERS</span></span>

### <span data-ttu-id="d1897-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d1897-115">-AccountName</span></span>
<span data-ttu-id="d1897-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="d1897-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d1897-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d1897-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d1897-118">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="d1897-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d1897-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1897-119">-Confirm</span></span>
<span data-ttu-id="d1897-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1897-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1897-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1897-121">-DefaultProfile</span></span>
<span data-ttu-id="d1897-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1897-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1897-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1897-123">-InputObject</span></span>
<span data-ttu-id="d1897-124">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="d1897-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="d1897-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1897-125">-Name</span></span>
<span data-ttu-id="d1897-126">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="d1897-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d1897-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1897-127">-ParentObject</span></span>
<span data-ttu-id="d1897-128">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d1897-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d1897-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1897-129">-ResourceGroupName</span></span>
<span data-ttu-id="d1897-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d1897-130">Name of resource group.</span></span>

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

### <span data-ttu-id="d1897-131">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="d1897-131">-Throughput</span></span>
<span data-ttu-id="d1897-132">Genomflödet av Cassandra-tecken (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d1897-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="d1897-133">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="d1897-133">Default value is 400.</span></span>

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

### <span data-ttu-id="d1897-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1897-134">-WhatIf</span></span>
<span data-ttu-id="d1897-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1897-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1897-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1897-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1897-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1897-137">CommonParameters</span></span>
<span data-ttu-id="d1897-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1897-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1897-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1897-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1897-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1897-140">INPUTS</span></span>

### <span data-ttu-id="d1897-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d1897-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="d1897-142">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="d1897-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="d1897-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1897-143">OUTPUTS</span></span>

### <span data-ttu-id="d1897-144">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="d1897-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="d1897-145">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d1897-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d1897-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1897-146">NOTES</span></span>

## <span data-ttu-id="d1897-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1897-147">RELATED LINKS</span></span>
