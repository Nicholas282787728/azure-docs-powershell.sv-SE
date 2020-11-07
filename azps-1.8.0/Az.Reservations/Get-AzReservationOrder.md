---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 3db5c7bf9665498236c3d0dacf05107926ed45eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747205"
---
# <span data-ttu-id="e71de-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="e71de-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="e71de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e71de-102">SYNOPSIS</span></span>
<span data-ttu-id="e71de-103">Lära `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="e71de-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="e71de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e71de-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e71de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e71de-105">DESCRIPTION</span></span>
<span data-ttu-id="e71de-106">Lista över alla `ReservationOrder` s som användaren har till gång till i den aktuella klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="e71de-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="e71de-107">Om ReservationOrderId parameter är aktive rad ska du hämta specifika ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="e71de-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="e71de-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e71de-108">EXAMPLES</span></span>

### <span data-ttu-id="e71de-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e71de-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="e71de-110">Visa alla `ReservationOrder` som användaren har åtkomst till i den aktuella klient organisationen</span><span class="sxs-lookup"><span data-stu-id="e71de-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="e71de-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e71de-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="e71de-112">Få `ReservationOrder` med angiven ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e71de-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="e71de-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e71de-113">PARAMETERS</span></span>

### <span data-ttu-id="e71de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71de-114">-DefaultProfile</span></span>
<span data-ttu-id="e71de-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e71de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e71de-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e71de-116">-ReservationOrderId</span></span>
<span data-ttu-id="e71de-117">ID för den specifika ReservationOrder som användaren vill se</span><span class="sxs-lookup"><span data-stu-id="e71de-117">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71de-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71de-118">CommonParameters</span></span>
<span data-ttu-id="e71de-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e71de-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71de-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e71de-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71de-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e71de-121">INPUTS</span></span>

### <span data-ttu-id="e71de-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="e71de-122">None</span></span>

## <span data-ttu-id="e71de-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e71de-123">OUTPUTS</span></span>

### <span data-ttu-id="e71de-124">Microsoft. Azure. commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="e71de-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="e71de-125">Microsoft. Azure. commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="e71de-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="e71de-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e71de-126">NOTES</span></span>

## <span data-ttu-id="e71de-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e71de-127">RELATED LINKS</span></span>
