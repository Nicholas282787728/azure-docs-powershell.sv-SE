---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 395ee4b20ae2c26d05ad66489b3c643d0f4245a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578940"
---
# <span data-ttu-id="5bf3a-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5bf3a-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="5bf3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bf3a-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf3a-103">Uppdaterar en CDN Origin Server.</span><span class="sxs-lookup"><span data-stu-id="5bf3a-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bf3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bf3a-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bf3a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bf3a-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf3a-106">Cmdleten **set-AzureRmCdnOrigin** uppdaterar en Origine-Server för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="5bf3a-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="5bf3a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bf3a-107">EXAMPLES</span></span>

## <span data-ttu-id="5bf3a-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bf3a-108">PARAMETERS</span></span>

### <span data-ttu-id="5bf3a-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5bf3a-109">-CdnOrigin</span></span>
<span data-ttu-id="5bf3a-110">Anger den ursprungs server som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="5bf3a-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf3a-111">-DefaultProfile</span></span>
<span data-ttu-id="5bf3a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5bf3a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bf3a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf3a-113">CommonParameters</span></span>
<span data-ttu-id="5bf3a-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf3a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf3a-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf3a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf3a-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bf3a-116">INPUTS</span></span>

### <span data-ttu-id="5bf3a-117">Microsoft. Azure. commands. CDN. Models. ORIGIN. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="5bf3a-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>
<span data-ttu-id="5bf3a-118">Parametrar: CdnOrigin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5bf3a-118">Parameters: CdnOrigin (ByValue)</span></span>

## <span data-ttu-id="5bf3a-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bf3a-119">OUTPUTS</span></span>

### <span data-ttu-id="5bf3a-120">Microsoft. Azure. commands. CDN. Models. ORIGIN. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="5bf3a-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="5bf3a-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bf3a-121">NOTES</span></span>

## <span data-ttu-id="5bf3a-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bf3a-122">RELATED LINKS</span></span>

[<span data-ttu-id="5bf3a-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5bf3a-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


