---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931522"
---
# <span data-ttu-id="b2a49-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="b2a49-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="b2a49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2a49-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a49-103">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="b2a49-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2a49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2a49-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2a49-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2a49-105">DESCRIPTION</span></span>
<span data-ttu-id="b2a49-106">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="b2a49-106">List all compute resource Skus</span></span>

## <span data-ttu-id="b2a49-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2a49-107">EXAMPLES</span></span>

### <span data-ttu-id="b2a49-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b2a49-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="b2a49-109">Lista alla resurs-SKU: er i västra USA-regionen</span><span class="sxs-lookup"><span data-stu-id="b2a49-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="b2a49-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2a49-110">PARAMETERS</span></span>

### <span data-ttu-id="b2a49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a49-111">-DefaultProfile</span></span>
<span data-ttu-id="b2a49-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2a49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2a49-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a49-113">CommonParameters</span></span>
<span data-ttu-id="b2a49-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2a49-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a49-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2a49-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a49-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2a49-116">INPUTS</span></span>

### <span data-ttu-id="b2a49-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="b2a49-117">None</span></span>

## <span data-ttu-id="b2a49-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2a49-118">OUTPUTS</span></span>

### <span data-ttu-id="b2a49-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="b2a49-119">System.Object</span></span>

## <span data-ttu-id="b2a49-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2a49-120">NOTES</span></span>

## <span data-ttu-id="b2a49-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2a49-121">RELATED LINKS</span></span>

