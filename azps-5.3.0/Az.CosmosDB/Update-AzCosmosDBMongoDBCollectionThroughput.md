---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524297"
---
# <span data-ttu-id="184c0-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="184c0-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="184c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="184c0-102">SYNOPSIS</span></span>
<span data-ttu-id="184c0-103">Uppdaterar genomflödet för en CosmosDB MongoDB-samling.</span><span class="sxs-lookup"><span data-stu-id="184c0-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="184c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="184c0-104">SYNTAX</span></span>

### <span data-ttu-id="184c0-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="184c0-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184c0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="184c0-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184c0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="184c0-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="184c0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="184c0-108">DESCRIPTION</span></span>
<span data-ttu-id="184c0-109">Uppdaterar genomflödet för en CosmosDB MongoDB-samling.</span><span class="sxs-lookup"><span data-stu-id="184c0-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="184c0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="184c0-110">EXAMPLES</span></span>

### <span data-ttu-id="184c0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="184c0-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="184c0-112">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="184c0-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="184c0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="184c0-113">PARAMETERS</span></span>

### <span data-ttu-id="184c0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="184c0-114">-AccountName</span></span>
<span data-ttu-id="184c0-115">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="184c0-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="184c0-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="184c0-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="184c0-117">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="184c0-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="184c0-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="184c0-118">-Confirm</span></span>
<span data-ttu-id="184c0-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="184c0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="184c0-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="184c0-120">-DatabaseName</span></span>
<span data-ttu-id="184c0-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="184c0-121">Database name.</span></span>

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

### <span data-ttu-id="184c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184c0-122">-DefaultProfile</span></span>
<span data-ttu-id="184c0-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="184c0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="184c0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="184c0-124">-InputObject</span></span>
<span data-ttu-id="184c0-125">Mongo.</span><span class="sxs-lookup"><span data-stu-id="184c0-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="184c0-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="184c0-126">-Name</span></span>
<span data-ttu-id="184c0-127">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="184c0-127">Collection name.</span></span>

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

### <span data-ttu-id="184c0-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="184c0-128">-ParentObject</span></span>
<span data-ttu-id="184c0-129">Mongo.</span><span class="sxs-lookup"><span data-stu-id="184c0-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="184c0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="184c0-130">-ResourceGroupName</span></span>
<span data-ttu-id="184c0-131">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="184c0-131">Name of resource group.</span></span>

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

### <span data-ttu-id="184c0-132">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="184c0-132">-Throughput</span></span>
<span data-ttu-id="184c0-133">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="184c0-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="184c0-134">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="184c0-134">Default value is 400.</span></span>

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

### <span data-ttu-id="184c0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="184c0-135">-WhatIf</span></span>
<span data-ttu-id="184c0-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="184c0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="184c0-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="184c0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="184c0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184c0-138">CommonParameters</span></span>
<span data-ttu-id="184c0-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="184c0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184c0-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="184c0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184c0-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="184c0-141">INPUTS</span></span>

### <span data-ttu-id="184c0-142">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="184c0-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="184c0-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="184c0-143">OUTPUTS</span></span>

### <span data-ttu-id="184c0-144">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="184c0-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="184c0-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="184c0-145">NOTES</span></span>

## <span data-ttu-id="184c0-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="184c0-146">RELATED LINKS</span></span>
