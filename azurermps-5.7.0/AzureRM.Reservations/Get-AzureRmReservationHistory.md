---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581012"
---
# <span data-ttu-id="20c49-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="20c49-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="20c49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20c49-102">SYNOPSIS</span></span>
<span data-ttu-id="20c49-103">Få `Reservation` revisions historik.</span><span class="sxs-lookup"><span data-stu-id="20c49-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20c49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20c49-104">SYNTAX</span></span>

### <span data-ttu-id="20c49-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="20c49-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="20c49-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="20c49-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="20c49-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20c49-107">DESCRIPTION</span></span>
<span data-ttu-id="20c49-108">Lista över alla ändringar för `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="20c49-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="20c49-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20c49-109">EXAMPLES</span></span>

### <span data-ttu-id="20c49-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20c49-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="20c49-111">Hämta revisions historiken för en viss reservation</span><span class="sxs-lookup"><span data-stu-id="20c49-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="20c49-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20c49-112">PARAMETERS</span></span>

### <span data-ttu-id="20c49-113">-Reservation</span><span class="sxs-lookup"><span data-stu-id="20c49-113">-Reservation</span></span>
<span data-ttu-id="20c49-114">Parametern pipe för `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="20c49-114">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="20c49-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="20c49-115">-ReservationId</span></span>
<span data-ttu-id="20c49-116">ReservationId som `Reservation` historiken ska visas för</span><span class="sxs-lookup"><span data-stu-id="20c49-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="20c49-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="20c49-117">-ReservationOrderId</span></span>
<span data-ttu-id="20c49-118">ReservationOrderId för den `ReservationOrder` som innehåller `Reservation`</span><span class="sxs-lookup"><span data-stu-id="20c49-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="20c49-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c49-119">CommonParameters</span></span>
<span data-ttu-id="20c49-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c49-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c49-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c49-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c49-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20c49-122">INPUTS</span></span>

### <span data-ttu-id="20c49-123">System. String</span><span class="sxs-lookup"><span data-stu-id="20c49-123">System.String</span></span>
<span data-ttu-id="20c49-124">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="20c49-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="20c49-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20c49-125">OUTPUTS</span></span>

### <span data-ttu-id="20c49-126">Microsoft. Azure. commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="20c49-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="20c49-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20c49-127">NOTES</span></span>

## <span data-ttu-id="20c49-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20c49-128">RELATED LINKS</span></span>

