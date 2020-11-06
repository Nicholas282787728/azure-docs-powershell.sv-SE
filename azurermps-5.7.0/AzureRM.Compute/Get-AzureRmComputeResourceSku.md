---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: b9e1c42ca3a67a80a939a4e79626253b903764f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574373"
---
# <span data-ttu-id="a3de6-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="a3de6-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="a3de6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3de6-102">SYNOPSIS</span></span>
<span data-ttu-id="a3de6-103">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="a3de6-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3de6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3de6-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [<CommonParameters>]
```

## <span data-ttu-id="a3de6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3de6-105">DESCRIPTION</span></span>
<span data-ttu-id="a3de6-106">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="a3de6-106">List all compute resource Skus</span></span>

## <span data-ttu-id="a3de6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3de6-107">EXAMPLES</span></span>

### <span data-ttu-id="a3de6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3de6-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="a3de6-109">Lista alla resurs-SKU: er i västra USA-regionen</span><span class="sxs-lookup"><span data-stu-id="a3de6-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="a3de6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3de6-110">PARAMETERS</span></span>

### <span data-ttu-id="a3de6-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3de6-111">CommonParameters</span></span>
<span data-ttu-id="a3de6-112">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3de6-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3de6-113">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3de6-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3de6-114">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3de6-114">INPUTS</span></span>

### <span data-ttu-id="a3de6-115">Ingen</span><span class="sxs-lookup"><span data-stu-id="a3de6-115">None</span></span>


## <span data-ttu-id="a3de6-116">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3de6-116">OUTPUTS</span></span>

### <span data-ttu-id="a3de6-117">System. Object</span><span class="sxs-lookup"><span data-stu-id="a3de6-117">System.Object</span></span>

## <span data-ttu-id="a3de6-118">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3de6-118">NOTES</span></span>

## <span data-ttu-id="a3de6-119">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3de6-119">RELATED LINKS</span></span>

