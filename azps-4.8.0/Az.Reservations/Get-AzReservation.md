---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262414"
---
# <span data-ttu-id="65a8a-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="65a8a-101">Get-AzReservation</span></span>

## <span data-ttu-id="65a8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="65a8a-103">Skaffa `Reservation` s på en viss reservations order</span><span class="sxs-lookup"><span data-stu-id="65a8a-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="65a8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65a8a-104">SYNTAX</span></span>

### <span data-ttu-id="65a8a-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="65a8a-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65a8a-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="65a8a-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65a8a-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="65a8a-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65a8a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65a8a-108">DESCRIPTION</span></span>
<span data-ttu-id="65a8a-109">Lista `Reservation` s inom en enda `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="65a8a-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="65a8a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65a8a-110">EXAMPLES</span></span>

### <span data-ttu-id="65a8a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="65a8a-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="65a8a-112">Lista `Reservation` s i angiven `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="65a8a-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="65a8a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="65a8a-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="65a8a-114">Få specifik `Reservation` information.</span><span class="sxs-lookup"><span data-stu-id="65a8a-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="65a8a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65a8a-115">PARAMETERS</span></span>

### <span data-ttu-id="65a8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a8a-116">-DefaultProfile</span></span>
<span data-ttu-id="65a8a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65a8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65a8a-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="65a8a-118">-ReservationId</span></span>
<span data-ttu-id="65a8a-119">ID för `Reservation` att titta på</span><span class="sxs-lookup"><span data-stu-id="65a8a-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="65a8a-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="65a8a-120">-ReservationOrder</span></span>
<span data-ttu-id="65a8a-121">Pipe-objekttyp för `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="65a8a-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="65a8a-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="65a8a-122">-ReservationOrderId</span></span>
<span data-ttu-id="65a8a-123">ID för det `ReservationOrder` som innehåller `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="65a8a-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="65a8a-124">Kunna.</span><span class="sxs-lookup"><span data-stu-id="65a8a-124">Required.</span></span>

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

### <span data-ttu-id="65a8a-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="65a8a-125">-ReservationOrderPage</span></span>
<span data-ttu-id="65a8a-126">Pipe-objekttyp för `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="65a8a-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="65a8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a8a-127">CommonParameters</span></span>
<span data-ttu-id="65a8a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a8a-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65a8a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a8a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65a8a-130">INPUTS</span></span>

### <span data-ttu-id="65a8a-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="65a8a-131">System.Guid</span></span>

### <span data-ttu-id="65a8a-132">Microsoft. Azure. commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="65a8a-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="65a8a-133">Microsoft. Azure. commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="65a8a-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="65a8a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65a8a-134">OUTPUTS</span></span>

### <span data-ttu-id="65a8a-135">Microsoft. Azure. commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="65a8a-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="65a8a-136">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="65a8a-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="65a8a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65a8a-137">NOTES</span></span>

## <span data-ttu-id="65a8a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65a8a-138">RELATED LINKS</span></span>
