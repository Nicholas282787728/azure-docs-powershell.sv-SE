---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270550"
---
# <span data-ttu-id="73d91-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="73d91-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="73d91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73d91-102">SYNOPSIS</span></span>
<span data-ttu-id="73d91-103">Skaffa en eller flera privata butiks offerter.</span><span class="sxs-lookup"><span data-stu-id="73d91-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="73d91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73d91-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73d91-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73d91-105">DESCRIPTION</span></span>
<span data-ttu-id="73d91-106">Skaffa en eller flera privata butiks erbjudanden med offentliga + privata abonnemang som har lagts till under klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="73d91-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="73d91-107">Om prenumerations-ID är upptaget kan du skaffa en eller flera privata erbjudanden med privata abonnemang endast under prenumerations omfattning</span><span class="sxs-lookup"><span data-stu-id="73d91-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="73d91-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73d91-108">EXAMPLES</span></span>

### <span data-ttu-id="73d91-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73d91-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="73d91-110">Få en privat butiks erbjudande med privata + offentliga abonnemang som har lagts till under klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="73d91-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="73d91-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="73d91-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="73d91-112">Få erbjudanden för privat butik med privata abonnemang som har lagts till under prenumerations omfattning.</span><span class="sxs-lookup"><span data-stu-id="73d91-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="73d91-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="73d91-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="73d91-114">Skaffa privat butikens bud med privata + offentliga abonnemang som har lagts till under klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="73d91-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="73d91-115">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="73d91-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="73d91-116">Få en privat butiks bud med privata abonnemang som har lagts till under innehavarens omfattning.</span><span class="sxs-lookup"><span data-stu-id="73d91-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="73d91-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73d91-117">PARAMETERS</span></span>

### <span data-ttu-id="73d91-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d91-118">-DefaultProfile</span></span>
<span data-ttu-id="73d91-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73d91-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73d91-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="73d91-120">-OfferId</span></span>
<span data-ttu-id="73d91-121">PrivateStore-utbud för Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="73d91-121">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d91-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="73d91-122">-PrivateStoreId</span></span>
<span data-ttu-id="73d91-123">Obligatoriska Azure Marketplace-privateStore erbjudanden</span><span class="sxs-lookup"><span data-stu-id="73d91-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="73d91-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73d91-124">-SubscriptionId</span></span>
<span data-ttu-id="73d91-125">Abonnemangs-ID för Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="73d91-125">Azure Marketplace subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d91-126">CommonParameters</span></span>
<span data-ttu-id="73d91-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d91-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73d91-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d91-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73d91-129">INPUTS</span></span>

### <span data-ttu-id="73d91-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="73d91-130">None</span></span>

## <span data-ttu-id="73d91-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73d91-131">OUTPUTS</span></span>

### <span data-ttu-id="73d91-132">Microsoft. Azure. commands. Marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="73d91-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="73d91-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73d91-133">NOTES</span></span>

## <span data-ttu-id="73d91-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73d91-134">RELATED LINKS</span></span>
