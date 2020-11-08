---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272775"
---
# <span data-ttu-id="88eb5-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="88eb5-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="88eb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="88eb5-103">Hämtar tillgänglighets status för CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="88eb5-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="88eb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88eb5-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88eb5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88eb5-105">DESCRIPTION</span></span>
<span data-ttu-id="88eb5-106">Cmdleten **Get-AzCdnEndpointNameAvailability** hämtar tillgänglighets statusen för slut punkten för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="88eb5-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="88eb5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88eb5-107">EXAMPLES</span></span>

## <span data-ttu-id="88eb5-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88eb5-108">PARAMETERS</span></span>

### <span data-ttu-id="88eb5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88eb5-109">-DefaultProfile</span></span>
<span data-ttu-id="88eb5-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="88eb5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88eb5-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="88eb5-111">-EndpointName</span></span>
<span data-ttu-id="88eb5-112">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="88eb5-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88eb5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88eb5-113">CommonParameters</span></span>
<span data-ttu-id="88eb5-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88eb5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88eb5-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88eb5-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88eb5-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88eb5-116">INPUTS</span></span>

### <span data-ttu-id="88eb5-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="88eb5-117">None</span></span>

## <span data-ttu-id="88eb5-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88eb5-118">OUTPUTS</span></span>

### <span data-ttu-id="88eb5-119">Microsoft. Azure. commands. CDN. Models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="88eb5-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="88eb5-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88eb5-120">NOTES</span></span>

## <span data-ttu-id="88eb5-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88eb5-121">RELATED LINKS</span></span>
