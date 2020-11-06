---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576435"
---
# <span data-ttu-id="f9abc-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="f9abc-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="f9abc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9abc-102">SYNOPSIS</span></span>
<span data-ttu-id="f9abc-103">Dela en `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="f9abc-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9abc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9abc-104">SYNTAX</span></span>

### <span data-ttu-id="f9abc-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="f9abc-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9abc-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="f9abc-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9abc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9abc-107">DESCRIPTION</span></span>
<span data-ttu-id="f9abc-108">Dela upp en `Reservation` i två `Reservation` s med angiven mängd fördelning.</span><span class="sxs-lookup"><span data-stu-id="f9abc-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="f9abc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9abc-109">EXAMPLES</span></span>

### <span data-ttu-id="f9abc-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f9abc-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="f9abc-111">Dela upp angiven `Reservation` i två `Reservation` s med motsvarande antal</span><span class="sxs-lookup"><span data-stu-id="f9abc-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="f9abc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9abc-112">PARAMETERS</span></span>

### <span data-ttu-id="f9abc-113">-Antal</span><span class="sxs-lookup"><span data-stu-id="f9abc-113">-Quantity</span></span>
<span data-ttu-id="f9abc-114">Kommaavgränsade heltal för fältet Antal för de båda `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="f9abc-114">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9abc-115">-Reservation</span><span class="sxs-lookup"><span data-stu-id="f9abc-115">-Reservation</span></span>
<span data-ttu-id="f9abc-116">Pipe-objekttyp för `Reservation`</span><span class="sxs-lookup"><span data-stu-id="f9abc-116">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9abc-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="f9abc-117">-ReservationId</span></span>
<span data-ttu-id="f9abc-118">ID för `Reservation` att dela</span><span class="sxs-lookup"><span data-stu-id="f9abc-118">Id of the `Reservation` to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9abc-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f9abc-119">-ReservationOrderId</span></span>
<span data-ttu-id="f9abc-120">ID för det `ReservationOrder` som innehåller den `Reservation` användare som vill dela</span><span class="sxs-lookup"><span data-stu-id="f9abc-120">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9abc-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f9abc-121">-Confirm</span></span>
<span data-ttu-id="f9abc-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f9abc-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9abc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9abc-123">-WhatIf</span></span>
<span data-ttu-id="f9abc-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f9abc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9abc-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f9abc-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9abc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9abc-126">CommonParameters</span></span>
<span data-ttu-id="f9abc-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9abc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9abc-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9abc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9abc-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9abc-129">INPUTS</span></span>

### <span data-ttu-id="f9abc-130">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="f9abc-130">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="f9abc-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9abc-131">OUTPUTS</span></span>

### <span data-ttu-id="f9abc-132">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. reservations. Models. PSReservation, Microsoft. Azure. commands. reservations, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f9abc-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f9abc-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9abc-133">NOTES</span></span>

## <span data-ttu-id="f9abc-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9abc-134">RELATED LINKS</span></span>

