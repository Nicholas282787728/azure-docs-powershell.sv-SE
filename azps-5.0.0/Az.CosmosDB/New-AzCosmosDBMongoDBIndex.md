---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321519"
---
# <span data-ttu-id="83afa-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="83afa-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="83afa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83afa-102">SYNOPSIS</span></span>
<span data-ttu-id="83afa-103">Skapar ett nytt CosmosDB MongoDB-index.</span><span class="sxs-lookup"><span data-stu-id="83afa-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="83afa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83afa-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83afa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83afa-105">DESCRIPTION</span></span>
<span data-ttu-id="83afa-106">**New-AzCosmosDBMongoDBIndex** skapar ett nytt CosmosDB MongoDB-index.</span><span class="sxs-lookup"><span data-stu-id="83afa-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="83afa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83afa-107">EXAMPLES</span></span>

### <span data-ttu-id="83afa-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="83afa-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="83afa-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83afa-109">PARAMETERS</span></span>

### <span data-ttu-id="83afa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83afa-110">-DefaultProfile</span></span>
<span data-ttu-id="83afa-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83afa-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83afa-112">-Viktiga</span><span class="sxs-lookup"><span data-stu-id="83afa-112">-Key</span></span>
<span data-ttu-id="83afa-113">Matris med nyckeltal som strängar.</span><span class="sxs-lookup"><span data-stu-id="83afa-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afa-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="83afa-114">-TtlInSeconds</span></span>
<span data-ttu-id="83afa-115">Antal sekunder efter vilket indexet går ut.</span><span class="sxs-lookup"><span data-stu-id="83afa-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="83afa-116">-Unikt</span><span class="sxs-lookup"><span data-stu-id="83afa-116">-Unique</span></span>
<span data-ttu-id="83afa-117">Bool för att ange om indexet är unikt eller inte.</span><span class="sxs-lookup"><span data-stu-id="83afa-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83afa-118">CommonParameters</span></span>
<span data-ttu-id="83afa-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83afa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83afa-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83afa-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83afa-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83afa-121">INPUTS</span></span>

### <span data-ttu-id="83afa-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="83afa-122">None</span></span>

## <span data-ttu-id="83afa-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83afa-123">OUTPUTS</span></span>

### <span data-ttu-id="83afa-124">Microsoft. Azure. commands. CosmosDB. Models. PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="83afa-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="83afa-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83afa-125">NOTES</span></span>

## <span data-ttu-id="83afa-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83afa-126">RELATED LINKS</span></span>