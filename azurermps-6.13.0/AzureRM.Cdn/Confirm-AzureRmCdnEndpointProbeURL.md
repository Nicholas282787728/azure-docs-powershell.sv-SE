---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/confirm-azurermcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
ms.openlocfilehash: d6cf25c352c89592112aaa0a60cf7ba14ff7acf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578975"
---
# <span data-ttu-id="7d104-101">Confirm-AzureRmCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="7d104-101">Confirm-AzureRmCdnEndpointProbeURL</span></span>

## <span data-ttu-id="7d104-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d104-102">SYNOPSIS</span></span>
<span data-ttu-id="7d104-103">Verifierar en URL för avsökning.</span><span class="sxs-lookup"><span data-stu-id="7d104-103">Validates a probe URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d104-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d104-104">SYNTAX</span></span>

```
Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d104-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d104-105">DESCRIPTION</span></span>
<span data-ttu-id="7d104-106">Cmdleten **Confirm-AzureRmCdnEndpointProbeURL** bekräftar om den angivna avsöknings-URL: en kan användas för dynamisk webbplats acceleration.</span><span class="sxs-lookup"><span data-stu-id="7d104-106">The **Confirm-AzureRmCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="7d104-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d104-107">EXAMPLES</span></span>

### <span data-ttu-id="7d104-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d104-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="7d104-109">Validerar URL " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="7d104-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="7d104-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d104-110">PARAMETERS</span></span>

### <span data-ttu-id="7d104-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d104-111">-DefaultProfile</span></span>
<span data-ttu-id="7d104-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d104-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d104-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="7d104-113">-ProbeUrl</span></span>
<span data-ttu-id="7d104-114">Föreslagen avsöknings-URL som ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="7d104-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="7d104-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d104-115">CommonParameters</span></span>
<span data-ttu-id="7d104-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d104-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d104-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d104-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d104-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d104-118">INPUTS</span></span>

### <span data-ttu-id="7d104-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="7d104-119">None</span></span>

## <span data-ttu-id="7d104-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d104-120">OUTPUTS</span></span>

### <span data-ttu-id="7d104-121">Microsoft. Azure. commands. CDN. Models. Endpoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="7d104-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="7d104-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d104-122">NOTES</span></span>

## <span data-ttu-id="7d104-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d104-123">RELATED LINKS</span></span>
