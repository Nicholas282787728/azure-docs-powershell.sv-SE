---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 71f5732f7473a90af0509d2e3932ca5151ef870a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745296"
---
# <span data-ttu-id="4b9a7-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="4b9a7-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="4b9a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9a7-103">Uppdaterar en CDN Origin Server.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="4b9a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b9a7-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b9a7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b9a7-105">DESCRIPTION</span></span>
<span data-ttu-id="4b9a7-106">Cmdleten **set-AzCdnOrigin** uppdaterar en Origine-Server för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="4b9a7-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="4b9a7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b9a7-107">EXAMPLES</span></span>

## <span data-ttu-id="4b9a7-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b9a7-108">PARAMETERS</span></span>

### <span data-ttu-id="4b9a7-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="4b9a7-109">-CdnOrigin</span></span>
<span data-ttu-id="4b9a7-110">Anger den ursprungs server som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="4b9a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b9a7-111">-DefaultProfile</span></span>
<span data-ttu-id="4b9a7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4b9a7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b9a7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9a7-113">CommonParameters</span></span>
<span data-ttu-id="4b9a7-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9a7-115">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b9a7-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9a7-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b9a7-116">INPUTS</span></span>

### <span data-ttu-id="4b9a7-117">Microsoft. Azure. commands. CDN. Models. ORIGIN. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="4b9a7-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="4b9a7-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b9a7-118">OUTPUTS</span></span>

### <span data-ttu-id="4b9a7-119">Microsoft. Azure. commands. CDN. Models. ORIGIN. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="4b9a7-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="4b9a7-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b9a7-120">NOTES</span></span>

## <span data-ttu-id="4b9a7-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b9a7-121">RELATED LINKS</span></span>

[<span data-ttu-id="4b9a7-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="4b9a7-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


