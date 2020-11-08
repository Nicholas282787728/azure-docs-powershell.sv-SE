---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261241"
---
# <span data-ttu-id="d425e-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="d425e-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="d425e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d425e-102">SYNOPSIS</span></span>
<span data-ttu-id="d425e-103">Uppdaterar eller skapar ett anbud för privat lagring.</span><span class="sxs-lookup"><span data-stu-id="d425e-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="d425e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d425e-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d425e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d425e-105">DESCRIPTION</span></span>
<span data-ttu-id="d425e-106">Uppdaterar eller skapar ett anbud för privat lagring som har skapats under klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="d425e-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="d425e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d425e-107">EXAMPLES</span></span>

### <span data-ttu-id="d425e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d425e-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="d425e-109">Skapar ett utbud med privata + offentliga abonnemang för privat lagring som har skapats under klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="d425e-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="d425e-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d425e-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="d425e-111">Skapar bara erbjudande med privata abonnemang för privat lagring som har skapats under prenumerations omfattning.</span><span class="sxs-lookup"><span data-stu-id="d425e-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="d425e-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d425e-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="d425e-113">Uppdaterings erbjudanden med privata + offentliga abonnemang för privat lagring som har skapats under klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="d425e-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="d425e-114">Etag behövs.</span><span class="sxs-lookup"><span data-stu-id="d425e-114">Etag is needed.</span></span>

### <span data-ttu-id="d425e-115">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="d425e-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="d425e-116">Uppdatering erbjudande för privat lagring med privata abonnemang som har skapats under prenumerationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="d425e-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="d425e-117">Etag behövs.</span><span class="sxs-lookup"><span data-stu-id="d425e-117">Etag is needed.</span></span>


## <span data-ttu-id="d425e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d425e-118">PARAMETERS</span></span>

### <span data-ttu-id="d425e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d425e-119">-DefaultProfile</span></span>
<span data-ttu-id="d425e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d425e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d425e-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="d425e-121">-ETag</span></span>
<span data-ttu-id="d425e-122">ETag för Azure Marketplace-privateStore för uppdatering</span><span class="sxs-lookup"><span data-stu-id="d425e-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="d425e-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="d425e-123">-OfferId</span></span>
<span data-ttu-id="d425e-124">PrivateStore-utbud för Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="d425e-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="d425e-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="d425e-125">-PrivateStoreId</span></span>
<span data-ttu-id="d425e-126">Obligatoriska Azure Marketplace-privateStore erbjudanden</span><span class="sxs-lookup"><span data-stu-id="d425e-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="d425e-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="d425e-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="d425e-128">Obligatoriska ID-begränsningar för Azure Marketplace-privateStore</span><span class="sxs-lookup"><span data-stu-id="d425e-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d425e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d425e-129">-Confirm</span></span>
<span data-ttu-id="d425e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d425e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d425e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d425e-131">-WhatIf</span></span>
<span data-ttu-id="d425e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d425e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d425e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d425e-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d425e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d425e-134">CommonParameters</span></span>
<span data-ttu-id="d425e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d425e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d425e-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d425e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d425e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d425e-137">INPUTS</span></span>

### <span data-ttu-id="d425e-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="d425e-138">None</span></span>

## <span data-ttu-id="d425e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d425e-139">OUTPUTS</span></span>

### <span data-ttu-id="d425e-140">Microsoft. Azure. commands. Marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="d425e-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="d425e-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d425e-141">NOTES</span></span>

## <span data-ttu-id="d425e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d425e-142">RELATED LINKS</span></span>
