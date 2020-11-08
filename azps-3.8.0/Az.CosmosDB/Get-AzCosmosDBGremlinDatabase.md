---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091851"
---
# <span data-ttu-id="1ecd2-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="1ecd2-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="1ecd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ecd2-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecd2-103">Hämtar CosmosDB Gremlin-databasen.</span><span class="sxs-lookup"><span data-stu-id="1ecd2-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="1ecd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ecd2-104">SYNTAX</span></span>

### <span data-ttu-id="1ecd2-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1ecd2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ecd2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ecd2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ecd2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ecd2-107">DESCRIPTION</span></span>
<span data-ttu-id="1ecd2-108">Cmdleten **Get-AzCosmosDBGremlinDatabase** hämtar databasen CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="1ecd2-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="1ecd2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ecd2-109">EXAMPLES</span></span>

### <span data-ttu-id="1ecd2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1ecd2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="1ecd2-111">Resource-objekt innehåller _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="1ecd2-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="1ecd2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ecd2-112">PARAMETERS</span></span>

### <span data-ttu-id="1ecd2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ecd2-113">-AccountName</span></span>
<span data-ttu-id="1ecd2-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="1ecd2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1ecd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecd2-115">-DefaultProfile</span></span>
<span data-ttu-id="1ecd2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ecd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ecd2-117">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="1ecd2-117">-Detailed</span></span>
<span data-ttu-id="1ecd2-118">Om den anges returnerar cmdleten databasen med motsvarande genomflöde-värde.</span><span class="sxs-lookup"><span data-stu-id="1ecd2-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="1ecd2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ecd2-119">-InputObject</span></span>
<span data-ttu-id="1ecd2-120">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1ecd2-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecd2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ecd2-121">-Name</span></span>
<span data-ttu-id="1ecd2-122">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="1ecd2-122">Database name.</span></span>

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

### <span data-ttu-id="1ecd2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ecd2-123">-ResourceGroupName</span></span>
<span data-ttu-id="1ecd2-124">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1ecd2-124">Name of resource group.</span></span>

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

### <span data-ttu-id="1ecd2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecd2-125">CommonParameters</span></span>
<span data-ttu-id="1ecd2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ecd2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecd2-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ecd2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecd2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ecd2-128">INPUTS</span></span>

### <span data-ttu-id="1ecd2-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1ecd2-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1ecd2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ecd2-130">OUTPUTS</span></span>

### <span data-ttu-id="1ecd2-131">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1ecd2-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="1ecd2-132">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1ecd2-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1ecd2-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ecd2-133">NOTES</span></span>

## <span data-ttu-id="1ecd2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ecd2-134">RELATED LINKS</span></span>
