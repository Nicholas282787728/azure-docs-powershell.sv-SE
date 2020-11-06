---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: c5db5d27edb537602638ff5654a6da3ac35813ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580836"
---
# <span data-ttu-id="1c2e7-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1c2e7-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="1c2e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2e7-103">Hämtar tillgänglighets status för CDN-slutpunkten.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c2e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c2e7-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c2e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c2e7-105">DESCRIPTION</span></span>
<span data-ttu-id="1c2e7-106">Cmdleten **Get-AzureRmCdnEndpointNameAvailability** hämtar tillgänglighets statusen för slut punkten för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="1c2e7-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1c2e7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c2e7-107">EXAMPLES</span></span>

## <span data-ttu-id="1c2e7-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c2e7-108">PARAMETERS</span></span>

### <span data-ttu-id="1c2e7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2e7-109">-DefaultProfile</span></span>
<span data-ttu-id="1c2e7-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1c2e7-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c2e7-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1c2e7-111">-EndpointName</span></span>
<span data-ttu-id="1c2e7-112">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="1c2e7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2e7-113">CommonParameters</span></span>
<span data-ttu-id="1c2e7-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2e7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2e7-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c2e7-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2e7-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c2e7-116">INPUTS</span></span>

### <span data-ttu-id="1c2e7-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="1c2e7-117">None</span></span>

## <span data-ttu-id="1c2e7-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c2e7-118">OUTPUTS</span></span>

### <span data-ttu-id="1c2e7-119">Microsoft. Azure. commands. CDN. Models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="1c2e7-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="1c2e7-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c2e7-120">NOTES</span></span>

## <span data-ttu-id="1c2e7-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c2e7-121">RELATED LINKS</span></span>
