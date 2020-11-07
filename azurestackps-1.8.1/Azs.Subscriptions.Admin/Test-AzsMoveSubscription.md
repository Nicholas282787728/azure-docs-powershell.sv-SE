---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921625"
---
# <span data-ttu-id="29665-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="29665-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="29665-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29665-102">SYNOPSIS</span></span>
<span data-ttu-id="29665-103">Verifiera att användar prenumerationer kan flyttas mellan erbjudna leverantörs erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="29665-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="29665-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29665-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="29665-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29665-105">DESCRIPTION</span></span>
<span data-ttu-id="29665-106">Verifiera att användar prenumerationer kan flyttas mellan erbjudna leverantörs erbjudanden.</span><span class="sxs-lookup"><span data-stu-id="29665-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="29665-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29665-107">EXAMPLES</span></span>

### <span data-ttu-id="29665-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="29665-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="29665-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceID "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/Subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="29665-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="29665-110">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="29665-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="29665-111">$resourceIds = Get-AzsUserSubscription-filter "offerName EQ ' O1 ' | Select-ExpandProperty ID Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="29665-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="29665-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29665-112">PARAMETERS</span></span>

### <span data-ttu-id="29665-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29665-113">-AsJob</span></span>
<span data-ttu-id="29665-114">Anger om flytt åtgärden ska utföras som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="29665-114">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="29665-115">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="29665-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="29665-116">Anger det fullständigt kvalificerade delegerade leverantörs offerter som den här cmdleten flyttar abonnemang till.</span><span class="sxs-lookup"><span data-stu-id="29665-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="29665-117">NULL om prenumerationen ska flyttas tillbaka till standardprovidern.</span><span class="sxs-lookup"><span data-stu-id="29665-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="29665-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29665-118">-ResourceId</span></span>
<span data-ttu-id="29665-119">Anger en matris med fullständigt kvalificerade prenumerations resurs-ID som denna cmdlet flyttar.</span><span class="sxs-lookup"><span data-stu-id="29665-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="29665-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29665-120">CommonParameters</span></span>
<span data-ttu-id="29665-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29665-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29665-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29665-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29665-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29665-123">INPUTS</span></span>

## <span data-ttu-id="29665-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29665-124">OUTPUTS</span></span>

## <span data-ttu-id="29665-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29665-125">NOTES</span></span>

## <span data-ttu-id="29665-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29665-126">RELATED LINKS</span></span>

