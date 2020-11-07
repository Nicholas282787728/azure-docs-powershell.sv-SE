---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 987793101e89a7f628f575bf7353994756edaeae
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921502"
---
# <span data-ttu-id="45c32-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="45c32-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="45c32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45c32-102">SYNOPSIS</span></span>
<span data-ttu-id="45c32-103">Flytta abonnemang mellan delegerade leverantörs erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="45c32-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="45c32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45c32-104">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="45c32-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45c32-105">DESCRIPTION</span></span>
<span data-ttu-id="45c32-106">Flytta abonnemang mellan delegerade leverantörs erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="45c32-106">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="45c32-107">Den här processen utför bara en omanpassning, det underliggande anbudet, abonnemangen, abonnemangen för prenumerationer ändras inte.</span><span class="sxs-lookup"><span data-stu-id="45c32-107">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="45c32-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45c32-108">EXAMPLES</span></span>

### <span data-ttu-id="45c32-109">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45c32-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="45c32-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceID "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="45c32-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="45c32-111">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="45c32-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="45c32-112">$resourceIds = Get-AzsUserSubscription-filter "offerName EQ ' O1 ' | där {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select-ExpandProperty ID Move-AzsSubscription-ResourceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="45c32-112">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="45c32-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45c32-113">PARAMETERS</span></span>

### <span data-ttu-id="45c32-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45c32-114">-AsJob</span></span>
<span data-ttu-id="45c32-115">Anger om flytt åtgärden ska utföras som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="45c32-115">Specifies whether the move operation is to be executed as a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c32-116">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="45c32-116">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="45c32-117">Anger det fullständigt kvalificerade delegerade leverantörs offerter som den här cmdleten flyttar abonnemang till.</span><span class="sxs-lookup"><span data-stu-id="45c32-117">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="45c32-118">NULL om prenumerationen ska flyttas tillbaka till standardprovidern.</span><span class="sxs-lookup"><span data-stu-id="45c32-118">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c32-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45c32-119">-ResourceId</span></span>
<span data-ttu-id="45c32-120">Anger en matris med fullständigt kvalificerade prenumerations resurs-ID som denna cmdlet flyttar.</span><span class="sxs-lookup"><span data-stu-id="45c32-120">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c32-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c32-121">CommonParameters</span></span>
<span data-ttu-id="45c32-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c32-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c32-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c32-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c32-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45c32-124">INPUTS</span></span>

## <span data-ttu-id="45c32-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45c32-125">OUTPUTS</span></span>

## <span data-ttu-id="45c32-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45c32-126">NOTES</span></span>

## <span data-ttu-id="45c32-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45c32-127">RELATED LINKS</span></span>

