---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421048"
---
# <span data-ttu-id="a2418-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="a2418-101">Split-AzReservation</span></span>

## <span data-ttu-id="a2418-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2418-102">SYNOPSIS</span></span>
<span data-ttu-id="a2418-103">Dela en `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="a2418-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="a2418-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2418-104">SYNTAX</span></span>

### <span data-ttu-id="a2418-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="a2418-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2418-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="a2418-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2418-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2418-107">DESCRIPTION</span></span>
<span data-ttu-id="a2418-108">Dela upp en `Reservation` i två `Reservation` s med angiven mängd fördelning.</span><span class="sxs-lookup"><span data-stu-id="a2418-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="a2418-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2418-109">EXAMPLES</span></span>

### <span data-ttu-id="a2418-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2418-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="a2418-111">Dela upp angiven `Reservation` i två `Reservation` s med motsvarande antal</span><span class="sxs-lookup"><span data-stu-id="a2418-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="a2418-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2418-112">PARAMETERS</span></span>

### <span data-ttu-id="a2418-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2418-113">-DefaultProfile</span></span>
<span data-ttu-id="a2418-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2418-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2418-115">-Antal</span><span class="sxs-lookup"><span data-stu-id="a2418-115">-Quantity</span></span>
<span data-ttu-id="a2418-116">Kommaavgränsade heltal för fältet Antal för de båda `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="a2418-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="a2418-117">-Reservation</span><span class="sxs-lookup"><span data-stu-id="a2418-117">-Reservation</span></span>
<span data-ttu-id="a2418-118">Pipe-objekttyp för `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a2418-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="a2418-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="a2418-119">-ReservationId</span></span>
<span data-ttu-id="a2418-120">ID för `Reservation` att dela</span><span class="sxs-lookup"><span data-stu-id="a2418-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="a2418-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a2418-121">-ReservationOrderId</span></span>
<span data-ttu-id="a2418-122">ID för det `ReservationOrder` som innehåller den `Reservation` användare som vill dela</span><span class="sxs-lookup"><span data-stu-id="a2418-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="a2418-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2418-123">-Confirm</span></span>
<span data-ttu-id="a2418-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2418-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2418-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2418-125">-WhatIf</span></span>
<span data-ttu-id="a2418-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2418-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2418-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2418-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2418-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2418-128">CommonParameters</span></span>
<span data-ttu-id="a2418-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2418-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2418-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2418-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2418-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2418-131">INPUTS</span></span>

### <span data-ttu-id="a2418-132">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="a2418-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a2418-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2418-133">OUTPUTS</span></span>

### <span data-ttu-id="a2418-134">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="a2418-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a2418-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2418-135">NOTES</span></span>

## <span data-ttu-id="a2418-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2418-136">RELATED LINKS</span></span>
