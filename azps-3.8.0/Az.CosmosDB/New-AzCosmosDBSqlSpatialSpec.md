---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091360"
---
# <span data-ttu-id="425da-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="425da-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="425da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="425da-102">SYNOPSIS</span></span>
<span data-ttu-id="425da-103">Skapar ett nytt objekt av typen PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="425da-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="425da-104">Det kan skickas som ett parameter värde för set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="425da-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="425da-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="425da-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="425da-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="425da-106">DESCRIPTION</span></span>
<span data-ttu-id="425da-107">Skapar ett objekt som motsvarar SQL API-SpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="425da-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="425da-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="425da-108">EXAMPLES</span></span>

### <span data-ttu-id="425da-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="425da-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="425da-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="425da-110">PARAMETERS</span></span>

### <span data-ttu-id="425da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425da-111">-DefaultProfile</span></span>
<span data-ttu-id="425da-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="425da-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="425da-113">-Path</span><span class="sxs-lookup"><span data-stu-id="425da-113">-Path</span></span>
<span data-ttu-id="425da-114">Sökväg i JSON-dokument som ska indexeras.</span><span class="sxs-lookup"><span data-stu-id="425da-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="425da-115">– Skriv</span><span class="sxs-lookup"><span data-stu-id="425da-115">-Type</span></span>
<span data-ttu-id="425da-116">Matris med strängar med acceptabla värden: punkt, LineString, polygon, multipolygon.</span><span class="sxs-lookup"><span data-stu-id="425da-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="425da-117">Representera olika banor.</span><span class="sxs-lookup"><span data-stu-id="425da-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="425da-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425da-118">CommonParameters</span></span>
<span data-ttu-id="425da-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="425da-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425da-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="425da-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425da-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="425da-121">INPUTS</span></span>

### <span data-ttu-id="425da-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="425da-122">None</span></span>

## <span data-ttu-id="425da-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="425da-123">OUTPUTS</span></span>

### <span data-ttu-id="425da-124">Microsoft. Azure. commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="425da-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="425da-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="425da-125">NOTES</span></span>

## <span data-ttu-id="425da-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="425da-126">RELATED LINKS</span></span>
