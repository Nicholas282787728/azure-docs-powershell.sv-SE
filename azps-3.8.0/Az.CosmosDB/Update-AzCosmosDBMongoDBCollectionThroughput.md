---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 605998d6bc5ae8b647b3644dc71b8063f0881910
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089910"
---
# <span data-ttu-id="c2302-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="c2302-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="c2302-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2302-102">SYNOPSIS</span></span>
<span data-ttu-id="c2302-103">Uppdaterar genomflödet för en CosmosDB MongoDB-samling.</span><span class="sxs-lookup"><span data-stu-id="c2302-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="c2302-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2302-104">SYNTAX</span></span>

### <span data-ttu-id="c2302-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c2302-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2302-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2302-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2302-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2302-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2302-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2302-108">EXAMPLES</span></span>

### <span data-ttu-id="c2302-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2302-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="c2302-110">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="c2302-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="c2302-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2302-111">PARAMETERS</span></span>

### <span data-ttu-id="c2302-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2302-112">-AccountName</span></span>
<span data-ttu-id="c2302-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="c2302-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2302-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2302-114">-Confirm</span></span>
<span data-ttu-id="c2302-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2302-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2302-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2302-116">-DatabaseName</span></span>
<span data-ttu-id="c2302-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="c2302-117">Database name.</span></span>

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

### <span data-ttu-id="c2302-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2302-118">-DefaultProfile</span></span>
<span data-ttu-id="c2302-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2302-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2302-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2302-120">-InputObject</span></span>
<span data-ttu-id="c2302-121">Mongo.</span><span class="sxs-lookup"><span data-stu-id="c2302-121">Mongo Database object.</span></span>

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

### <span data-ttu-id="c2302-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2302-122">-Name</span></span>
<span data-ttu-id="c2302-123">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="c2302-123">Collection name.</span></span>

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

### <span data-ttu-id="c2302-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2302-124">-ParentObject</span></span>
<span data-ttu-id="c2302-125">Mongo.</span><span class="sxs-lookup"><span data-stu-id="c2302-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="c2302-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2302-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2302-127">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c2302-127">Name of resource group.</span></span>

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

### <span data-ttu-id="c2302-128">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="c2302-128">-Throughput</span></span>
<span data-ttu-id="c2302-129">Genomflödet i SQL-behållare (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c2302-129">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="c2302-130">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="c2302-130">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2302-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2302-131">-WhatIf</span></span>
<span data-ttu-id="c2302-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2302-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2302-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2302-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2302-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2302-134">CommonParameters</span></span>
<span data-ttu-id="c2302-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2302-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2302-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2302-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2302-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2302-137">INPUTS</span></span>

### <span data-ttu-id="c2302-138">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c2302-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="c2302-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2302-139">OUTPUTS</span></span>

### <span data-ttu-id="c2302-140">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c2302-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c2302-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2302-141">NOTES</span></span>

## <span data-ttu-id="c2302-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2302-142">RELATED LINKS</span></span>