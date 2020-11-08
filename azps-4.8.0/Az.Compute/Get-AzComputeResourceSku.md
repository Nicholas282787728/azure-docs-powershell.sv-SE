---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101384"
---
# <span data-ttu-id="08f98-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="08f98-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="08f98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08f98-102">SYNOPSIS</span></span>
<span data-ttu-id="08f98-103">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="08f98-103">List all compute resource Skus</span></span>

## <span data-ttu-id="08f98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08f98-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08f98-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08f98-105">DESCRIPTION</span></span>
<span data-ttu-id="08f98-106">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="08f98-106">List all compute resource Skus</span></span>

## <span data-ttu-id="08f98-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08f98-107">EXAMPLES</span></span>

### <span data-ttu-id="08f98-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="08f98-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="08f98-109">Lista alla resurs-SKU: er i västra USA-regionen</span><span class="sxs-lookup"><span data-stu-id="08f98-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="08f98-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08f98-110">PARAMETERS</span></span>

### <span data-ttu-id="08f98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f98-111">-DefaultProfile</span></span>
<span data-ttu-id="08f98-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08f98-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08f98-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="08f98-113">-Location</span></span>
<span data-ttu-id="08f98-114">Anger en plats för listan tillgängliga SKU: er.</span><span class="sxs-lookup"><span data-stu-id="08f98-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08f98-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f98-115">CommonParameters</span></span>
<span data-ttu-id="08f98-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f98-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f98-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08f98-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f98-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08f98-118">INPUTS</span></span>

### <span data-ttu-id="08f98-119">System. String</span><span class="sxs-lookup"><span data-stu-id="08f98-119">System.String</span></span>

## <span data-ttu-id="08f98-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08f98-120">OUTPUTS</span></span>

### <span data-ttu-id="08f98-121">Microsoft. Azure. commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="08f98-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="08f98-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08f98-122">NOTES</span></span>

## <span data-ttu-id="08f98-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08f98-123">RELATED LINKS</span></span>
