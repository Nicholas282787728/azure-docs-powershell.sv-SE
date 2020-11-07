---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921895"
---
# <span data-ttu-id="15754-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="15754-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="15754-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15754-102">SYNOPSIS</span></span>
<span data-ttu-id="15754-103">Hämta listan med delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="15754-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="15754-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15754-104">SYNTAX</span></span>

### <span data-ttu-id="15754-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="15754-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="15754-106">Lära</span><span class="sxs-lookup"><span data-stu-id="15754-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="15754-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15754-107">DESCRIPTION</span></span>
<span data-ttu-id="15754-108">Hämta listan med delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="15754-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="15754-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15754-109">EXAMPLES</span></span>

### <span data-ttu-id="15754-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="15754-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="15754-111">Få en lista med delegerade providrar.</span><span class="sxs-lookup"><span data-stu-id="15754-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="15754-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="15754-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="15754-113">Skaffa en specifik delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="15754-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="15754-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15754-114">PARAMETERS</span></span>

### <span data-ttu-id="15754-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="15754-115">-DelegatedProviderId</span></span>
<span data-ttu-id="15754-116">{{Fill DelegatedProviderId Description}}</span><span class="sxs-lookup"><span data-stu-id="15754-116">{{Fill DelegatedProviderId Description}}</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15754-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15754-117">CommonParameters</span></span>
<span data-ttu-id="15754-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15754-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15754-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15754-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15754-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15754-120">INPUTS</span></span>

## <span data-ttu-id="15754-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15754-121">OUTPUTS</span></span>

### <span data-ttu-id="15754-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="15754-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="15754-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15754-123">NOTES</span></span>

## <span data-ttu-id="15754-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15754-124">RELATED LINKS</span></span>

