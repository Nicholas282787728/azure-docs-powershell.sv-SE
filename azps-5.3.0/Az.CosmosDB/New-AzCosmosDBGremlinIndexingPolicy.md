---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524344"
---
# <span data-ttu-id="2ab37-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2ab37-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="2ab37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ab37-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab37-103">Skapar ett nytt CosmosDB IndexingPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="2ab37-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="2ab37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ab37-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ab37-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ab37-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab37-106">**New-AzCosmosDBGremlinIndexingPolicy-** cmdleten skapar ett nytt objekt av typen PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="2ab37-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="2ab37-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ab37-107">EXAMPLES</span></span>

### <span data-ttu-id="2ab37-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2ab37-108">Example 1</span></span>
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

<span data-ttu-id="2ab37-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="2ab37-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="2ab37-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ab37-110">PARAMETERS</span></span>

### <span data-ttu-id="2ab37-111">-Automatisk</span><span class="sxs-lookup"><span data-stu-id="2ab37-111">-Automatic</span></span>
<span data-ttu-id="2ab37-112">Bool för att ange om indexerings principen är automatisk</span><span class="sxs-lookup"><span data-stu-id="2ab37-112">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="2ab37-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="2ab37-113">-CompositePath</span></span>
<span data-ttu-id="2ab37-114">Matris med objekt av typen Microsoft. Azure. commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="2ab37-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="2ab37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab37-115">-DefaultProfile</span></span>
<span data-ttu-id="2ab37-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ab37-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="2ab37-117">-ExcludedPath</span></span>
<span data-ttu-id="2ab37-118">Matris med strängar som innehåller excludedPath (anger en sökväg i ett JSON-dokument som ska uteslutas i Azure Cosmos DB-tjänsten.)  element.</span><span class="sxs-lookup"><span data-stu-id="2ab37-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="2ab37-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="2ab37-119">-IncludedPath</span></span>
<span data-ttu-id="2ab37-120">Matris med strängar som innehåller includedPath (anger en sökväg i ett JSON-dokument som ska ingå i Azure Cosmos DB service.)-elementen.</span><span class="sxs-lookup"><span data-stu-id="2ab37-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="2ab37-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="2ab37-121">-IndexingMode</span></span>
<span data-ttu-id="2ab37-122">Anger indexerings läget.</span><span class="sxs-lookup"><span data-stu-id="2ab37-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="2ab37-123">Möjliga värden är: "konsekvent", "Lazy", "inget"</span><span class="sxs-lookup"><span data-stu-id="2ab37-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="2ab37-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="2ab37-124">-SpatialSpec</span></span>
<span data-ttu-id="2ab37-125">Matris med objekt av typen Microsoft. Azure. commands. CosmosDB. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="2ab37-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="2ab37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab37-126">CommonParameters</span></span>
<span data-ttu-id="2ab37-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab37-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ab37-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab37-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ab37-129">INPUTS</span></span>

### <span data-ttu-id="2ab37-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="2ab37-130">None</span></span>

## <span data-ttu-id="2ab37-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ab37-131">OUTPUTS</span></span>

### <span data-ttu-id="2ab37-132">Microsoft. Azure. commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2ab37-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="2ab37-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ab37-133">NOTES</span></span>

## <span data-ttu-id="2ab37-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ab37-134">RELATED LINKS</span></span>
