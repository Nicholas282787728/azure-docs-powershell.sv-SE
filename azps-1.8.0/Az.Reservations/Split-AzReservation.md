---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: 1345978ac502d0c7d576b56f720bd16ca704e062
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747194"
---
# <span data-ttu-id="6a56a-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="6a56a-101">Split-AzReservation</span></span>

## <span data-ttu-id="6a56a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a56a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a56a-103">Dela en `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="6a56a-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="6a56a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a56a-104">SYNTAX</span></span>

### <span data-ttu-id="6a56a-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="6a56a-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a56a-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="6a56a-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a56a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a56a-107">DESCRIPTION</span></span>
<span data-ttu-id="6a56a-108">Dela upp en `Reservation` i två `Reservation` s med angiven mängd fördelning.</span><span class="sxs-lookup"><span data-stu-id="6a56a-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="6a56a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a56a-109">EXAMPLES</span></span>

### <span data-ttu-id="6a56a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6a56a-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="6a56a-111">Dela upp angiven `Reservation` i två `Reservation` s med motsvarande antal</span><span class="sxs-lookup"><span data-stu-id="6a56a-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="6a56a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a56a-112">PARAMETERS</span></span>

### <span data-ttu-id="6a56a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a56a-113">-DefaultProfile</span></span>
<span data-ttu-id="6a56a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a56a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a56a-115">-Antal</span><span class="sxs-lookup"><span data-stu-id="6a56a-115">-Quantity</span></span>
<span data-ttu-id="6a56a-116">Kommaavgränsade heltal för fältet Antal för de båda `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="6a56a-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a56a-117">-Reservation</span><span class="sxs-lookup"><span data-stu-id="6a56a-117">-Reservation</span></span>
<span data-ttu-id="6a56a-118">Pipe-objekttyp för `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6a56a-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a56a-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="6a56a-119">-ReservationId</span></span>
<span data-ttu-id="6a56a-120">ID för `Reservation` att dela</span><span class="sxs-lookup"><span data-stu-id="6a56a-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a56a-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6a56a-121">-ReservationOrderId</span></span>
<span data-ttu-id="6a56a-122">ID för det `ReservationOrder` som innehåller den `Reservation` användare som vill dela</span><span class="sxs-lookup"><span data-stu-id="6a56a-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a56a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a56a-123">-Confirm</span></span>
<span data-ttu-id="6a56a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a56a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a56a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a56a-125">-WhatIf</span></span>
<span data-ttu-id="6a56a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a56a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a56a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a56a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a56a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a56a-128">CommonParameters</span></span>
<span data-ttu-id="6a56a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a56a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a56a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a56a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a56a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a56a-131">INPUTS</span></span>

### <span data-ttu-id="6a56a-132">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6a56a-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6a56a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a56a-133">OUTPUTS</span></span>

### <span data-ttu-id="6a56a-134">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6a56a-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6a56a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a56a-135">NOTES</span></span>

## <span data-ttu-id="6a56a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a56a-136">RELATED LINKS</span></span>
