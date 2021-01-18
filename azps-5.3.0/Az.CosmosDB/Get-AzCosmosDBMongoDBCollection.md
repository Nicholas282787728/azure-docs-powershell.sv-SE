---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526473"
---
# <span data-ttu-id="0e379-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="0e379-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="0e379-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e379-102">SYNOPSIS</span></span>
<span data-ttu-id="0e379-103">Hämtar CosmosDB MongoDB-samlingen.</span><span class="sxs-lookup"><span data-stu-id="0e379-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="0e379-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e379-104">SYNTAX</span></span>

### <span data-ttu-id="0e379-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0e379-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="0e379-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e379-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e379-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e379-107">DESCRIPTION</span></span>
<span data-ttu-id="0e379-108">Cmdleten **Get-AzCosmosDBMongoDBCollection** hämtar CosmosDB MongoDB-samlingen.</span><span class="sxs-lookup"><span data-stu-id="0e379-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="0e379-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e379-109">EXAMPLES</span></span>

### <span data-ttu-id="0e379-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e379-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="0e379-111">Resurs objekt innehåller MongoIndexes, _rid _ts _etag egenskaper.</span><span class="sxs-lookup"><span data-stu-id="0e379-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="0e379-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0e379-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="0e379-113">I det här exemplet hämtas ShardKey mängd</span><span class="sxs-lookup"><span data-stu-id="0e379-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="0e379-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e379-114">PARAMETERS</span></span>

### <span data-ttu-id="0e379-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0e379-115">-AccountName</span></span>
<span data-ttu-id="0e379-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="0e379-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0e379-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0e379-117">-DatabaseName</span></span>
<span data-ttu-id="0e379-118">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="0e379-118">Database name.</span></span>

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

### <span data-ttu-id="0e379-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e379-119">-DefaultProfile</span></span>
<span data-ttu-id="0e379-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e379-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e379-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e379-121">-Name</span></span>
<span data-ttu-id="0e379-122">Samlingens namn.</span><span class="sxs-lookup"><span data-stu-id="0e379-122">Collection name.</span></span>

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

### <span data-ttu-id="0e379-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0e379-123">-ParentObject</span></span>
<span data-ttu-id="0e379-124">Mongo.</span><span class="sxs-lookup"><span data-stu-id="0e379-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="0e379-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e379-125">-ResourceGroupName</span></span>
<span data-ttu-id="0e379-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0e379-126">Name of resource group.</span></span>

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

### <span data-ttu-id="0e379-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e379-127">CommonParameters</span></span>
<span data-ttu-id="0e379-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e379-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e379-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e379-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e379-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e379-130">INPUTS</span></span>

### <span data-ttu-id="0e379-131">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0e379-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="0e379-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e379-132">OUTPUTS</span></span>

### <span data-ttu-id="0e379-133">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="0e379-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="0e379-134">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0e379-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0e379-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e379-135">NOTES</span></span>

## <span data-ttu-id="0e379-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e379-136">RELATED LINKS</span></span>
