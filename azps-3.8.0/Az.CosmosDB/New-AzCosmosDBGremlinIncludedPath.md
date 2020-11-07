---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925929"
---
# <span data-ttu-id="698b5-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="698b5-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="698b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="698b5-102">SYNOPSIS</span></span>
<span data-ttu-id="698b5-103">Skapar ett nytt objekt av typen PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="698b5-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="698b5-104">Det kan skickas som ett parameter värde för set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="698b5-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="698b5-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="698b5-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="698b5-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="698b5-106">DESCRIPTION</span></span>
<span data-ttu-id="698b5-107">Objekt som motsvarar Gremlin API-IncludedPath.</span><span class="sxs-lookup"><span data-stu-id="698b5-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="698b5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="698b5-108">EXAMPLES</span></span>

### <span data-ttu-id="698b5-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="698b5-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="698b5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="698b5-110">PARAMETERS</span></span>

### <span data-ttu-id="698b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698b5-111">-DefaultProfile</span></span>
<span data-ttu-id="698b5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="698b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="698b5-113">-Index</span><span class="sxs-lookup"><span data-stu-id="698b5-113">-Index</span></span>
<span data-ttu-id="698b5-114">Lista över index för den här sökvägen</span><span class="sxs-lookup"><span data-stu-id="698b5-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698b5-115">-Path</span><span class="sxs-lookup"><span data-stu-id="698b5-115">-Path</span></span>
<span data-ttu-id="698b5-116">Sökvägen som indexerings beteendet gäller för.</span><span class="sxs-lookup"><span data-stu-id="698b5-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="698b5-117">Index Sök vägar börjar normalt med rot och end med jokertecken (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="698b5-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="698b5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698b5-118">CommonParameters</span></span>
<span data-ttu-id="698b5-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="698b5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698b5-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="698b5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698b5-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="698b5-121">INPUTS</span></span>

### <span data-ttu-id="698b5-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="698b5-122">None</span></span>

## <span data-ttu-id="698b5-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="698b5-123">OUTPUTS</span></span>

### <span data-ttu-id="698b5-124">Microsoft. Azure. commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="698b5-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="698b5-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="698b5-125">NOTES</span></span>

## <span data-ttu-id="698b5-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="698b5-126">RELATED LINKS</span></span>
