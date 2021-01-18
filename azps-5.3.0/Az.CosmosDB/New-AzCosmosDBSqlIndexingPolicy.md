---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524329"
---
# <span data-ttu-id="20f33-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="20f33-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="20f33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20f33-102">SYNOPSIS</span></span>
<span data-ttu-id="20f33-103">Skapar ett nytt CosmosDB SQL IndexingPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="20f33-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="20f33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20f33-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20f33-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20f33-105">DESCRIPTION</span></span>
<span data-ttu-id="20f33-106">**New-AzCosmosDBSqlIndexingPolicy-** cmdleten skapar ett nytt objekt av typen PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="20f33-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="20f33-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20f33-107">EXAMPLES</span></span>

### <span data-ttu-id="20f33-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20f33-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="20f33-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20f33-109">PARAMETERS</span></span>

### <span data-ttu-id="20f33-110">-Automatisk</span><span class="sxs-lookup"><span data-stu-id="20f33-110">-Automatic</span></span>
<span data-ttu-id="20f33-111">Bool för att ange om indexerings principen är automatisk</span><span class="sxs-lookup"><span data-stu-id="20f33-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="20f33-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="20f33-112">-CompositePath</span></span>
<span data-ttu-id="20f33-113">Matris med objekt av typen Microsoft. Azure. commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="20f33-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="20f33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f33-114">-DefaultProfile</span></span>
<span data-ttu-id="20f33-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20f33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20f33-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="20f33-116">-ExcludedPath</span></span>
<span data-ttu-id="20f33-117">Matris med strängar som innehåller excludedPath (anger en sökväg i ett JSON-dokument som ska uteslutas i Azure Cosmos DB-tjänsten.)  element.</span><span class="sxs-lookup"><span data-stu-id="20f33-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="20f33-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="20f33-118">-IncludedPath</span></span>
<span data-ttu-id="20f33-119">Matris med strängar som innehåller includedPath (anger en sökväg i ett JSON-dokument som ska ingå i Azure Cosmos DB service.)-elementen.</span><span class="sxs-lookup"><span data-stu-id="20f33-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="20f33-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="20f33-120">-IndexingMode</span></span>
<span data-ttu-id="20f33-121">anger indexerings läget.</span><span class="sxs-lookup"><span data-stu-id="20f33-121">indicates the indexing mode.</span></span>
<span data-ttu-id="20f33-122">Möjliga värden är: "konsekvent", "Lazy", "inget"</span><span class="sxs-lookup"><span data-stu-id="20f33-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="20f33-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="20f33-123">-SpatialSpec</span></span>
<span data-ttu-id="20f33-124">Matris med objekt av typen Microsoft. Azure. commands. CosmosDB. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="20f33-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="20f33-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f33-125">CommonParameters</span></span>
<span data-ttu-id="20f33-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f33-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f33-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20f33-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f33-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20f33-128">INPUTS</span></span>

### <span data-ttu-id="20f33-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="20f33-129">None</span></span>

## <span data-ttu-id="20f33-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20f33-130">OUTPUTS</span></span>

### <span data-ttu-id="20f33-131">Microsoft. Azure. commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="20f33-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="20f33-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20f33-132">NOTES</span></span>

## <span data-ttu-id="20f33-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20f33-133">RELATED LINKS</span></span>
