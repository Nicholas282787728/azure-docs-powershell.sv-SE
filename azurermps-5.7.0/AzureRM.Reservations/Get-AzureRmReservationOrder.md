---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576436"
---
# <span data-ttu-id="63f2a-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="63f2a-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="63f2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="63f2a-103">Lära `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="63f2a-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63f2a-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## <span data-ttu-id="63f2a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="63f2a-106">Lista över alla `ReservationOrder` s som användaren har till gång till i den aktuella klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="63f2a-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="63f2a-107">Om ReservationOrderId parameter är aktive rad ska du hämta specifika ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="63f2a-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="63f2a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63f2a-108">EXAMPLES</span></span>

### <span data-ttu-id="63f2a-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63f2a-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="63f2a-110">Visa alla `ReservationOrder` som användaren har åtkomst till i den aktuella klient organisationen</span><span class="sxs-lookup"><span data-stu-id="63f2a-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="63f2a-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="63f2a-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="63f2a-112">Få `ReservationOrder` med angiven ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="63f2a-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="63f2a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63f2a-113">PARAMETERS</span></span>

### <span data-ttu-id="63f2a-114">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="63f2a-114">-ReservationOrderId</span></span>
<span data-ttu-id="63f2a-115">ID för den specifika ReservationOrder som användaren vill se</span><span class="sxs-lookup"><span data-stu-id="63f2a-115">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f2a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f2a-116">CommonParameters</span></span>
<span data-ttu-id="63f2a-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f2a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f2a-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f2a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f2a-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63f2a-119">INPUTS</span></span>

### <span data-ttu-id="63f2a-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="63f2a-120">None</span></span>

## <span data-ttu-id="63f2a-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63f2a-121">OUTPUTS</span></span>

### <span data-ttu-id="63f2a-122">Microsoft. Azure. commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="63f2a-122">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="63f2a-123">Microsoft. Azure. commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="63f2a-123">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="63f2a-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63f2a-124">NOTES</span></span>

## <span data-ttu-id="63f2a-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63f2a-125">RELATED LINKS</span></span>

