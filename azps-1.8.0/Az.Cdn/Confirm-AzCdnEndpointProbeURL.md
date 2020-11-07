---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: 10712077490831f864d94c43fe54fc6ff9f30e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917589"
---
# <span data-ttu-id="0980f-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="0980f-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="0980f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0980f-102">SYNOPSIS</span></span>
<span data-ttu-id="0980f-103">Verifierar en URL för avsökning.</span><span class="sxs-lookup"><span data-stu-id="0980f-103">Validates a probe URL.</span></span>

## <span data-ttu-id="0980f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0980f-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0980f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0980f-105">DESCRIPTION</span></span>
<span data-ttu-id="0980f-106">Cmdleten **Confirm-AzCdnEndpointProbeURL** bekräftar om den angivna avsöknings-URL: en kan användas för dynamisk webbplats acceleration.</span><span class="sxs-lookup"><span data-stu-id="0980f-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="0980f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0980f-107">EXAMPLES</span></span>

### <span data-ttu-id="0980f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0980f-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="0980f-109">Validerar URL " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="0980f-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="0980f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0980f-110">PARAMETERS</span></span>

### <span data-ttu-id="0980f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0980f-111">-DefaultProfile</span></span>
<span data-ttu-id="0980f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0980f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0980f-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="0980f-113">-ProbeUrl</span></span>
<span data-ttu-id="0980f-114">Föreslagen avsöknings-URL som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="0980f-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="0980f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0980f-115">CommonParameters</span></span>
<span data-ttu-id="0980f-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0980f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0980f-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0980f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0980f-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0980f-118">INPUTS</span></span>

### <span data-ttu-id="0980f-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="0980f-119">None</span></span>

## <span data-ttu-id="0980f-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0980f-120">OUTPUTS</span></span>

### <span data-ttu-id="0980f-121">Microsoft. Azure. commands. CDN. Models. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="0980f-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="0980f-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0980f-122">NOTES</span></span>

## <span data-ttu-id="0980f-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0980f-123">RELATED LINKS</span></span>
