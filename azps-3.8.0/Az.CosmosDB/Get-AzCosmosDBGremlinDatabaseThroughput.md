---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 961ba3375c25098de32bf93b4559d9bfa6b8944d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091850"
---
# <span data-ttu-id="f6499-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="f6499-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="f6499-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6499-102">SYNOPSIS</span></span>
<span data-ttu-id="f6499-103">Hämtar data flödet i en CosmosDB Gremlin-databas.</span><span class="sxs-lookup"><span data-stu-id="f6499-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f6499-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6499-104">SYNTAX</span></span>

### <span data-ttu-id="f6499-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f6499-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6499-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6499-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6499-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6499-107">DESCRIPTION</span></span>
<span data-ttu-id="f6499-108">Cmdleten **Get-AzCosmosDBGremlinDatabaseThroughput** hämtar data flödet för en CosmosDB Gremlin-databas.</span><span class="sxs-lookup"><span data-stu-id="f6499-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f6499-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6499-109">EXAMPLES</span></span>

### <span data-ttu-id="f6499-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6499-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="f6499-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6499-111">PARAMETERS</span></span>

### <span data-ttu-id="f6499-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f6499-112">-AccountName</span></span>
<span data-ttu-id="f6499-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="f6499-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f6499-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6499-114">-DefaultProfile</span></span>
<span data-ttu-id="f6499-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6499-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6499-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6499-116">-InputObject</span></span>
<span data-ttu-id="f6499-117">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f6499-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6499-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6499-118">-Name</span></span>
<span data-ttu-id="f6499-119">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="f6499-119">Database name.</span></span>

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

### <span data-ttu-id="f6499-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6499-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6499-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f6499-121">Name of resource group.</span></span>

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

### <span data-ttu-id="f6499-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6499-122">CommonParameters</span></span>
<span data-ttu-id="f6499-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6499-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6499-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6499-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6499-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6499-125">INPUTS</span></span>

### <span data-ttu-id="f6499-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="f6499-126">None</span></span>

## <span data-ttu-id="f6499-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6499-127">OUTPUTS</span></span>

### <span data-ttu-id="f6499-128">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f6499-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f6499-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6499-129">NOTES</span></span>

## <span data-ttu-id="f6499-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6499-130">RELATED LINKS</span></span>
