---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 1003dcf38815be8daba8b0e218dbca430a89f9e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573916"
---
# <span data-ttu-id="d0adc-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="d0adc-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="d0adc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0adc-102">SYNOPSIS</span></span>
<span data-ttu-id="d0adc-103">Skaffa `Reservation` s på en viss reservations order</span><span class="sxs-lookup"><span data-stu-id="d0adc-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0adc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0adc-104">SYNTAX</span></span>

### <span data-ttu-id="d0adc-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="d0adc-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <Guid> [-ReservationId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0adc-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d0adc-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0adc-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="d0adc-107">PagePipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrderPage <PSReservationOrderPage>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0adc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0adc-108">DESCRIPTION</span></span>
<span data-ttu-id="d0adc-109">Lista `Reservation` s inom en enda `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="d0adc-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="d0adc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0adc-110">EXAMPLES</span></span>

### <span data-ttu-id="d0adc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0adc-111">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="d0adc-112">Lista `Reservation` s i angiven `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="d0adc-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="d0adc-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d0adc-113">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="d0adc-114">Få specifik `Reservation` information.</span><span class="sxs-lookup"><span data-stu-id="d0adc-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="d0adc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0adc-115">PARAMETERS</span></span>

### <span data-ttu-id="d0adc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0adc-116">-DefaultProfile</span></span>
<span data-ttu-id="d0adc-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0adc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0adc-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d0adc-118">-ReservationId</span></span>
<span data-ttu-id="d0adc-119">ID för `Reservation` att titta på</span><span class="sxs-lookup"><span data-stu-id="d0adc-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0adc-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d0adc-120">-ReservationOrder</span></span>
<span data-ttu-id="d0adc-121">Pipe-objekttyp för `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d0adc-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0adc-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d0adc-122">-ReservationOrderId</span></span>
<span data-ttu-id="d0adc-123">ID för det `ReservationOrder` som innehåller `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d0adc-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="d0adc-124">Kunna.</span><span class="sxs-lookup"><span data-stu-id="d0adc-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0adc-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="d0adc-125">-ReservationOrderPage</span></span>
<span data-ttu-id="d0adc-126">Pipe-objekttyp för `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d0adc-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0adc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0adc-127">CommonParameters</span></span>
<span data-ttu-id="d0adc-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0adc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0adc-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0adc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0adc-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0adc-130">INPUTS</span></span>

### <span data-ttu-id="d0adc-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d0adc-131">System.Guid</span></span>

### <span data-ttu-id="d0adc-132">Microsoft. Azure. commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d0adc-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>
<span data-ttu-id="d0adc-133">Parametrar: ReservationOrder (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0adc-133">Parameters: ReservationOrder (ByValue)</span></span>

### <span data-ttu-id="d0adc-134">Microsoft. Azure. commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="d0adc-134">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="d0adc-135">Parametrar: ReservationOrderPage (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0adc-135">Parameters: ReservationOrderPage (ByValue)</span></span>

## <span data-ttu-id="d0adc-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0adc-136">OUTPUTS</span></span>

### <span data-ttu-id="d0adc-137">Microsoft. Azure. commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="d0adc-137">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="d0adc-138">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d0adc-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d0adc-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0adc-139">NOTES</span></span>

## <span data-ttu-id="d0adc-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0adc-140">RELATED LINKS</span></span>
