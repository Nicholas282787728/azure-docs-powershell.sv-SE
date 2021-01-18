---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526448"
---
# <span data-ttu-id="3e638-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="3e638-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="3e638-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e638-102">SYNOPSIS</span></span>
<span data-ttu-id="3e638-103">Skapar ett nytt CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="3e638-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="3e638-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e638-104">SYNTAX</span></span>

### <span data-ttu-id="3e638-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3e638-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e638-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e638-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e638-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e638-107">DESCRIPTION</span></span>
<span data-ttu-id="3e638-108">Skapar ett nytt CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="3e638-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="3e638-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e638-109">EXAMPLES</span></span>

### <span data-ttu-id="3e638-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e638-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="3e638-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e638-111">PARAMETERS</span></span>

### <span data-ttu-id="3e638-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e638-112">-AccountName</span></span>
<span data-ttu-id="3e638-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="3e638-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3e638-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="3e638-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="3e638-115">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="3e638-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="3e638-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e638-116">-Confirm</span></span>
<span data-ttu-id="3e638-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e638-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e638-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e638-118">-DefaultProfile</span></span>
<span data-ttu-id="3e638-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e638-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e638-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e638-120">-Name</span></span>
<span data-ttu-id="3e638-121">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="3e638-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="3e638-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3e638-122">-ParentObject</span></span>
<span data-ttu-id="3e638-123">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="3e638-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3e638-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e638-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e638-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3e638-125">Name of resource group.</span></span>

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

### <span data-ttu-id="3e638-126">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="3e638-126">-Throughput</span></span>
<span data-ttu-id="3e638-127">Genomflödet av Cassandra-tecken (RU/s).</span><span class="sxs-lookup"><span data-stu-id="3e638-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="3e638-128">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="3e638-128">Default value is 400.</span></span>

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

### <span data-ttu-id="3e638-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e638-129">-WhatIf</span></span>
<span data-ttu-id="3e638-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e638-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e638-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e638-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e638-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e638-132">CommonParameters</span></span>
<span data-ttu-id="3e638-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e638-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e638-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e638-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e638-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e638-135">INPUTS</span></span>

### <span data-ttu-id="3e638-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="3e638-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="3e638-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e638-137">OUTPUTS</span></span>

### <span data-ttu-id="3e638-138">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="3e638-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="3e638-139">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="3e638-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="3e638-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e638-140">NOTES</span></span>

## <span data-ttu-id="3e638-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e638-141">RELATED LINKS</span></span>
