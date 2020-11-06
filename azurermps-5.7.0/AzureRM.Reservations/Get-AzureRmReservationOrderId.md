---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576433"
---
# <span data-ttu-id="eba03-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="eba03-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="eba03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eba03-102">SYNOPSIS</span></span>
<span data-ttu-id="eba03-103">Hämta en lista över tillämpliga `ReservationOrder` ID: n.</span><span class="sxs-lookup"><span data-stu-id="eba03-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eba03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eba03-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="eba03-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eba03-105">DESCRIPTION</span></span>
<span data-ttu-id="eba03-106">Skaffa ID: n `ReservationOrder` som kan tillämpas på det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="eba03-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="eba03-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eba03-107">EXAMPLES</span></span>

### <span data-ttu-id="eba03-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eba03-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="eba03-109">Använda `ReservationOrder` för standard abonnemang</span><span class="sxs-lookup"><span data-stu-id="eba03-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="eba03-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="eba03-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="eba03-111">Använda `ReservationOrder` för angivet abonnemang</span><span class="sxs-lookup"><span data-stu-id="eba03-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="eba03-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eba03-112">PARAMETERS</span></span>

### <span data-ttu-id="eba03-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eba03-113">-SubscriptionId</span></span>
<span data-ttu-id="eba03-114">ID för abonnemanget för att få det använda `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="eba03-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="eba03-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba03-115">CommonParameters</span></span>
<span data-ttu-id="eba03-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba03-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba03-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eba03-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba03-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eba03-118">INPUTS</span></span>

### <span data-ttu-id="eba03-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="eba03-119">None</span></span>

## <span data-ttu-id="eba03-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eba03-120">OUTPUTS</span></span>

### <span data-ttu-id="eba03-121">Microsoft. Azure. commands. reservations. Models. PSAppliedReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="eba03-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="eba03-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eba03-122">NOTES</span></span>

## <span data-ttu-id="eba03-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eba03-123">RELATED LINKS</span></span>

