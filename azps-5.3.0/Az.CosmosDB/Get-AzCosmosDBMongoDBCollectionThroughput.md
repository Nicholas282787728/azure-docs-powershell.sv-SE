---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524377"
---
# <span data-ttu-id="51e03-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="51e03-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="51e03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51e03-102">SYNOPSIS</span></span>
<span data-ttu-id="51e03-103">Hämtar CosmosDB genomflöde-egenskaper för MongoDB-samlingen.</span><span class="sxs-lookup"><span data-stu-id="51e03-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="51e03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51e03-104">SYNTAX</span></span>

### <span data-ttu-id="51e03-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51e03-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51e03-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51e03-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51e03-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51e03-107">DESCRIPTION</span></span>
<span data-ttu-id="51e03-108">Cmdleten **Get-AzCosmosDBMongoDBCollectionThroughput** hämtar genomflödet-egenskaperna för MongoDB-samlingen.</span><span class="sxs-lookup"><span data-stu-id="51e03-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="51e03-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51e03-109">EXAMPLES</span></span>

### <span data-ttu-id="51e03-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51e03-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="51e03-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51e03-111">PARAMETERS</span></span>

### <span data-ttu-id="51e03-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="51e03-112">-AccountName</span></span>
<span data-ttu-id="51e03-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="51e03-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="51e03-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51e03-114">-Confirm</span></span>
<span data-ttu-id="51e03-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51e03-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e03-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="51e03-116">-DatabaseName</span></span>
<span data-ttu-id="51e03-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="51e03-117">Database name.</span></span>

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

### <span data-ttu-id="51e03-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e03-118">-DefaultProfile</span></span>
<span data-ttu-id="51e03-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51e03-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51e03-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51e03-120">-InputObject</span></span>
<span data-ttu-id="51e03-121">Om den anges returnerar cmdleten samlingen med motsvarande genomflöde-värde.</span><span class="sxs-lookup"><span data-stu-id="51e03-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51e03-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="51e03-122">-Name</span></span>
<span data-ttu-id="51e03-123">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="51e03-123">Collection name.</span></span>

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

### <span data-ttu-id="51e03-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e03-124">-ResourceGroupName</span></span>
<span data-ttu-id="51e03-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51e03-125">Name of resource group.</span></span>

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

### <span data-ttu-id="51e03-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e03-126">-WhatIf</span></span>
<span data-ttu-id="51e03-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51e03-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e03-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51e03-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e03-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e03-129">CommonParameters</span></span>
<span data-ttu-id="51e03-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e03-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e03-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51e03-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e03-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51e03-132">INPUTS</span></span>

### <span data-ttu-id="51e03-133">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="51e03-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="51e03-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51e03-134">OUTPUTS</span></span>

### <span data-ttu-id="51e03-135">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="51e03-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="51e03-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51e03-136">NOTES</span></span>

## <span data-ttu-id="51e03-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51e03-137">RELATED LINKS</span></span>
