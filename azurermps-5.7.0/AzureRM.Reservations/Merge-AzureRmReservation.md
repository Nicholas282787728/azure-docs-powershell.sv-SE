---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576434"
---
# <span data-ttu-id="f1e4d-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="f1e4d-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="f1e4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e4d-103">Sammanfogar två `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="f1e4d-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1e4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1e4d-104">SYNTAX</span></span>

### <span data-ttu-id="f1e4d-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="f1e4d-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1e4d-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="f1e4d-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e4d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1e4d-107">DESCRIPTION</span></span>
<span data-ttu-id="f1e4d-108">Slå samman de angivna `Reservation` s till en ny `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="f1e4d-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="f1e4d-109">De två `Reservation` s som slås samman måste ha samma egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f1e4d-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="f1e4d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1e4d-110">EXAMPLES</span></span>

### <span data-ttu-id="f1e4d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f1e4d-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="f1e4d-112">Slå samman de två angivna `Reservation` s till ett `Reservation`</span><span class="sxs-lookup"><span data-stu-id="f1e4d-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="f1e4d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1e4d-113">PARAMETERS</span></span>

### <span data-ttu-id="f1e4d-114">-Reservation</span><span class="sxs-lookup"><span data-stu-id="f1e4d-114">-Reservation</span></span>
<span data-ttu-id="f1e4d-115">Kommaavgränsade strängar med två ReservationIds att sammanfoga</span><span class="sxs-lookup"><span data-stu-id="f1e4d-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e4d-116">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="f1e4d-116">-ReservationId</span></span>
<span data-ttu-id="f1e4d-117">ReservationOrderId för den `ReservationOrder` som innehåller de två `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="f1e4d-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e4d-118">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f1e4d-118">-ReservationOrderId</span></span>
<span data-ttu-id="f1e4d-119">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="f1e4d-119">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="f1e4d-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f1e4d-120">-Confirm</span></span>
<span data-ttu-id="f1e4d-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1e4d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e4d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e4d-122">-WhatIf</span></span>
<span data-ttu-id="f1e4d-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f1e4d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1e4d-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f1e4d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e4d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e4d-125">CommonParameters</span></span>
<span data-ttu-id="f1e4d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e4d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e4d-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e4d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e4d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1e4d-128">INPUTS</span></span>

### <span data-ttu-id="f1e4d-129">Microsoft. Azure. commands. reservations. Models. PSReservation []</span><span class="sxs-lookup"><span data-stu-id="f1e4d-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="f1e4d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1e4d-130">OUTPUTS</span></span>

### <span data-ttu-id="f1e4d-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. reservations. Models. PSReservation, Microsoft. Azure. commands. reservations, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f1e4d-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f1e4d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1e4d-132">NOTES</span></span>

## <span data-ttu-id="f1e4d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1e4d-133">RELATED LINKS</span></span>

