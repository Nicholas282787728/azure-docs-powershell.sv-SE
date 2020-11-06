---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 3149e2fa0ef748d11583919161555805d54f5efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586311"
---
# <span data-ttu-id="7e281-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="7e281-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="7e281-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e281-102">SYNOPSIS</span></span>
<span data-ttu-id="7e281-103">Få `Reservation` revisions historik.</span><span class="sxs-lookup"><span data-stu-id="7e281-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e281-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e281-104">SYNTAX</span></span>

### <span data-ttu-id="7e281-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="7e281-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e281-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="7e281-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e281-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e281-107">DESCRIPTION</span></span>
<span data-ttu-id="7e281-108">Lista över alla ändringar för `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="7e281-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="7e281-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e281-109">EXAMPLES</span></span>

### <span data-ttu-id="7e281-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7e281-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="7e281-111">Hämta revisions historiken för en viss reservation</span><span class="sxs-lookup"><span data-stu-id="7e281-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="7e281-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e281-112">PARAMETERS</span></span>

### <span data-ttu-id="7e281-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e281-113">-DefaultProfile</span></span>
<span data-ttu-id="7e281-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e281-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e281-115">-Reservation</span><span class="sxs-lookup"><span data-stu-id="7e281-115">-Reservation</span></span>
<span data-ttu-id="7e281-116">Parametern pipe för `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="7e281-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="7e281-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="7e281-117">-ReservationId</span></span>
<span data-ttu-id="7e281-118">ReservationId som `Reservation` historiken ska visas för</span><span class="sxs-lookup"><span data-stu-id="7e281-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="7e281-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="7e281-119">-ReservationOrderId</span></span>
<span data-ttu-id="7e281-120">ReservationOrderId för den `ReservationOrder` som innehåller `Reservation`</span><span class="sxs-lookup"><span data-stu-id="7e281-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="7e281-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e281-121">CommonParameters</span></span>
<span data-ttu-id="7e281-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e281-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e281-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e281-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e281-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e281-124">INPUTS</span></span>

### <span data-ttu-id="7e281-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7e281-125">System.Guid</span></span>

### <span data-ttu-id="7e281-126">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="7e281-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="7e281-127">Parametrar: reservation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e281-127">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="7e281-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e281-128">OUTPUTS</span></span>

### <span data-ttu-id="7e281-129">Microsoft. Azure. commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="7e281-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="7e281-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e281-130">NOTES</span></span>

## <span data-ttu-id="7e281-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e281-131">RELATED LINKS</span></span>
