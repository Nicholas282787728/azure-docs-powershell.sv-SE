---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416523"
---
# <span data-ttu-id="a3c2c-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="a3c2c-101">Merge-AzReservation</span></span>

## <span data-ttu-id="a3c2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c2c-103">Sammanfogar två `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="a3c2c-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="a3c2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3c2c-104">SYNTAX</span></span>

### <span data-ttu-id="a3c2c-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="a3c2c-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c2c-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="a3c2c-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3c2c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3c2c-107">DESCRIPTION</span></span>
<span data-ttu-id="a3c2c-108">Slå samman de angivna `Reservation` s till en ny `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="a3c2c-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="a3c2c-109">De två `Reservation` s som slås samman måste ha samma egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a3c2c-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="a3c2c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3c2c-110">EXAMPLES</span></span>

### <span data-ttu-id="a3c2c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3c2c-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="a3c2c-112">Slå samman de två angivna `Reservation` s till ett `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a3c2c-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="a3c2c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3c2c-113">PARAMETERS</span></span>

### <span data-ttu-id="a3c2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c2c-114">-DefaultProfile</span></span>
<span data-ttu-id="a3c2c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3c2c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c2c-116">-Reservation</span><span class="sxs-lookup"><span data-stu-id="a3c2c-116">-Reservation</span></span>
<span data-ttu-id="a3c2c-117">Kommaavgränsade strängar med två ReservationIds att sammanfoga</span><span class="sxs-lookup"><span data-stu-id="a3c2c-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c2c-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="a3c2c-118">-ReservationId</span></span>
<span data-ttu-id="a3c2c-119">ReservationOrderId för den `ReservationOrder` som innehåller de två `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="a3c2c-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c2c-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a3c2c-120">-ReservationOrderId</span></span>
<span data-ttu-id="a3c2c-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="a3c2c-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="a3c2c-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3c2c-122">-Confirm</span></span>
<span data-ttu-id="a3c2c-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3c2c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3c2c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c2c-124">-WhatIf</span></span>
<span data-ttu-id="a3c2c-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3c2c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3c2c-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3c2c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3c2c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c2c-127">CommonParameters</span></span>
<span data-ttu-id="a3c2c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3c2c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c2c-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3c2c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c2c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3c2c-130">INPUTS</span></span>

### <span data-ttu-id="a3c2c-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="a3c2c-131">None</span></span>

## <span data-ttu-id="a3c2c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3c2c-132">OUTPUTS</span></span>

### <span data-ttu-id="a3c2c-133">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="a3c2c-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a3c2c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3c2c-134">NOTES</span></span>

## <span data-ttu-id="a3c2c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3c2c-135">RELATED LINKS</span></span>
