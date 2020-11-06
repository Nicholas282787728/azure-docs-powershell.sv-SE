---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573312"
---
# <span data-ttu-id="2ee74-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="2ee74-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="2ee74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ee74-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee74-103">Skaffa `Reservation` s på en viss reservations order</span><span class="sxs-lookup"><span data-stu-id="2ee74-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ee74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ee74-104">SYNTAX</span></span>

### <span data-ttu-id="2ee74-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="2ee74-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ee74-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="2ee74-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="2ee74-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ee74-107">DESCRIPTION</span></span>
<span data-ttu-id="2ee74-108">Lista `Reservation` s inom en enda `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="2ee74-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="2ee74-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ee74-109">EXAMPLES</span></span>

### <span data-ttu-id="2ee74-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2ee74-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="2ee74-111">Lista `Reservation` s i angiven `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="2ee74-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="2ee74-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2ee74-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="2ee74-113">Få specifik `Reservation` information.</span><span class="sxs-lookup"><span data-stu-id="2ee74-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="2ee74-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ee74-114">PARAMETERS</span></span>

### <span data-ttu-id="2ee74-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="2ee74-115">-ReservationId</span></span>
<span data-ttu-id="2ee74-116">ID för `Reservation` att titta på</span><span class="sxs-lookup"><span data-stu-id="2ee74-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee74-117">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="2ee74-117">-ReservationOrder</span></span>
<span data-ttu-id="2ee74-118">Pipe-objekttyp för `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="2ee74-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee74-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="2ee74-119">-ReservationOrderId</span></span>
<span data-ttu-id="2ee74-120">ID för det `ReservationOrder` som innehåller `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="2ee74-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="2ee74-121">Kunna.</span><span class="sxs-lookup"><span data-stu-id="2ee74-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee74-122">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="2ee74-122">-ReservationOrderPage</span></span>
<span data-ttu-id="2ee74-123">Pipe-objekttyp för `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="2ee74-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee74-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee74-124">CommonParameters</span></span>
<span data-ttu-id="2ee74-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee74-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee74-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee74-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee74-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ee74-127">INPUTS</span></span>

### <span data-ttu-id="2ee74-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee74-128">System.String</span></span>
<span data-ttu-id="2ee74-129">Microsoft. Azure. commands. reservations. Models. PSReservationOrder Microsoft. Azure. commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="2ee74-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="2ee74-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ee74-130">OUTPUTS</span></span>

### <span data-ttu-id="2ee74-131">Microsoft. Azure. commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="2ee74-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="2ee74-132">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="2ee74-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="2ee74-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ee74-133">NOTES</span></span>

## <span data-ttu-id="2ee74-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ee74-134">RELATED LINKS</span></span>

