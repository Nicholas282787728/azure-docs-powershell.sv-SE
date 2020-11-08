---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: ab57e922a7ef63d14a36bbd91ed268822e2c61e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091417"
---
# <span data-ttu-id="56024-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="56024-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="56024-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56024-102">SYNOPSIS</span></span>
<span data-ttu-id="56024-103">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="56024-103">List all compute resource Skus</span></span>

## <span data-ttu-id="56024-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56024-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56024-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56024-105">DESCRIPTION</span></span>
<span data-ttu-id="56024-106">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="56024-106">List all compute resource Skus</span></span>

## <span data-ttu-id="56024-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56024-107">EXAMPLES</span></span>

### <span data-ttu-id="56024-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="56024-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="56024-109">Lista alla resurs-SKU: er i västra USA-regionen</span><span class="sxs-lookup"><span data-stu-id="56024-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="56024-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56024-110">PARAMETERS</span></span>

### <span data-ttu-id="56024-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56024-111">-DefaultProfile</span></span>
<span data-ttu-id="56024-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56024-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56024-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56024-113">CommonParameters</span></span>
<span data-ttu-id="56024-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56024-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56024-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56024-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56024-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56024-116">INPUTS</span></span>

### <span data-ttu-id="56024-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="56024-117">None</span></span>

## <span data-ttu-id="56024-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56024-118">OUTPUTS</span></span>

### <span data-ttu-id="56024-119">Microsoft. Azure. commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="56024-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="56024-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56024-120">NOTES</span></span>

## <span data-ttu-id="56024-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56024-121">RELATED LINKS</span></span>
