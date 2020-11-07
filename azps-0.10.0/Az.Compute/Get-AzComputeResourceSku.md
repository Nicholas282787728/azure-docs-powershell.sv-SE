---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 751a551f5ed0a0a1968c74e5f94bcabad3b5ff32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925249"
---
# <span data-ttu-id="f774c-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="f774c-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="f774c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f774c-102">SYNOPSIS</span></span>
<span data-ttu-id="f774c-103">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="f774c-103">List all compute resource Skus</span></span>

## <span data-ttu-id="f774c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f774c-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f774c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f774c-105">DESCRIPTION</span></span>
<span data-ttu-id="f774c-106">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="f774c-106">List all compute resource Skus</span></span>

## <span data-ttu-id="f774c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f774c-107">EXAMPLES</span></span>

### <span data-ttu-id="f774c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f774c-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="f774c-109">Lista alla resurs-SKU: er i västra USA-regionen</span><span class="sxs-lookup"><span data-stu-id="f774c-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="f774c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f774c-110">PARAMETERS</span></span>

### <span data-ttu-id="f774c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f774c-111">-DefaultProfile</span></span>
<span data-ttu-id="f774c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f774c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f774c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f774c-113">CommonParameters</span></span>
<span data-ttu-id="f774c-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f774c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f774c-115">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f774c-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f774c-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f774c-116">INPUTS</span></span>

### <span data-ttu-id="f774c-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="f774c-117">None</span></span>

## <span data-ttu-id="f774c-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f774c-118">OUTPUTS</span></span>

### <span data-ttu-id="f774c-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="f774c-119">System.Object</span></span>

## <span data-ttu-id="f774c-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f774c-120">NOTES</span></span>

## <span data-ttu-id="f774c-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f774c-121">RELATED LINKS</span></span>

