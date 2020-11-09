---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321543"
---
# <span data-ttu-id="a3c09-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="a3c09-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="a3c09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3c09-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c09-103">Skapar ett nytt objekt av typen PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="a3c09-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="a3c09-104">Det kan skickas som ett parameter värde för set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="a3c09-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="a3c09-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3c09-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3c09-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3c09-106">DESCRIPTION</span></span>
<span data-ttu-id="a3c09-107">Skapar objekt som motsvarar Gremlin API-SpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="a3c09-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="a3c09-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3c09-108">EXAMPLES</span></span>

### <span data-ttu-id="a3c09-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3c09-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="a3c09-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3c09-110">PARAMETERS</span></span>

### <span data-ttu-id="a3c09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c09-111">-DefaultProfile</span></span>
<span data-ttu-id="a3c09-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3c09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c09-113">-Path</span><span class="sxs-lookup"><span data-stu-id="a3c09-113">-Path</span></span>
<span data-ttu-id="a3c09-114">Sökväg i JSON-dokument som ska indexeras.</span><span class="sxs-lookup"><span data-stu-id="a3c09-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="a3c09-115">– Skriv</span><span class="sxs-lookup"><span data-stu-id="a3c09-115">-Type</span></span>
<span data-ttu-id="a3c09-116">Matris med strängar med acceptabla värden: punkt, LineString, polygon, multipolygon.</span><span class="sxs-lookup"><span data-stu-id="a3c09-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="a3c09-117">Representera olika banor.</span><span class="sxs-lookup"><span data-stu-id="a3c09-117">Represent's paths spatial type.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c09-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c09-118">CommonParameters</span></span>
<span data-ttu-id="a3c09-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3c09-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c09-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3c09-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c09-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3c09-121">INPUTS</span></span>

### <span data-ttu-id="a3c09-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="a3c09-122">None</span></span>

## <span data-ttu-id="a3c09-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3c09-123">OUTPUTS</span></span>

### <span data-ttu-id="a3c09-124">Microsoft. Azure. commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="a3c09-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="a3c09-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3c09-125">NOTES</span></span>

## <span data-ttu-id="a3c09-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3c09-126">RELATED LINKS</span></span>
