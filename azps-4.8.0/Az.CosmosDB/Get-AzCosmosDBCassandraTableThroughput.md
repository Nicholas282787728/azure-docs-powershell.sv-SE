---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260295"
---
# <span data-ttu-id="fc256-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="fc256-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="fc256-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc256-102">SYNOPSIS</span></span>
<span data-ttu-id="fc256-103">Hämtar värdet för data flödet i Cassandra-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fc256-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="fc256-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc256-104">SYNTAX</span></span>

### <span data-ttu-id="fc256-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fc256-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc256-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc256-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc256-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc256-107">DESCRIPTION</span></span>
<span data-ttu-id="fc256-108">Cmdleten **Get-AzCosmosDBCassandraTableThroughput** hämtar det genomflöde-objekt som motsvarar ett givet tecken.</span><span class="sxs-lookup"><span data-stu-id="fc256-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="fc256-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc256-109">EXAMPLES</span></span>

### <span data-ttu-id="fc256-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fc256-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="fc256-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc256-111">PARAMETERS</span></span>

### <span data-ttu-id="fc256-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc256-112">-AccountName</span></span>
<span data-ttu-id="fc256-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="fc256-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fc256-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc256-114">-Confirm</span></span>
<span data-ttu-id="fc256-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc256-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc256-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc256-116">-DefaultProfile</span></span>
<span data-ttu-id="fc256-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc256-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc256-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc256-118">-InputObject</span></span>
<span data-ttu-id="fc256-119">Cassandra.</span><span class="sxs-lookup"><span data-stu-id="fc256-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="fc256-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="fc256-120">-KeyspaceName</span></span>
<span data-ttu-id="fc256-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="fc256-121">Database name.</span></span>

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

### <span data-ttu-id="fc256-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc256-122">-Name</span></span>
<span data-ttu-id="fc256-123">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="fc256-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="fc256-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc256-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc256-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fc256-125">Name of resource group.</span></span>

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

### <span data-ttu-id="fc256-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc256-126">-WhatIf</span></span>
<span data-ttu-id="fc256-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc256-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc256-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc256-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc256-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc256-129">CommonParameters</span></span>
<span data-ttu-id="fc256-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc256-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc256-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc256-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc256-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc256-132">INPUTS</span></span>

### <span data-ttu-id="fc256-133">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="fc256-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="fc256-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc256-134">OUTPUTS</span></span>

### <span data-ttu-id="fc256-135">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fc256-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fc256-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc256-136">NOTES</span></span>

## <span data-ttu-id="fc256-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc256-137">RELATED LINKS</span></span>
