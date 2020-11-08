---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092165"
---
# <span data-ttu-id="c7cb6-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="c7cb6-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="c7cb6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="c7cb6-103">Anger tabellen CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="c7cb6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7cb6-104">SYNTAX</span></span>

### <span data-ttu-id="c7cb6-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c7cb6-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7cb6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7cb6-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7cb6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7cb6-107">DESCRIPTION</span></span>
<span data-ttu-id="c7cb6-108">Cmdleten **set-AzCosmosDBCassandraTable** anger CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="c7cb6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7cb6-109">EXAMPLES</span></span>

### <span data-ttu-id="c7cb6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7cb6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="c7cb6-111">Resurs objekt innehåller värdena för _rid, _ts, _etag, DefaultTtl och schema egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="c7cb6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7cb6-112">PARAMETERS</span></span>

### <span data-ttu-id="c7cb6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c7cb6-113">-AccountName</span></span>
<span data-ttu-id="c7cb6-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c7cb6-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7cb6-115">-Confirm</span></span>
<span data-ttu-id="c7cb6-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7cb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7cb6-117">-DefaultProfile</span></span>
<span data-ttu-id="c7cb6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7cb6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7cb6-119">-InputObject</span></span>
<span data-ttu-id="c7cb6-120">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c7cb6-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="c7cb6-121">-KeyspaceName</span></span>
<span data-ttu-id="c7cb6-122">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c7cb6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7cb6-123">-Name</span></span>
<span data-ttu-id="c7cb6-124">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="c7cb6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7cb6-125">-ResourceGroupName</span></span>
<span data-ttu-id="c7cb6-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-126">Name of resource group.</span></span>

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

### <span data-ttu-id="c7cb6-127">– Schema</span><span class="sxs-lookup"><span data-stu-id="c7cb6-127">-Schema</span></span>
<span data-ttu-id="c7cb6-128">PSCassandraSchema-objekt.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="c7cb6-129">Använd New-AzCosmosDBCassandraSchema för att skapa det här objektet.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7cb6-130">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="c7cb6-130">-Throughput</span></span>
<span data-ttu-id="c7cb6-131">Genomflödet av Cassandra-tecken (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c7cb6-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="c7cb6-132">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-132">Default value is 400.</span></span>

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

### <span data-ttu-id="c7cb6-133">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c7cb6-133">-TtlInSeconds</span></span>
<span data-ttu-id="c7cb6-134">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="c7cb6-135">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="c7cb6-136">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="c7cb6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7cb6-137">-WhatIf</span></span>
<span data-ttu-id="c7cb6-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7cb6-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7cb6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7cb6-140">CommonParameters</span></span>
<span data-ttu-id="c7cb6-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7cb6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7cb6-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7cb6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7cb6-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7cb6-143">INPUTS</span></span>

### <span data-ttu-id="c7cb6-144">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="c7cb6-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="c7cb6-145">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c7cb6-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="c7cb6-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7cb6-146">OUTPUTS</span></span>

### <span data-ttu-id="c7cb6-147">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="c7cb6-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="c7cb6-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7cb6-148">NOTES</span></span>

## <span data-ttu-id="c7cb6-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7cb6-149">RELATED LINKS</span></span>
