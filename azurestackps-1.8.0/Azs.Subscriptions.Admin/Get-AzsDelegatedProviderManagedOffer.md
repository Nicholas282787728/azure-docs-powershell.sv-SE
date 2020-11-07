---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921523"
---
# <span data-ttu-id="7ad3b-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="7ad3b-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="7ad3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ad3b-102">SYNOPSIS</span></span>
<span data-ttu-id="7ad3b-103">Hämta listan med erbjudanden för ombud.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="7ad3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ad3b-104">SYNTAX</span></span>

### <span data-ttu-id="7ad3b-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="7ad3b-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ad3b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="7ad3b-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="7ad3b-107">ID</span><span class="sxs-lookup"><span data-stu-id="7ad3b-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7ad3b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ad3b-108">DESCRIPTION</span></span>
<span data-ttu-id="7ad3b-109">Hämta listan med erbjudanden för ombud.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="7ad3b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ad3b-110">EXAMPLES</span></span>

### <span data-ttu-id="7ad3b-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7ad3b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="7ad3b-112">Hämta listan med erbjudanden för ombud.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="7ad3b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ad3b-113">PARAMETERS</span></span>

### <span data-ttu-id="7ad3b-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="7ad3b-114">-DelegatedProviderId</span></span>
<span data-ttu-id="7ad3b-115">DelegatedProvider-ID.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ad3b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ad3b-116">-Name</span></span>
<span data-ttu-id="7ad3b-117">Namn på ett bud.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ad3b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ad3b-118">-ResourceId</span></span>
<span data-ttu-id="7ad3b-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ad3b-120">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="7ad3b-120">-Skip</span></span>
<span data-ttu-id="7ad3b-121">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ad3b-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="7ad3b-122">-Top</span></span>
<span data-ttu-id="7ad3b-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7ad3b-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ad3b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ad3b-125">CommonParameters</span></span>
<span data-ttu-id="7ad3b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ad3b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ad3b-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ad3b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ad3b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ad3b-128">INPUTS</span></span>

## <span data-ttu-id="7ad3b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ad3b-129">OUTPUTS</span></span>

### <span data-ttu-id="7ad3b-130">Microsoft. AzureStack. Management. abonnemang. admin. Models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="7ad3b-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="7ad3b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ad3b-131">NOTES</span></span>

## <span data-ttu-id="7ad3b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ad3b-132">RELATED LINKS</span></span>

