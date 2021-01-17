---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413816"
---
# <span data-ttu-id="18cf1-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="18cf1-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="18cf1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="18cf1-103">Skapar ett nytt objekt av typen PSCompositePath.</span><span class="sxs-lookup"><span data-stu-id="18cf1-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="18cf1-104">Det kan skickas som ett parameter värde för set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="18cf1-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="18cf1-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18cf1-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18cf1-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18cf1-106">DESCRIPTION</span></span>
<span data-ttu-id="18cf1-107">Objekt som motsvarar SQL API-CompositePath.</span><span class="sxs-lookup"><span data-stu-id="18cf1-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="18cf1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18cf1-108">EXAMPLES</span></span>

### <span data-ttu-id="18cf1-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="18cf1-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="18cf1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18cf1-110">PARAMETERS</span></span>

### <span data-ttu-id="18cf1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cf1-111">-DefaultProfile</span></span>
<span data-ttu-id="18cf1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18cf1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18cf1-113">-Beställ</span><span class="sxs-lookup"><span data-stu-id="18cf1-113">-Order</span></span>
<span data-ttu-id="18cf1-114">Hämtar eller anger sorterings ordning för sammansatta banor.</span><span class="sxs-lookup"><span data-stu-id="18cf1-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="18cf1-115">Möjliga värden är: "stigande", "fallande"</span><span class="sxs-lookup"><span data-stu-id="18cf1-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="18cf1-116">-Path</span><span class="sxs-lookup"><span data-stu-id="18cf1-116">-Path</span></span>
<span data-ttu-id="18cf1-117">Sökvägen som indexerings beteendet gäller för.</span><span class="sxs-lookup"><span data-stu-id="18cf1-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="18cf1-118">Index Sök vägar börjar normalt med rot och end med jokertecken (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="18cf1-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="18cf1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cf1-119">CommonParameters</span></span>
<span data-ttu-id="18cf1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18cf1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cf1-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18cf1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cf1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18cf1-122">INPUTS</span></span>

### <span data-ttu-id="18cf1-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="18cf1-123">None</span></span>

## <span data-ttu-id="18cf1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18cf1-124">OUTPUTS</span></span>

### <span data-ttu-id="18cf1-125">Microsoft. Azure. commands. CosmosDB. Models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="18cf1-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="18cf1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18cf1-126">NOTES</span></span>

## <span data-ttu-id="18cf1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18cf1-127">RELATED LINKS</span></span>
