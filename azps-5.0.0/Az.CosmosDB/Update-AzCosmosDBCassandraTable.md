---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321384"
---
# <span data-ttu-id="792fe-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="792fe-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="792fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="792fe-102">SYNOPSIS</span></span>
<span data-ttu-id="792fe-103">Uppdaterar CosmosDB Cassandra-tabellen.</span><span class="sxs-lookup"><span data-stu-id="792fe-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="792fe-104">Utför en klient uppdaterings åtgärd genom att läsa den befintliga tabellen.</span><span class="sxs-lookup"><span data-stu-id="792fe-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="792fe-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="792fe-105">SYNTAX</span></span>

### <span data-ttu-id="792fe-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="792fe-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="792fe-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="792fe-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="792fe-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="792fe-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="792fe-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="792fe-109">DESCRIPTION</span></span>
<span data-ttu-id="792fe-110">Uppdaterar CosmosDB Cassandra-tabellen.</span><span class="sxs-lookup"><span data-stu-id="792fe-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="792fe-111">Utför en klient uppdaterings åtgärd genom att läsa den befintliga tabellen.</span><span class="sxs-lookup"><span data-stu-id="792fe-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="792fe-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="792fe-112">EXAMPLES</span></span>

### <span data-ttu-id="792fe-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="792fe-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="792fe-114">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="792fe-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="792fe-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="792fe-115">PARAMETERS</span></span>

### <span data-ttu-id="792fe-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="792fe-116">-AccountName</span></span>
<span data-ttu-id="792fe-117">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="792fe-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="792fe-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="792fe-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="792fe-119">TTL för analys lagring.</span><span class="sxs-lookup"><span data-stu-id="792fe-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="792fe-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="792fe-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="792fe-121">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="792fe-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="792fe-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="792fe-122">-Confirm</span></span>
<span data-ttu-id="792fe-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="792fe-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="792fe-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792fe-124">-DefaultProfile</span></span>
<span data-ttu-id="792fe-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="792fe-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792fe-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="792fe-126">-InputObject</span></span>
<span data-ttu-id="792fe-127">Cassandra.</span><span class="sxs-lookup"><span data-stu-id="792fe-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="792fe-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="792fe-128">-KeyspaceName</span></span>
<span data-ttu-id="792fe-129">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="792fe-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="792fe-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="792fe-130">-Name</span></span>
<span data-ttu-id="792fe-131">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="792fe-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="792fe-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="792fe-132">-ParentObject</span></span>
<span data-ttu-id="792fe-133">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="792fe-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="792fe-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="792fe-134">-ResourceGroupName</span></span>
<span data-ttu-id="792fe-135">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="792fe-135">Name of resource group.</span></span>

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

### <span data-ttu-id="792fe-136">– Schema</span><span class="sxs-lookup"><span data-stu-id="792fe-136">-Schema</span></span>
<span data-ttu-id="792fe-137">PSCassandraSchema-objekt.</span><span class="sxs-lookup"><span data-stu-id="792fe-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="792fe-138">Använd New-AzCosmosDBCassandraSchema för att skapa det här objektet.</span><span class="sxs-lookup"><span data-stu-id="792fe-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="792fe-139">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="792fe-139">-Throughput</span></span>
<span data-ttu-id="792fe-140">Genomflödet av Cassandra-tecken (RU/s).</span><span class="sxs-lookup"><span data-stu-id="792fe-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="792fe-141">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="792fe-141">Default value is 400.</span></span>

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

### <span data-ttu-id="792fe-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="792fe-142">-TtlInSeconds</span></span>
<span data-ttu-id="792fe-143">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="792fe-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="792fe-144">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="792fe-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="792fe-145">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="792fe-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="792fe-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="792fe-146">-WhatIf</span></span>
<span data-ttu-id="792fe-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="792fe-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="792fe-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="792fe-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="792fe-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792fe-149">CommonParameters</span></span>
<span data-ttu-id="792fe-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="792fe-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792fe-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="792fe-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792fe-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="792fe-152">INPUTS</span></span>

### <span data-ttu-id="792fe-153">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="792fe-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="792fe-154">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="792fe-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="792fe-155">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="792fe-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="792fe-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="792fe-156">OUTPUTS</span></span>

### <span data-ttu-id="792fe-157">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="792fe-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="792fe-158">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="792fe-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="792fe-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="792fe-159">NOTES</span></span>

## <span data-ttu-id="792fe-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="792fe-160">RELATED LINKS</span></span>
