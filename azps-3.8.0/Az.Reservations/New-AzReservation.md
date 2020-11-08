---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090485"
---
# <span data-ttu-id="372c3-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="372c3-101">New-AzReservation</span></span>

## <span data-ttu-id="372c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="372c3-102">SYNOPSIS</span></span>
<span data-ttu-id="372c3-103">Köp en reservation</span><span class="sxs-lookup"><span data-stu-id="372c3-103">Purchase a reservation</span></span>

## <span data-ttu-id="372c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="372c3-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="372c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="372c3-105">DESCRIPTION</span></span>
<span data-ttu-id="372c3-106">Köp en reservations instans och få nytta</span><span class="sxs-lookup"><span data-stu-id="372c3-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="372c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="372c3-107">EXAMPLES</span></span>

### <span data-ttu-id="372c3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="372c3-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="372c3-109">Efter att ha beräknat pris kan kunden Purcahse att RI tillhandahåller via calculatePrice</span><span class="sxs-lookup"><span data-stu-id="372c3-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="372c3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="372c3-110">PARAMETERS</span></span>

### <span data-ttu-id="372c3-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="372c3-111">-AppliedScope</span></span>
<span data-ttu-id="372c3-112">Abonnemang som förmånen kommer att användas.</span><span class="sxs-lookup"><span data-stu-id="372c3-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="372c3-113">Obligatoriskt om--scope-Type är Single.</span><span class="sxs-lookup"><span data-stu-id="372c3-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="372c3-114">Ange inte IF--den typ av omfattning som är delad.</span><span class="sxs-lookup"><span data-stu-id="372c3-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="372c3-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="372c3-115">-AppliedScopeType</span></span>
<span data-ttu-id="372c3-116">Typ av använt scope för att uppdatera reservationen med "enkel" eller "delad"</span><span class="sxs-lookup"><span data-stu-id="372c3-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="372c3-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="372c3-117">-BillingPlan</span></span>
<span data-ttu-id="372c3-118">Alternativen för fakturerings abonnemanget för denna SKU.</span><span class="sxs-lookup"><span data-stu-id="372c3-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="372c3-119">"Månad" eller "förframen"</span><span class="sxs-lookup"><span data-stu-id="372c3-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="372c3-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="372c3-120">-BillingScopeId</span></span>
<span data-ttu-id="372c3-121">Abonnemang som kommer att debiteras för inköps reservation.</span><span class="sxs-lookup"><span data-stu-id="372c3-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="372c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372c3-122">-DefaultProfile</span></span>
<span data-ttu-id="372c3-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="372c3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="372c3-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="372c3-124">-DisplayName</span></span>
<span data-ttu-id="372c3-125">Användarvänligt namn för användaren för att identifiera reservationen.</span><span class="sxs-lookup"><span data-stu-id="372c3-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="372c3-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="372c3-126">-InstanceFlexibility</span></span>
<span data-ttu-id="372c3-127">{{Fill InstanceFlexibility Description}}</span><span class="sxs-lookup"><span data-stu-id="372c3-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="372c3-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="372c3-128">-Location</span></span>
<span data-ttu-id="372c3-129">Plats där SKU är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="372c3-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="372c3-130">-Antal</span><span class="sxs-lookup"><span data-stu-id="372c3-130">-Quantity</span></span>
<span data-ttu-id="372c3-131">Produkt antal för att beräkna priset eller inköpet.</span><span class="sxs-lookup"><span data-stu-id="372c3-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="372c3-132">-Förnya</span><span class="sxs-lookup"><span data-stu-id="372c3-132">-Renew</span></span>
<span data-ttu-id="372c3-133">Om du anger värdet till sant kommer en ny reservation automatiskt att köpas efter förfallo datum tiden.</span><span class="sxs-lookup"><span data-stu-id="372c3-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="372c3-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="372c3-134">-ReservationOrderId</span></span>
<span data-ttu-id="372c3-135">ID för reservations order att köpa, generera med AZ reservationer reservation.</span><span class="sxs-lookup"><span data-stu-id="372c3-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="372c3-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="372c3-136">-ReservedResourceType</span></span>
<span data-ttu-id="372c3-137">Typ av resurs som SKU ska tillhandahållas för.</span><span class="sxs-lookup"><span data-stu-id="372c3-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="372c3-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="372c3-138">-Sku</span></span>
<span data-ttu-id="372c3-139">SKU-namn</span><span class="sxs-lookup"><span data-stu-id="372c3-139">Sku name</span></span>

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

### <span data-ttu-id="372c3-140">-Period</span><span class="sxs-lookup"><span data-stu-id="372c3-140">-Term</span></span>
<span data-ttu-id="372c3-141">Tillgängliga reservations villkor för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="372c3-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="372c3-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="372c3-142">-Confirm</span></span>
<span data-ttu-id="372c3-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="372c3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372c3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372c3-144">-WhatIf</span></span>
<span data-ttu-id="372c3-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="372c3-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="372c3-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="372c3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372c3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372c3-147">CommonParameters</span></span>
<span data-ttu-id="372c3-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="372c3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372c3-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="372c3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372c3-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="372c3-150">INPUTS</span></span>

### <span data-ttu-id="372c3-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="372c3-151">None</span></span>

## <span data-ttu-id="372c3-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="372c3-152">OUTPUTS</span></span>

### <span data-ttu-id="372c3-153">Microsoft. Azure. Management. reservations. Models. ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="372c3-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="372c3-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="372c3-154">NOTES</span></span>

## <span data-ttu-id="372c3-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="372c3-155">RELATED LINKS</span></span>
