---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403792"
---
# <span data-ttu-id="cd3f8-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="cd3f8-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="cd3f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3f8-103">Skapar ett nytt objekt av typen PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="cd3f8-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="cd3f8-104">Det kan skickas som ett parameter värde för set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="cd3f8-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="cd3f8-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd3f8-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd3f8-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd3f8-106">DESCRIPTION</span></span>
<span data-ttu-id="cd3f8-107">Objekt som motsvarar Gremlin API-CompositePath.</span><span class="sxs-lookup"><span data-stu-id="cd3f8-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="cd3f8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd3f8-108">EXAMPLES</span></span>

### <span data-ttu-id="cd3f8-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd3f8-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="cd3f8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd3f8-110">PARAMETERS</span></span>

### <span data-ttu-id="cd3f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3f8-111">-DefaultProfile</span></span>
<span data-ttu-id="cd3f8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd3f8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd3f8-113">-Beställ</span><span class="sxs-lookup"><span data-stu-id="cd3f8-113">-Order</span></span>
<span data-ttu-id="cd3f8-114">Hämtar eller anger sorterings ordning för sammansatta banor.</span><span class="sxs-lookup"><span data-stu-id="cd3f8-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="cd3f8-115">Möjliga värden är: "stigande", "fallande"</span><span class="sxs-lookup"><span data-stu-id="cd3f8-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="cd3f8-116">-Path</span><span class="sxs-lookup"><span data-stu-id="cd3f8-116">-Path</span></span>
<span data-ttu-id="cd3f8-117">Sökvägen som indexerings beteendet gäller för.</span><span class="sxs-lookup"><span data-stu-id="cd3f8-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="cd3f8-118">Index Sök vägar börjar normalt med rot och end med jokertecken (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="cd3f8-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="cd3f8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3f8-119">CommonParameters</span></span>
<span data-ttu-id="cd3f8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd3f8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3f8-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd3f8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3f8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd3f8-122">INPUTS</span></span>

### <span data-ttu-id="cd3f8-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd3f8-123">None</span></span>

## <span data-ttu-id="cd3f8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd3f8-124">OUTPUTS</span></span>

### <span data-ttu-id="cd3f8-125">Microsoft. Azure. commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="cd3f8-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="cd3f8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd3f8-126">NOTES</span></span>

## <span data-ttu-id="cd3f8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd3f8-127">RELATED LINKS</span></span>
