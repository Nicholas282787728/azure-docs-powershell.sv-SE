---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743550"
---
# <span data-ttu-id="f6f5d-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="f6f5d-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="f6f5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f5d-103">Hämta listan med delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="f6f5d-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="f6f5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6f5d-104">SYNTAX</span></span>

### <span data-ttu-id="f6f5d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="f6f5d-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="f6f5d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="f6f5d-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="f6f5d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6f5d-107">DESCRIPTION</span></span>
<span data-ttu-id="f6f5d-108">Hämta listan med delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="f6f5d-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="f6f5d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6f5d-109">EXAMPLES</span></span>

### <span data-ttu-id="f6f5d-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f6f5d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="f6f5d-111">Få en lista med delegerade providrar.</span><span class="sxs-lookup"><span data-stu-id="f6f5d-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="f6f5d-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f6f5d-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="f6f5d-113">Skaffa en specifik delegerad leverantör.</span><span class="sxs-lookup"><span data-stu-id="f6f5d-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="f6f5d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6f5d-114">PARAMETERS</span></span>

### <span data-ttu-id="f6f5d-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="f6f5d-115">-DelegatedProviderId</span></span>
<span data-ttu-id="f6f5d-116">DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="f6f5d-116">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="f6f5d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f5d-117">CommonParameters</span></span>
<span data-ttu-id="f6f5d-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f5d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f5d-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6f5d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f5d-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6f5d-120">INPUTS</span></span>

## <span data-ttu-id="f6f5d-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6f5d-121">OUTPUTS</span></span>

### <span data-ttu-id="f6f5d-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="f6f5d-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="f6f5d-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6f5d-123">NOTES</span></span>

## <span data-ttu-id="f6f5d-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6f5d-124">RELATED LINKS</span></span>

