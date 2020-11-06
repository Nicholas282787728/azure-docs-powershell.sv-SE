---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: bc1fba5c7fa7e01a3c2461907a214809e175f3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573911"
---
# <span data-ttu-id="aeab4-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="aeab4-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="aeab4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aeab4-102">SYNOPSIS</span></span>
<span data-ttu-id="aeab4-103">Dela en `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="aeab4-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeab4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aeab4-104">SYNTAX</span></span>

### <span data-ttu-id="aeab4-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="aeab4-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeab4-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="aeab4-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Int32[]> -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeab4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aeab4-107">DESCRIPTION</span></span>
<span data-ttu-id="aeab4-108">Dela upp en `Reservation` i två `Reservation` s med angiven mängd fördelning.</span><span class="sxs-lookup"><span data-stu-id="aeab4-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="aeab4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aeab4-109">EXAMPLES</span></span>

### <span data-ttu-id="aeab4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aeab4-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="aeab4-111">Dela upp angiven `Reservation` i två `Reservation` s med motsvarande antal</span><span class="sxs-lookup"><span data-stu-id="aeab4-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="aeab4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aeab4-112">PARAMETERS</span></span>

### <span data-ttu-id="aeab4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeab4-113">-DefaultProfile</span></span>
<span data-ttu-id="aeab4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aeab4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeab4-115">-Antal</span><span class="sxs-lookup"><span data-stu-id="aeab4-115">-Quantity</span></span>
<span data-ttu-id="aeab4-116">Kommaavgränsade heltal för fältet Antal för de båda `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="aeab4-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="aeab4-117">-Reservation</span><span class="sxs-lookup"><span data-stu-id="aeab4-117">-Reservation</span></span>
<span data-ttu-id="aeab4-118">Pipe-objekttyp för `Reservation`</span><span class="sxs-lookup"><span data-stu-id="aeab4-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="aeab4-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="aeab4-119">-ReservationId</span></span>
<span data-ttu-id="aeab4-120">ID för `Reservation` att dela</span><span class="sxs-lookup"><span data-stu-id="aeab4-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="aeab4-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="aeab4-121">-ReservationOrderId</span></span>
<span data-ttu-id="aeab4-122">ID för det `ReservationOrder` som innehåller den `Reservation` användare som vill dela</span><span class="sxs-lookup"><span data-stu-id="aeab4-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="aeab4-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aeab4-123">-Confirm</span></span>
<span data-ttu-id="aeab4-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aeab4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeab4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeab4-125">-WhatIf</span></span>
<span data-ttu-id="aeab4-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aeab4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeab4-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aeab4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeab4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeab4-128">CommonParameters</span></span>
<span data-ttu-id="aeab4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeab4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeab4-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeab4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeab4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aeab4-131">INPUTS</span></span>

### <span data-ttu-id="aeab4-132">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="aeab4-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="aeab4-133">Parametrar: reservation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aeab4-133">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="aeab4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aeab4-134">OUTPUTS</span></span>

### <span data-ttu-id="aeab4-135">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="aeab4-135">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="aeab4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aeab4-136">NOTES</span></span>

## <span data-ttu-id="aeab4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aeab4-137">RELATED LINKS</span></span>
