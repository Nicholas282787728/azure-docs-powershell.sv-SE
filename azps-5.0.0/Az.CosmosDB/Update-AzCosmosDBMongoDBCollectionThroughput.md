---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321359"
---
# <span data-ttu-id="1993a-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="1993a-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="1993a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1993a-102">SYNOPSIS</span></span>
<span data-ttu-id="1993a-103">Uppdaterar genomflödet för en CosmosDB MongoDB-samling.</span><span class="sxs-lookup"><span data-stu-id="1993a-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="1993a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1993a-104">SYNTAX</span></span>

### <span data-ttu-id="1993a-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1993a-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1993a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1993a-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1993a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1993a-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1993a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1993a-108">DESCRIPTION</span></span>
<span data-ttu-id="1993a-109">Uppdaterar genomflödet för en CosmosDB MongoDB-samling.</span><span class="sxs-lookup"><span data-stu-id="1993a-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="1993a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1993a-110">EXAMPLES</span></span>

### <span data-ttu-id="1993a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1993a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="1993a-112">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="1993a-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="1993a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1993a-113">PARAMETERS</span></span>

### <span data-ttu-id="1993a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1993a-114">-AccountName</span></span>
<span data-ttu-id="1993a-115">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="1993a-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1993a-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1993a-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1993a-117">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="1993a-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1993a-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1993a-118">-Confirm</span></span>
<span data-ttu-id="1993a-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1993a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1993a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1993a-120">-DatabaseName</span></span>
<span data-ttu-id="1993a-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="1993a-121">Database name.</span></span>

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

### <span data-ttu-id="1993a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1993a-122">-DefaultProfile</span></span>
<span data-ttu-id="1993a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1993a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1993a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1993a-124">-InputObject</span></span>
<span data-ttu-id="1993a-125">Mongo.</span><span class="sxs-lookup"><span data-stu-id="1993a-125">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1993a-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="1993a-126">-Name</span></span>
<span data-ttu-id="1993a-127">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="1993a-127">Collection name.</span></span>

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

### <span data-ttu-id="1993a-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1993a-128">-ParentObject</span></span>
<span data-ttu-id="1993a-129">Mongo.</span><span class="sxs-lookup"><span data-stu-id="1993a-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1993a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1993a-130">-ResourceGroupName</span></span>
<span data-ttu-id="1993a-131">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1993a-131">Name of resource group.</span></span>

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

### <span data-ttu-id="1993a-132">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="1993a-132">-Throughput</span></span>
<span data-ttu-id="1993a-133">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1993a-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="1993a-134">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="1993a-134">Default value is 400.</span></span>

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

### <span data-ttu-id="1993a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1993a-135">-WhatIf</span></span>
<span data-ttu-id="1993a-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1993a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1993a-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1993a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1993a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1993a-138">CommonParameters</span></span>
<span data-ttu-id="1993a-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1993a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1993a-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1993a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1993a-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1993a-141">INPUTS</span></span>

### <span data-ttu-id="1993a-142">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1993a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="1993a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1993a-143">OUTPUTS</span></span>

### <span data-ttu-id="1993a-144">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1993a-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1993a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1993a-145">NOTES</span></span>

## <span data-ttu-id="1993a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1993a-146">RELATED LINKS</span></span>
