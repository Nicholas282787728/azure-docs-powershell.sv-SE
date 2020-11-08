---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 623ed0391ba36722cce26a42f1dd3d820cbd49f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091846"
---
# <span data-ttu-id="41e42-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="41e42-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="41e42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41e42-102">SYNOPSIS</span></span>
<span data-ttu-id="41e42-103">Hämtar CosmosDB MongoDB-samlingen.</span><span class="sxs-lookup"><span data-stu-id="41e42-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="41e42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41e42-104">SYNTAX</span></span>

### <span data-ttu-id="41e42-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="41e42-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="41e42-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41e42-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41e42-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41e42-107">DESCRIPTION</span></span>
<span data-ttu-id="41e42-108">Cmdleten **Get-AzCosmosDBMongoDBCollection** hämtar CosmosDB MongoDB-samlingen.</span><span class="sxs-lookup"><span data-stu-id="41e42-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="41e42-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41e42-109">EXAMPLES</span></span>

### <span data-ttu-id="41e42-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="41e42-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="41e42-111">Resurs objekt innehåller MongoIndexes, _rid _ts _etag egenskaper.</span><span class="sxs-lookup"><span data-stu-id="41e42-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="41e42-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41e42-112">PARAMETERS</span></span>

### <span data-ttu-id="41e42-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="41e42-113">-AccountName</span></span>
<span data-ttu-id="41e42-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="41e42-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="41e42-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="41e42-115">-DatabaseName</span></span>
<span data-ttu-id="41e42-116">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="41e42-116">Database name.</span></span>

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

### <span data-ttu-id="41e42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e42-117">-DefaultProfile</span></span>
<span data-ttu-id="41e42-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41e42-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41e42-119">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="41e42-119">-Detailed</span></span>
<span data-ttu-id="41e42-120">Om den anges returnerar cmdleten samlingen med motsvarande genomflöde-värde.</span><span class="sxs-lookup"><span data-stu-id="41e42-120">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e42-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41e42-121">-InputObject</span></span>
<span data-ttu-id="41e42-122">Mongo.</span><span class="sxs-lookup"><span data-stu-id="41e42-122">Mongo Database object.</span></span>

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

### <span data-ttu-id="41e42-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="41e42-123">-Name</span></span>
<span data-ttu-id="41e42-124">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="41e42-124">Collection name.</span></span>

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

### <span data-ttu-id="41e42-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e42-125">-ResourceGroupName</span></span>
<span data-ttu-id="41e42-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="41e42-126">Name of resource group.</span></span>

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

### <span data-ttu-id="41e42-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e42-127">CommonParameters</span></span>
<span data-ttu-id="41e42-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e42-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e42-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41e42-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e42-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41e42-130">INPUTS</span></span>

### <span data-ttu-id="41e42-131">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="41e42-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="41e42-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41e42-132">OUTPUTS</span></span>

### <span data-ttu-id="41e42-133">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="41e42-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="41e42-134">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="41e42-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="41e42-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41e42-135">NOTES</span></span>

## <span data-ttu-id="41e42-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41e42-136">RELATED LINKS</span></span>
