---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260110"
---
# <span data-ttu-id="0b042-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="0b042-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="0b042-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b042-102">SYNOPSIS</span></span>
<span data-ttu-id="0b042-103">Skapar en ny CosmosDB Cassandra-tabell.</span><span class="sxs-lookup"><span data-stu-id="0b042-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="0b042-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b042-104">SYNTAX</span></span>

### <span data-ttu-id="0b042-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0b042-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b042-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b042-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b042-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b042-107">DESCRIPTION</span></span>
<span data-ttu-id="0b042-108">Skapar en ny CosmosDB Cassandra-tabell.</span><span class="sxs-lookup"><span data-stu-id="0b042-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="0b042-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b042-109">EXAMPLES</span></span>

### <span data-ttu-id="0b042-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0b042-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="0b042-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b042-111">PARAMETERS</span></span>

### <span data-ttu-id="0b042-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b042-112">-AccountName</span></span>
<span data-ttu-id="0b042-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="0b042-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0b042-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="0b042-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="0b042-115">TTL för analys lagring.</span><span class="sxs-lookup"><span data-stu-id="0b042-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="0b042-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0b042-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0b042-117">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="0b042-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0b042-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b042-118">-Confirm</span></span>
<span data-ttu-id="0b042-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b042-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b042-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b042-120">-DefaultProfile</span></span>
<span data-ttu-id="0b042-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b042-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b042-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="0b042-122">-KeyspaceName</span></span>
<span data-ttu-id="0b042-123">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="0b042-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0b042-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="0b042-124">-Name</span></span>
<span data-ttu-id="0b042-125">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="0b042-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="0b042-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0b042-126">-ParentObject</span></span>
<span data-ttu-id="0b042-127">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="0b042-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="0b042-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b042-128">-ResourceGroupName</span></span>
<span data-ttu-id="0b042-129">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0b042-129">Name of resource group.</span></span>

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

### <span data-ttu-id="0b042-130">– Schema</span><span class="sxs-lookup"><span data-stu-id="0b042-130">-Schema</span></span>
<span data-ttu-id="0b042-131">PSCassandraSchema-objekt.</span><span class="sxs-lookup"><span data-stu-id="0b042-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="0b042-132">Använd New-AzCosmosDBCassandraSchema för att skapa det här objektet.</span><span class="sxs-lookup"><span data-stu-id="0b042-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="0b042-133">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="0b042-133">-Throughput</span></span>
<span data-ttu-id="0b042-134">Genomflödet av Cassandra-tecken (RU/s).</span><span class="sxs-lookup"><span data-stu-id="0b042-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="0b042-135">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="0b042-135">Default value is 400.</span></span>

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

### <span data-ttu-id="0b042-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="0b042-136">-TtlInSeconds</span></span>
<span data-ttu-id="0b042-137">Standard-TTL i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0b042-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="0b042-138">Om värdet saknas eller är-1 går det inte att utgå från objekt.</span><span class="sxs-lookup"><span data-stu-id="0b042-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="0b042-139">Om värdet är inställt på n kommer artiklar att gå ut n sekunder efter den senaste ändringen.</span><span class="sxs-lookup"><span data-stu-id="0b042-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="0b042-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b042-140">-WhatIf</span></span>
<span data-ttu-id="0b042-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b042-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b042-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b042-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b042-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b042-143">CommonParameters</span></span>
<span data-ttu-id="0b042-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b042-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b042-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b042-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b042-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b042-146">INPUTS</span></span>

### <span data-ttu-id="0b042-147">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="0b042-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="0b042-148">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0b042-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="0b042-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b042-149">OUTPUTS</span></span>

### <span data-ttu-id="0b042-150">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="0b042-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="0b042-151">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="0b042-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="0b042-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b042-152">NOTES</span></span>

## <span data-ttu-id="0b042-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b042-153">RELATED LINKS</span></span>
