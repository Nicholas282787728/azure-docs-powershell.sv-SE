---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527148"
---
# <span data-ttu-id="57a6c-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="57a6c-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="57a6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="57a6c-103">Hämtar tillgänglighets status för CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="57a6c-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="57a6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57a6c-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57a6c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57a6c-105">DESCRIPTION</span></span>
<span data-ttu-id="57a6c-106">Cmdleten **Get-AzCdnEndpointNameAvailability** hämtar tillgänglighets statusen för slut punkten för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="57a6c-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="57a6c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57a6c-107">EXAMPLES</span></span>

## <span data-ttu-id="57a6c-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57a6c-108">PARAMETERS</span></span>

### <span data-ttu-id="57a6c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a6c-109">-DefaultProfile</span></span>
<span data-ttu-id="57a6c-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="57a6c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57a6c-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="57a6c-111">-EndpointName</span></span>
<span data-ttu-id="57a6c-112">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="57a6c-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="57a6c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a6c-113">CommonParameters</span></span>
<span data-ttu-id="57a6c-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a6c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a6c-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57a6c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a6c-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57a6c-116">INPUTS</span></span>

### <span data-ttu-id="57a6c-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="57a6c-117">None</span></span>

## <span data-ttu-id="57a6c-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57a6c-118">OUTPUTS</span></span>

### <span data-ttu-id="57a6c-119">Microsoft. Azure. commands. CDN. Models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="57a6c-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="57a6c-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57a6c-120">NOTES</span></span>

## <span data-ttu-id="57a6c-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57a6c-121">RELATED LINKS</span></span>
