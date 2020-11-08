---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260103"
---
# <span data-ttu-id="c24bb-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c24bb-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="c24bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c24bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c24bb-103">Skapar ett nytt objekt av typen PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="c24bb-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="c24bb-104">Det kan skickas som ett parameter värde för set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="c24bb-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="c24bb-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c24bb-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c24bb-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c24bb-106">DESCRIPTION</span></span>
<span data-ttu-id="c24bb-107">Objekt som motsvarar SQL API-ConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="c24bb-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="c24bb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c24bb-108">EXAMPLES</span></span>

### <span data-ttu-id="c24bb-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c24bb-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="c24bb-110">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="c24bb-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="c24bb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c24bb-111">PARAMETERS</span></span>

### <span data-ttu-id="c24bb-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="c24bb-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="c24bb-113">Ska anges när typen är anpassad.</span><span class="sxs-lookup"><span data-stu-id="c24bb-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="c24bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24bb-114">-DefaultProfile</span></span>
<span data-ttu-id="c24bb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c24bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c24bb-116">-Path</span><span class="sxs-lookup"><span data-stu-id="c24bb-116">-Path</span></span>
<span data-ttu-id="c24bb-117">Ska anges när typen är LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="c24bb-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="c24bb-118">– Skriv</span><span class="sxs-lookup"><span data-stu-id="c24bb-118">-Type</span></span>
<span data-ttu-id="c24bb-119">Kan ha värdena: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="c24bb-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="c24bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24bb-120">CommonParameters</span></span>
<span data-ttu-id="c24bb-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24bb-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c24bb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24bb-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c24bb-123">INPUTS</span></span>

### <span data-ttu-id="c24bb-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="c24bb-124">None</span></span>

## <span data-ttu-id="c24bb-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c24bb-125">OUTPUTS</span></span>

### <span data-ttu-id="c24bb-126">Microsoft. Azure. commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c24bb-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="c24bb-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c24bb-127">NOTES</span></span>

## <span data-ttu-id="c24bb-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c24bb-128">RELATED LINKS</span></span>
