---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089042"
---
# <span data-ttu-id="e19b3-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="e19b3-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="e19b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e19b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e19b3-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="e19b3-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="e19b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e19b3-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e19b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e19b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e19b3-106">Beräkna priset för att placera en reservations order.</span><span class="sxs-lookup"><span data-stu-id="e19b3-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="e19b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e19b3-107">EXAMPLES</span></span>

### <span data-ttu-id="e19b3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e19b3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="e19b3-109">Efter att du har skaffat katalogen kan kunden få den olika produkten baserat på platsen.</span><span class="sxs-lookup"><span data-stu-id="e19b3-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="e19b3-110">Genom att använda informationen kontrollerar du priset korrekt</span><span class="sxs-lookup"><span data-stu-id="e19b3-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="e19b3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e19b3-111">PARAMETERS</span></span>

### <span data-ttu-id="e19b3-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="e19b3-112">-AppliedScope</span></span>
<span data-ttu-id="e19b3-113">Abonnemang som förmånen kommer att användas.</span><span class="sxs-lookup"><span data-stu-id="e19b3-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="e19b3-114">Obligatoriskt om--scope-Type är Single.</span><span class="sxs-lookup"><span data-stu-id="e19b3-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="e19b3-115">Ange inte IF--den typ av omfattning som är delad.</span><span class="sxs-lookup"><span data-stu-id="e19b3-115">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="e19b3-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="e19b3-116">-AppliedScopeType</span></span>
<span data-ttu-id="e19b3-117">Typ av använt scope för att uppdatera reservationen med "enkel" eller "delad"</span><span class="sxs-lookup"><span data-stu-id="e19b3-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="e19b3-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="e19b3-118">-BillingPlan</span></span>
<span data-ttu-id="e19b3-119">Alternativen för fakturerings abonnemanget för denna SKU.</span><span class="sxs-lookup"><span data-stu-id="e19b3-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="e19b3-120">"Månad" eller "förframen"</span><span class="sxs-lookup"><span data-stu-id="e19b3-120">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="e19b3-121">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="e19b3-121">-BillingScopeId</span></span>
<span data-ttu-id="e19b3-122">Abonnemang som kommer att debiteras för inköps reservation.</span><span class="sxs-lookup"><span data-stu-id="e19b3-122">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="e19b3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19b3-123">-DefaultProfile</span></span>
<span data-ttu-id="e19b3-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e19b3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e19b3-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e19b3-125">-DisplayName</span></span>
<span data-ttu-id="e19b3-126">Användarvänligt namn för användaren för att identifiera reservationen.</span><span class="sxs-lookup"><span data-stu-id="e19b3-126">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="e19b3-127">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="e19b3-127">-InstanceFlexibility</span></span>
<span data-ttu-id="e19b3-128">Typ av infalls flexibilitet att uppdatera reservationen med.</span><span class="sxs-lookup"><span data-stu-id="e19b3-128">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="e19b3-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="e19b3-129">-Location</span></span>
<span data-ttu-id="e19b3-130">Plats där SKU är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="e19b3-130">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="e19b3-131">-Antal</span><span class="sxs-lookup"><span data-stu-id="e19b3-131">-Quantity</span></span>
<span data-ttu-id="e19b3-132">Produkt antal för att beräkna priset eller inköpet.</span><span class="sxs-lookup"><span data-stu-id="e19b3-132">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e19b3-133">-Förnya</span><span class="sxs-lookup"><span data-stu-id="e19b3-133">-Renew</span></span>
<span data-ttu-id="e19b3-134">Om du anger värdet till sant kommer en ny reservation automatiskt att köpas efter förfallo datum tiden.</span><span class="sxs-lookup"><span data-stu-id="e19b3-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e19b3-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="e19b3-135">-ReservedResourceType</span></span>
<span data-ttu-id="e19b3-136">Typ av resurs som SKU ska tillhandahållas för.</span><span class="sxs-lookup"><span data-stu-id="e19b3-136">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="e19b3-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="e19b3-137">-Sku</span></span>
<span data-ttu-id="e19b3-138">SKU-namn, Hämta SKU-listan genom att använda kommando AZ reservationer katalog Visa</span><span class="sxs-lookup"><span data-stu-id="e19b3-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="e19b3-139">-Period</span><span class="sxs-lookup"><span data-stu-id="e19b3-139">-Term</span></span>
<span data-ttu-id="e19b3-140">Tillgängliga reservations villkor för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="e19b3-140">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="e19b3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19b3-141">CommonParameters</span></span>
<span data-ttu-id="e19b3-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e19b3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19b3-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e19b3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19b3-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e19b3-144">INPUTS</span></span>

### <span data-ttu-id="e19b3-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="e19b3-145">None</span></span>

## <span data-ttu-id="e19b3-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e19b3-146">OUTPUTS</span></span>

### <span data-ttu-id="e19b3-147">Microsoft. Azure. Management. reservations. Models. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="e19b3-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="e19b3-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e19b3-148">NOTES</span></span>

## <span data-ttu-id="e19b3-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e19b3-149">RELATED LINKS</span></span>
