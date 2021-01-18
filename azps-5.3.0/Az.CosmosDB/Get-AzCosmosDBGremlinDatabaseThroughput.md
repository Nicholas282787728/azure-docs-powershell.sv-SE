---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 8905f4e4ffc4268b74ce57bfaf1bcb14565f70fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524382"
---
# <span data-ttu-id="e016a-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="e016a-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="e016a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e016a-102">SYNOPSIS</span></span>
<span data-ttu-id="e016a-103">Hämtar data flödet i en CosmosDB Gremlin-databas.</span><span class="sxs-lookup"><span data-stu-id="e016a-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e016a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e016a-104">SYNTAX</span></span>

### <span data-ttu-id="e016a-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e016a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e016a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e016a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e016a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e016a-107">DESCRIPTION</span></span>
<span data-ttu-id="e016a-108">Cmdleten **Get-AzCosmosDBGremlinDatabaseThroughput** hämtar data flödet för en CosmosDB Gremlin-databas.</span><span class="sxs-lookup"><span data-stu-id="e016a-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e016a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e016a-109">EXAMPLES</span></span>

### <span data-ttu-id="e016a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e016a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="e016a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e016a-111">PARAMETERS</span></span>

### <span data-ttu-id="e016a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e016a-112">-AccountName</span></span>
<span data-ttu-id="e016a-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="e016a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e016a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e016a-114">-DefaultProfile</span></span>
<span data-ttu-id="e016a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e016a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e016a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e016a-116">-InputObject</span></span>
<span data-ttu-id="e016a-117">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e016a-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e016a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e016a-118">-Name</span></span>
<span data-ttu-id="e016a-119">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="e016a-119">Database name.</span></span>

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

### <span data-ttu-id="e016a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e016a-120">-ResourceGroupName</span></span>
<span data-ttu-id="e016a-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e016a-121">Name of resource group.</span></span>

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

### <span data-ttu-id="e016a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e016a-122">CommonParameters</span></span>
<span data-ttu-id="e016a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e016a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e016a-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e016a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e016a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e016a-125">INPUTS</span></span>

### <span data-ttu-id="e016a-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="e016a-126">None</span></span>

## <span data-ttu-id="e016a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e016a-127">OUTPUTS</span></span>

### <span data-ttu-id="e016a-128">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e016a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e016a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e016a-129">NOTES</span></span>

## <span data-ttu-id="e016a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e016a-130">RELATED LINKS</span></span>
