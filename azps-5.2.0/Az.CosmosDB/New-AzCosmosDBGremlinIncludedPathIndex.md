---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403771"
---
# <span data-ttu-id="c497c-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="c497c-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="c497c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c497c-102">SYNOPSIS</span></span>
<span data-ttu-id="c497c-103">Skapar ett nytt objekt av typen PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="c497c-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="c497c-104">Det kan skickas som ett parameter värde för set-AzCosmosDBGremlinIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="c497c-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="c497c-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c497c-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c497c-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c497c-106">DESCRIPTION</span></span>
<span data-ttu-id="c497c-107">Objekt som motsvarar Gremlin API-IncludedPath's-index.</span><span class="sxs-lookup"><span data-stu-id="c497c-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="c497c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c497c-108">EXAMPLES</span></span>

### <span data-ttu-id="c497c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c497c-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="c497c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c497c-110">PARAMETERS</span></span>

### <span data-ttu-id="c497c-111">-Datatyp</span><span class="sxs-lookup"><span data-stu-id="c497c-111">-DataType</span></span>
<span data-ttu-id="c497c-112">Datatyp som indexerings beteendet tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="c497c-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="c497c-113">Möjliga värden inkluderar: "String", "Number", "Point", "polygon", "multipolygon"</span><span class="sxs-lookup"><span data-stu-id="c497c-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="c497c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c497c-114">-DefaultProfile</span></span>
<span data-ttu-id="c497c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c497c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c497c-116">-Sort</span><span class="sxs-lookup"><span data-stu-id="c497c-116">-Kind</span></span>
<span data-ttu-id="c497c-117">Anger typen av index.</span><span class="sxs-lookup"><span data-stu-id="c497c-117">Indicates the type of index.</span></span>
<span data-ttu-id="c497c-118">Möjliga värden inkluderar: "hash", "Range", "Spatial"</span><span class="sxs-lookup"><span data-stu-id="c497c-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="c497c-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="c497c-119">-Precision</span></span>
<span data-ttu-id="c497c-120">Precisionen för indexet.</span><span class="sxs-lookup"><span data-stu-id="c497c-120">The precision of the index.</span></span>
<span data-ttu-id="c497c-121">-1 är maximal precision.</span><span class="sxs-lookup"><span data-stu-id="c497c-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c497c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c497c-122">CommonParameters</span></span>
<span data-ttu-id="c497c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c497c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c497c-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c497c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c497c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c497c-125">INPUTS</span></span>

### <span data-ttu-id="c497c-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="c497c-126">None</span></span>

## <span data-ttu-id="c497c-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c497c-127">OUTPUTS</span></span>

### <span data-ttu-id="c497c-128">Microsoft. Azure. commands. CosmosDB. Models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="c497c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="c497c-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c497c-129">NOTES</span></span>

## <span data-ttu-id="c497c-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c497c-130">RELATED LINKS</span></span>
