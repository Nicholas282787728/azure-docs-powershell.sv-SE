---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: fd4a06375a4dfab7f8b8cd4b08a2112310e99b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584803"
---
# <span data-ttu-id="3eb58-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="3eb58-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="3eb58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3eb58-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb58-103">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="3eb58-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3eb58-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eb58-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3eb58-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb58-106">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="3eb58-106">List all compute resource Skus</span></span>

## <span data-ttu-id="3eb58-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3eb58-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb58-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3eb58-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="3eb58-109">Lista alla resurs-SKU: er i västra USA-regionen</span><span class="sxs-lookup"><span data-stu-id="3eb58-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="3eb58-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3eb58-110">PARAMETERS</span></span>

### <span data-ttu-id="3eb58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb58-111">-DefaultProfile</span></span>
<span data-ttu-id="3eb58-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3eb58-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb58-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb58-113">CommonParameters</span></span>
<span data-ttu-id="3eb58-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb58-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb58-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb58-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb58-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3eb58-116">INPUTS</span></span>

### <span data-ttu-id="3eb58-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="3eb58-117">None</span></span>

## <span data-ttu-id="3eb58-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3eb58-118">OUTPUTS</span></span>

### <span data-ttu-id="3eb58-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="3eb58-119">System.Object</span></span>

## <span data-ttu-id="3eb58-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3eb58-120">NOTES</span></span>

## <span data-ttu-id="3eb58-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3eb58-121">RELATED LINKS</span></span>
