---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091852"
---
# <span data-ttu-id="02c50-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="02c50-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="02c50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02c50-102">SYNOPSIS</span></span>
<span data-ttu-id="02c50-103">Hämtar värdet för data flödet i Cassandra-tabellen.</span><span class="sxs-lookup"><span data-stu-id="02c50-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="02c50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02c50-104">SYNTAX</span></span>

### <span data-ttu-id="02c50-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="02c50-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c50-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c50-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c50-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02c50-107">DESCRIPTION</span></span>
<span data-ttu-id="02c50-108">Cmdleten **Get-AzCosmosDBCassandraTableThroughput** hämtar det genomflöde-objekt som motsvarar ett givet tecken.</span><span class="sxs-lookup"><span data-stu-id="02c50-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="02c50-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02c50-109">EXAMPLES</span></span>

### <span data-ttu-id="02c50-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="02c50-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="02c50-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02c50-111">PARAMETERS</span></span>

### <span data-ttu-id="02c50-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02c50-112">-AccountName</span></span>
<span data-ttu-id="02c50-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="02c50-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="02c50-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02c50-114">-Confirm</span></span>
<span data-ttu-id="02c50-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02c50-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c50-116">-DefaultProfile</span></span>
<span data-ttu-id="02c50-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02c50-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c50-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02c50-118">-InputObject</span></span>
<span data-ttu-id="02c50-119">Cassandra.</span><span class="sxs-lookup"><span data-stu-id="02c50-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="02c50-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="02c50-120">-KeyspaceName</span></span>
<span data-ttu-id="02c50-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="02c50-121">Database name.</span></span>

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

### <span data-ttu-id="02c50-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="02c50-122">-Name</span></span>
<span data-ttu-id="02c50-123">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="02c50-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="02c50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c50-124">-ResourceGroupName</span></span>
<span data-ttu-id="02c50-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="02c50-125">Name of resource group.</span></span>

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

### <span data-ttu-id="02c50-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c50-126">-WhatIf</span></span>
<span data-ttu-id="02c50-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02c50-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c50-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02c50-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c50-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c50-129">CommonParameters</span></span>
<span data-ttu-id="02c50-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c50-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c50-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02c50-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c50-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02c50-132">INPUTS</span></span>

### <span data-ttu-id="02c50-133">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="02c50-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="02c50-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02c50-134">OUTPUTS</span></span>

### <span data-ttu-id="02c50-135">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="02c50-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="02c50-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02c50-136">NOTES</span></span>

## <span data-ttu-id="02c50-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02c50-137">RELATED LINKS</span></span>