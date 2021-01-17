---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 073a059063198e91a1bbcc67814c01c1b786e7c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416544"
---
# <span data-ttu-id="1bf28-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="1bf28-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="1bf28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1bf28-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf28-103">Få en offert för reservationen.</span><span class="sxs-lookup"><span data-stu-id="1bf28-103">Get a quote for the reservation.</span></span> <span data-ttu-id="1bf28-104">Detta skickas till `New-AzReservation` för att du ska kunna köpa.</span><span class="sxs-lookup"><span data-stu-id="1bf28-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="1bf28-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1bf28-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf28-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1bf28-106">DESCRIPTION</span></span>
<span data-ttu-id="1bf28-107">Beräkna priset för att placera en reservations order.</span><span class="sxs-lookup"><span data-stu-id="1bf28-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="1bf28-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1bf28-108">EXAMPLES</span></span>

### <span data-ttu-id="1bf28-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1bf28-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="1bf28-110">Efter att du har skaffat katalogen kan kunden få den olika produkten baserat på platsen.</span><span class="sxs-lookup"><span data-stu-id="1bf28-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="1bf28-111">Genom att använda informationen kontrollerar du priset korrekt</span><span class="sxs-lookup"><span data-stu-id="1bf28-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="1bf28-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1bf28-112">PARAMETERS</span></span>

### <span data-ttu-id="1bf28-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="1bf28-113">-AppliedScope</span></span>
<span data-ttu-id="1bf28-114">Abonnemang som förmånen kommer att användas.</span><span class="sxs-lookup"><span data-stu-id="1bf28-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="1bf28-115">Obligatoriskt om--scope-Type är Single.</span><span class="sxs-lookup"><span data-stu-id="1bf28-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="1bf28-116">Ange inte IF--den typ av omfattning som är delad.</span><span class="sxs-lookup"><span data-stu-id="1bf28-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="1bf28-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="1bf28-117">-AppliedScopeType</span></span>
<span data-ttu-id="1bf28-118">Typ av använt scope för att uppdatera reservationen med "enkel" eller "delad"</span><span class="sxs-lookup"><span data-stu-id="1bf28-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="1bf28-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="1bf28-119">-BillingPlan</span></span>
<span data-ttu-id="1bf28-120">Alternativen för fakturerings abonnemanget för denna SKU.</span><span class="sxs-lookup"><span data-stu-id="1bf28-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="1bf28-121">"Månad" eller "förframen"</span><span class="sxs-lookup"><span data-stu-id="1bf28-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="1bf28-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="1bf28-122">-BillingScopeId</span></span>
<span data-ttu-id="1bf28-123">Abonnemang som kommer att debiteras för inköps reservation.</span><span class="sxs-lookup"><span data-stu-id="1bf28-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="1bf28-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf28-124">-DefaultProfile</span></span>
<span data-ttu-id="1bf28-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf28-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf28-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1bf28-126">-DisplayName</span></span>
<span data-ttu-id="1bf28-127">Användarvänligt namn för användaren för att identifiera reservationen.</span><span class="sxs-lookup"><span data-stu-id="1bf28-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="1bf28-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="1bf28-128">-InstanceFlexibility</span></span>
<span data-ttu-id="1bf28-129">Typ av infalls flexibilitet att uppdatera reservationen med.</span><span class="sxs-lookup"><span data-stu-id="1bf28-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="1bf28-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="1bf28-130">-Location</span></span>
<span data-ttu-id="1bf28-131">Plats där SKU är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="1bf28-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="1bf28-132">-Antal</span><span class="sxs-lookup"><span data-stu-id="1bf28-132">-Quantity</span></span>
<span data-ttu-id="1bf28-133">Produkt antal för att beräkna priset eller inköpet.</span><span class="sxs-lookup"><span data-stu-id="1bf28-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="1bf28-134">-Förnya</span><span class="sxs-lookup"><span data-stu-id="1bf28-134">-Renew</span></span>
<span data-ttu-id="1bf28-135">Om du anger värdet till sant kommer en ny reservation automatiskt att köpas efter förfallo datum tiden.</span><span class="sxs-lookup"><span data-stu-id="1bf28-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="1bf28-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="1bf28-136">-ReservedResourceType</span></span>
<span data-ttu-id="1bf28-137">Typ av resurs som SKU ska tillhandahållas för.</span><span class="sxs-lookup"><span data-stu-id="1bf28-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="1bf28-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="1bf28-138">-Sku</span></span>
<span data-ttu-id="1bf28-139">SKU-namn, Hämta SKU-listan genom att använda kommando AZ reservationer katalog Visa</span><span class="sxs-lookup"><span data-stu-id="1bf28-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="1bf28-140">-Period</span><span class="sxs-lookup"><span data-stu-id="1bf28-140">-Term</span></span>
<span data-ttu-id="1bf28-141">Tillgängliga reservations villkor för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="1bf28-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="1bf28-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf28-142">CommonParameters</span></span>
<span data-ttu-id="1bf28-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf28-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf28-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bf28-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf28-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1bf28-145">INPUTS</span></span>

### <span data-ttu-id="1bf28-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="1bf28-146">None</span></span>

## <span data-ttu-id="1bf28-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1bf28-147">OUTPUTS</span></span>

### <span data-ttu-id="1bf28-148">Microsoft. Azure. Management. reservations. Models. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="1bf28-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="1bf28-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1bf28-149">NOTES</span></span>

## <span data-ttu-id="1bf28-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1bf28-150">RELATED LINKS</span></span>
