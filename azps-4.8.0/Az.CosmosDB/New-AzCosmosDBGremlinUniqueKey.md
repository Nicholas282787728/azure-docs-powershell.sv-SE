---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262816"
---
# <span data-ttu-id="2bb26-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="2bb26-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="2bb26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bb26-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb26-103">Skapar ett nytt CosmosDB UniqueKeyPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="2bb26-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="2bb26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bb26-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bb26-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bb26-105">DESCRIPTION</span></span>
<span data-ttu-id="2bb26-106">**New-AzCosmosDBGremlinUniqueKeyPolicy-** cmdleten skapar ett nytt objekt av typen PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="2bb26-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="2bb26-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bb26-107">EXAMPLES</span></span>

### <span data-ttu-id="2bb26-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2bb26-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="2bb26-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bb26-109">PARAMETERS</span></span>

### <span data-ttu-id="2bb26-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb26-110">-DefaultProfile</span></span>
<span data-ttu-id="2bb26-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb26-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bb26-112">-Path</span><span class="sxs-lookup"><span data-stu-id="2bb26-112">-Path</span></span>
<span data-ttu-id="2bb26-113">Matris med Sök vägs värden</span><span class="sxs-lookup"><span data-stu-id="2bb26-113">Array of string of path values</span></span>

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

### <span data-ttu-id="2bb26-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb26-114">CommonParameters</span></span>
<span data-ttu-id="2bb26-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb26-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb26-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bb26-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb26-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bb26-117">INPUTS</span></span>

### <span data-ttu-id="2bb26-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="2bb26-118">None</span></span>

## <span data-ttu-id="2bb26-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bb26-119">OUTPUTS</span></span>

### <span data-ttu-id="2bb26-120">Microsoft. Azure. commands. CosmosDB. Models. PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="2bb26-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="2bb26-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bb26-121">NOTES</span></span>

## <span data-ttu-id="2bb26-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bb26-122">RELATED LINKS</span></span>
