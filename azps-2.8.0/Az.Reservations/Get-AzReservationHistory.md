---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cf68c40a13247d1101f6d25abac92f01ae1a0053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919357"
---
# <span data-ttu-id="6aecd-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="6aecd-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="6aecd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6aecd-102">SYNOPSIS</span></span>
<span data-ttu-id="6aecd-103">Få `Reservation` revisions historik.</span><span class="sxs-lookup"><span data-stu-id="6aecd-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="6aecd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6aecd-104">SYNTAX</span></span>

### <span data-ttu-id="6aecd-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="6aecd-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aecd-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="6aecd-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6aecd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6aecd-107">DESCRIPTION</span></span>
<span data-ttu-id="6aecd-108">Lista över alla ändringar för `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="6aecd-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="6aecd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6aecd-109">EXAMPLES</span></span>

### <span data-ttu-id="6aecd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6aecd-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="6aecd-111">Hämta revisions historiken för en viss reservation</span><span class="sxs-lookup"><span data-stu-id="6aecd-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="6aecd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6aecd-112">PARAMETERS</span></span>

### <span data-ttu-id="6aecd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aecd-113">-DefaultProfile</span></span>
<span data-ttu-id="6aecd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6aecd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aecd-115">-Reservation</span><span class="sxs-lookup"><span data-stu-id="6aecd-115">-Reservation</span></span>
<span data-ttu-id="6aecd-116">Parametern pipe för `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="6aecd-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="6aecd-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="6aecd-117">-ReservationId</span></span>
<span data-ttu-id="6aecd-118">ReservationId som `Reservation` historiken ska visas för</span><span class="sxs-lookup"><span data-stu-id="6aecd-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="6aecd-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6aecd-119">-ReservationOrderId</span></span>
<span data-ttu-id="6aecd-120">ReservationOrderId för den `ReservationOrder` som innehåller `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6aecd-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="6aecd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aecd-121">CommonParameters</span></span>
<span data-ttu-id="6aecd-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aecd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aecd-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aecd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aecd-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6aecd-124">INPUTS</span></span>

### <span data-ttu-id="6aecd-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6aecd-125">System.Guid</span></span>

### <span data-ttu-id="6aecd-126">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6aecd-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6aecd-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6aecd-127">OUTPUTS</span></span>

### <span data-ttu-id="6aecd-128">Microsoft. Azure. commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="6aecd-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="6aecd-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6aecd-129">NOTES</span></span>

## <span data-ttu-id="6aecd-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6aecd-130">RELATED LINKS</span></span>
