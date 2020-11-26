---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260602"
---
# <span data-ttu-id="78fd9-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="78fd9-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="78fd9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="78fd9-103">Hämtar CosmosDB MongoDB-databasen</span><span class="sxs-lookup"><span data-stu-id="78fd9-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="78fd9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78fd9-104">SYNTAX</span></span>

### <span data-ttu-id="78fd9-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="78fd9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fd9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78fd9-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78fd9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78fd9-107">DESCRIPTION</span></span>
<span data-ttu-id="78fd9-108">Cmdleten **Get-AzCosmosDBMongoDBDatabase** hämtar databasen CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="78fd9-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="78fd9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78fd9-109">EXAMPLES</span></span>

### <span data-ttu-id="78fd9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="78fd9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="78fd9-111">Resource-objekt innehåller _rid, _ts, _etag egenskaper.</span><span class="sxs-lookup"><span data-stu-id="78fd9-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="78fd9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78fd9-112">PARAMETERS</span></span>

### <span data-ttu-id="78fd9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78fd9-113">-AccountName</span></span>
<span data-ttu-id="78fd9-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="78fd9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="78fd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fd9-115">-DefaultProfile</span></span>
<span data-ttu-id="78fd9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78fd9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78fd9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="78fd9-117">-Name</span></span>
<span data-ttu-id="78fd9-118">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="78fd9-118">Database name.</span></span>

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

### <span data-ttu-id="78fd9-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="78fd9-119">-ParentObject</span></span>
<span data-ttu-id="78fd9-120">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="78fd9-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78fd9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78fd9-121">-ResourceGroupName</span></span>
<span data-ttu-id="78fd9-122">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="78fd9-122">Name of resource group.</span></span>

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

### <span data-ttu-id="78fd9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fd9-123">CommonParameters</span></span>
<span data-ttu-id="78fd9-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78fd9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fd9-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78fd9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fd9-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78fd9-126">INPUTS</span></span>

### <span data-ttu-id="78fd9-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="78fd9-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="78fd9-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78fd9-128">OUTPUTS</span></span>

### <span data-ttu-id="78fd9-129">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="78fd9-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="78fd9-130">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="78fd9-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="78fd9-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78fd9-131">NOTES</span></span>

## <span data-ttu-id="78fd9-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78fd9-132">RELATED LINKS</span></span>