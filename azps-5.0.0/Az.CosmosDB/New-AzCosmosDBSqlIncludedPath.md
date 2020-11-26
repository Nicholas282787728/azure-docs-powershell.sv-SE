---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321504"
---
# <span data-ttu-id="d20e8-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="d20e8-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="d20e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d20e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d20e8-103">Skapar ett nytt objekt av typen PSIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="d20e8-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="d20e8-104">Det kan skickas som ett parameter värde för set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="d20e8-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="d20e8-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d20e8-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d20e8-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d20e8-106">DESCRIPTION</span></span>
<span data-ttu-id="d20e8-107">Objekt som motsvarar SQL API-IncludedPath.</span><span class="sxs-lookup"><span data-stu-id="d20e8-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="d20e8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d20e8-108">EXAMPLES</span></span>

### <span data-ttu-id="d20e8-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d20e8-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="d20e8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d20e8-110">PARAMETERS</span></span>

### <span data-ttu-id="d20e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20e8-111">-DefaultProfile</span></span>
<span data-ttu-id="d20e8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d20e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d20e8-113">-Index</span><span class="sxs-lookup"><span data-stu-id="d20e8-113">-Index</span></span>
<span data-ttu-id="d20e8-114">Lista över index för den här sökvägen</span><span class="sxs-lookup"><span data-stu-id="d20e8-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="d20e8-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d20e8-115">-Path</span></span>
<span data-ttu-id="d20e8-116">Sökvägen som indexerings beteendet gäller för.</span><span class="sxs-lookup"><span data-stu-id="d20e8-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="d20e8-117">Index Sök vägar börjar normalt med rot och end med jokertecken (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="d20e8-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="d20e8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20e8-118">CommonParameters</span></span>
<span data-ttu-id="d20e8-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d20e8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20e8-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d20e8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20e8-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d20e8-121">INPUTS</span></span>

### <span data-ttu-id="d20e8-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="d20e8-122">None</span></span>

## <span data-ttu-id="d20e8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d20e8-123">OUTPUTS</span></span>

### <span data-ttu-id="d20e8-124">Microsoft. Azure. commands. CosmosDB. Models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="d20e8-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="d20e8-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d20e8-125">NOTES</span></span>

## <span data-ttu-id="d20e8-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d20e8-126">RELATED LINKS</span></span>