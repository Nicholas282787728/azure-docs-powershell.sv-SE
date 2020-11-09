---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321552"
---
# <span data-ttu-id="9cdeb-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="9cdeb-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="9cdeb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cdeb-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdeb-103">Skapar ett nytt CosmosDB IndexingPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="9cdeb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cdeb-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cdeb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cdeb-105">DESCRIPTION</span></span>
<span data-ttu-id="9cdeb-106">**New-AzCosmosDBGremlinIndexingPolicy-** cmdleten skapar ett nytt objekt av typen PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="9cdeb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cdeb-107">EXAMPLES</span></span>

### <span data-ttu-id="9cdeb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9cdeb-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="9cdeb-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="9cdeb-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9cdeb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cdeb-110">PARAMETERS</span></span>

### <span data-ttu-id="9cdeb-111">-Automatisk</span><span class="sxs-lookup"><span data-stu-id="9cdeb-111">-Automatic</span></span>
<span data-ttu-id="9cdeb-112">Bool för att ange om indexerings principen är automatisk</span><span class="sxs-lookup"><span data-stu-id="9cdeb-112">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="9cdeb-113">-CompositePath</span></span>
<span data-ttu-id="9cdeb-114">Matris med objekt av typen Microsoft. Azure. commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="9cdeb-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdeb-115">-DefaultProfile</span></span>
<span data-ttu-id="9cdeb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cdeb-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="9cdeb-117">-ExcludedPath</span></span>
<span data-ttu-id="9cdeb-118">Matris med strängar som innehåller excludedPath (anger en sökväg i ett JSON-dokument som ska uteslutas i Azure Cosmos DB-tjänsten.)  element.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="9cdeb-119">-IncludedPath</span></span>
<span data-ttu-id="9cdeb-120">Matris med strängar som innehåller includedPath (anger en sökväg i ett JSON-dokument som ska ingå i Azure Cosmos DB service.)-elementen.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="9cdeb-121">-IndexingMode</span></span>
<span data-ttu-id="9cdeb-122">Anger indexerings läget.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="9cdeb-123">Möjliga värden är: "konsekvent", "Lazy", "inget"</span><span class="sxs-lookup"><span data-stu-id="9cdeb-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="9cdeb-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9cdeb-124">-SpatialSpec</span></span>
<span data-ttu-id="9cdeb-125">Matris med objekt av typen Microsoft. Azure. commands. CosmosDB. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9cdeb-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdeb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdeb-126">CommonParameters</span></span>
<span data-ttu-id="9cdeb-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cdeb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdeb-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cdeb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdeb-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cdeb-129">INPUTS</span></span>

### <span data-ttu-id="9cdeb-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="9cdeb-130">None</span></span>

## <span data-ttu-id="9cdeb-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cdeb-131">OUTPUTS</span></span>

### <span data-ttu-id="9cdeb-132">Microsoft. Azure. commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="9cdeb-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="9cdeb-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cdeb-133">NOTES</span></span>

## <span data-ttu-id="9cdeb-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cdeb-134">RELATED LINKS</span></span>
