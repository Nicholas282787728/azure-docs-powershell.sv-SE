---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260106"
---
# <span data-ttu-id="42bf8-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="42bf8-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="42bf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="42bf8-103">Skapar ett nytt objekt av typen PSConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="42bf8-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="42bf8-104">Det kan skickas som ett parameter värde för set-AzCosmosDBGremlinGraph.</span><span class="sxs-lookup"><span data-stu-id="42bf8-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="42bf8-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42bf8-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42bf8-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42bf8-106">DESCRIPTION</span></span>
<span data-ttu-id="42bf8-107">Objekt som motsvarar Gremlin API-ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="42bf8-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="42bf8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42bf8-108">EXAMPLES</span></span>

### <span data-ttu-id="42bf8-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42bf8-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="42bf8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42bf8-110">PARAMETERS</span></span>

### <span data-ttu-id="42bf8-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="42bf8-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="42bf8-112">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="42bf8-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="42bf8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42bf8-113">-DefaultProfile</span></span>
<span data-ttu-id="42bf8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42bf8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42bf8-115">-Path</span><span class="sxs-lookup"><span data-stu-id="42bf8-115">-Path</span></span>
<span data-ttu-id="42bf8-116">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="42bf8-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="42bf8-117">– Skriv</span><span class="sxs-lookup"><span data-stu-id="42bf8-117">-Type</span></span>
<span data-ttu-id="42bf8-118">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="42bf8-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="42bf8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42bf8-119">CommonParameters</span></span>
<span data-ttu-id="42bf8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42bf8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42bf8-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42bf8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42bf8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42bf8-122">INPUTS</span></span>

### <span data-ttu-id="42bf8-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="42bf8-123">None</span></span>

## <span data-ttu-id="42bf8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42bf8-124">OUTPUTS</span></span>

### <span data-ttu-id="42bf8-125">Microsoft. Azure. commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="42bf8-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="42bf8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42bf8-126">NOTES</span></span>

## <span data-ttu-id="42bf8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42bf8-127">RELATED LINKS</span></span>