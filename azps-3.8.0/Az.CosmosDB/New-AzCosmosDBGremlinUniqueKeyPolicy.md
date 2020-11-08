---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 593e299a6d7a1aa8131848f6de5f6c7aec8bd8c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091371"
---
# <span data-ttu-id="ad782-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="ad782-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="ad782-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad782-102">SYNOPSIS</span></span>
<span data-ttu-id="ad782-103">Skapar ett nytt CosmosDB UniqueKeyPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="ad782-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="ad782-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad782-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad782-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad782-105">DESCRIPTION</span></span>
<span data-ttu-id="ad782-106">**New-AzCosmosDBGremlinUniqueKeyPolicy-** cmdleten skapar ett nytt objekt av typen PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="ad782-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="ad782-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad782-107">EXAMPLES</span></span>

### <span data-ttu-id="ad782-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad782-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="ad782-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad782-109">PARAMETERS</span></span>

### <span data-ttu-id="ad782-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad782-110">-DefaultProfile</span></span>
<span data-ttu-id="ad782-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad782-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad782-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="ad782-112">-UniqueKey</span></span>
<span data-ttu-id="ad782-113">Matris med objekt av typen PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="ad782-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad782-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad782-114">CommonParameters</span></span>
<span data-ttu-id="ad782-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad782-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad782-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad782-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad782-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad782-117">INPUTS</span></span>

### <span data-ttu-id="ad782-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="ad782-118">None</span></span>

## <span data-ttu-id="ad782-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad782-119">OUTPUTS</span></span>

### <span data-ttu-id="ad782-120">Microsoft. Azure. commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="ad782-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="ad782-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad782-121">NOTES</span></span>

## <span data-ttu-id="ad782-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad782-122">RELATED LINKS</span></span>
