---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089812"
---
# <span data-ttu-id="39912-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="39912-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="39912-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39912-102">SYNOPSIS</span></span>
<span data-ttu-id="39912-103">Skapar ett nytt objekt av typen PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="39912-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="39912-104">Det kan skickas som ett parameter värde för set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="39912-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="39912-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39912-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39912-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39912-106">DESCRIPTION</span></span>
<span data-ttu-id="39912-107">Objekt som motsvarar Gremlin API-ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="39912-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="39912-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39912-108">EXAMPLES</span></span>

### <span data-ttu-id="39912-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="39912-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="39912-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39912-110">PARAMETERS</span></span>

### <span data-ttu-id="39912-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="39912-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="39912-112">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="39912-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="39912-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39912-113">-DefaultProfile</span></span>
<span data-ttu-id="39912-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39912-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39912-115">-Path</span><span class="sxs-lookup"><span data-stu-id="39912-115">-Path</span></span>
<span data-ttu-id="39912-116">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="39912-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="39912-117">– Skriv</span><span class="sxs-lookup"><span data-stu-id="39912-117">-Type</span></span>
<span data-ttu-id="39912-118">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="39912-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="39912-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39912-119">CommonParameters</span></span>
<span data-ttu-id="39912-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39912-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39912-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39912-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39912-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39912-122">INPUTS</span></span>

### <span data-ttu-id="39912-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="39912-123">None</span></span>

## <span data-ttu-id="39912-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39912-124">OUTPUTS</span></span>

### <span data-ttu-id="39912-125">Microsoft. Azure. commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="39912-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="39912-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39912-126">NOTES</span></span>

## <span data-ttu-id="39912-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39912-127">RELATED LINKS</span></span>
