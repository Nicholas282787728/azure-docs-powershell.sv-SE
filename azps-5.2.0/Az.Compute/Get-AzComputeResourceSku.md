---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393795"
---
# <span data-ttu-id="80f08-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="80f08-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="80f08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80f08-102">SYNOPSIS</span></span>
<span data-ttu-id="80f08-103">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="80f08-103">List all compute resource Skus</span></span>

## <span data-ttu-id="80f08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80f08-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80f08-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80f08-105">DESCRIPTION</span></span>
<span data-ttu-id="80f08-106">Lista alla Compute Resource-SKU: er</span><span class="sxs-lookup"><span data-stu-id="80f08-106">List all compute resource Skus</span></span>

## <span data-ttu-id="80f08-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80f08-107">EXAMPLES</span></span>

### <span data-ttu-id="80f08-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="80f08-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="80f08-109">Lista alla resurs-SKU: er i västra USA-regionen</span><span class="sxs-lookup"><span data-stu-id="80f08-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="80f08-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80f08-110">PARAMETERS</span></span>

### <span data-ttu-id="80f08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f08-111">-DefaultProfile</span></span>
<span data-ttu-id="80f08-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80f08-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80f08-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="80f08-113">-Location</span></span>
<span data-ttu-id="80f08-114">Anger en plats för listan tillgängliga SKU: er.</span><span class="sxs-lookup"><span data-stu-id="80f08-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="80f08-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f08-115">CommonParameters</span></span>
<span data-ttu-id="80f08-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f08-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f08-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80f08-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f08-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80f08-118">INPUTS</span></span>

### <span data-ttu-id="80f08-119">System. String</span><span class="sxs-lookup"><span data-stu-id="80f08-119">System.String</span></span>

## <span data-ttu-id="80f08-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80f08-120">OUTPUTS</span></span>

### <span data-ttu-id="80f08-121">Microsoft. Azure. commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="80f08-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="80f08-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80f08-122">NOTES</span></span>

## <span data-ttu-id="80f08-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80f08-123">RELATED LINKS</span></span>
