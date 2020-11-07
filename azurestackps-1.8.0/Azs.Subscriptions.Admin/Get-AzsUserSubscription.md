---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921505"
---
# <span data-ttu-id="18e5e-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="18e5e-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="18e5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="18e5e-103">Hämta listan med användar abonnemang som administratör.</span><span class="sxs-lookup"><span data-stu-id="18e5e-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="18e5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18e5e-104">SYNTAX</span></span>

### <span data-ttu-id="18e5e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="18e5e-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="18e5e-106">Lära</span><span class="sxs-lookup"><span data-stu-id="18e5e-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="18e5e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="18e5e-108">Hämta listan med användar abonnemang som administratör.</span><span class="sxs-lookup"><span data-stu-id="18e5e-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="18e5e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18e5e-109">EXAMPLES</span></span>

### <span data-ttu-id="18e5e-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="18e5e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="18e5e-111">Hämta listan med användar abonnemang som administratör.</span><span class="sxs-lookup"><span data-stu-id="18e5e-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="18e5e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18e5e-112">PARAMETERS</span></span>

### <span data-ttu-id="18e5e-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="18e5e-113">-Filter</span></span>
<span data-ttu-id="18e5e-114">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="18e5e-114">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18e5e-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18e5e-115">-SubscriptionId</span></span>
<span data-ttu-id="18e5e-116">Parametern prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="18e5e-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18e5e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e5e-117">CommonParameters</span></span>
<span data-ttu-id="18e5e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e5e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e5e-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e5e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e5e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18e5e-120">INPUTS</span></span>

## <span data-ttu-id="18e5e-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18e5e-121">OUTPUTS</span></span>

### <span data-ttu-id="18e5e-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="18e5e-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="18e5e-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18e5e-123">NOTES</span></span>

## <span data-ttu-id="18e5e-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18e5e-124">RELATED LINKS</span></span>

