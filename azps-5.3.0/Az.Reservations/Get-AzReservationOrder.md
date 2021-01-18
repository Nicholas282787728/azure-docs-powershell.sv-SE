---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523062"
---
# <span data-ttu-id="a4aad-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="a4aad-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="a4aad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4aad-102">SYNOPSIS</span></span>
<span data-ttu-id="a4aad-103">Lära `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="a4aad-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="a4aad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4aad-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4aad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4aad-105">DESCRIPTION</span></span>
<span data-ttu-id="a4aad-106">Lista över alla `ReservationOrder` s som användaren har till gång till i den aktuella klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="a4aad-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="a4aad-107">Om ReservationOrderId parameter är aktive rad ska du hämta specifika ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="a4aad-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="a4aad-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4aad-108">EXAMPLES</span></span>

### <span data-ttu-id="a4aad-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4aad-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="a4aad-110">Visa alla `ReservationOrder` som användaren har åtkomst till i den aktuella klient organisationen</span><span class="sxs-lookup"><span data-stu-id="a4aad-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="a4aad-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a4aad-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="a4aad-112">Få `ReservationOrder` med angiven ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a4aad-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="a4aad-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4aad-113">PARAMETERS</span></span>

### <span data-ttu-id="a4aad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4aad-114">-DefaultProfile</span></span>
<span data-ttu-id="a4aad-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4aad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4aad-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a4aad-116">-ReservationOrderId</span></span>
<span data-ttu-id="a4aad-117">ID för den specifika ReservationOrder som användaren vill se</span><span class="sxs-lookup"><span data-stu-id="a4aad-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="a4aad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4aad-118">CommonParameters</span></span>
<span data-ttu-id="a4aad-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4aad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4aad-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4aad-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4aad-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4aad-121">INPUTS</span></span>

### <span data-ttu-id="a4aad-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="a4aad-122">None</span></span>

## <span data-ttu-id="a4aad-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4aad-123">OUTPUTS</span></span>

### <span data-ttu-id="a4aad-124">Microsoft. Azure. commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="a4aad-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="a4aad-125">Microsoft. Azure. commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="a4aad-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="a4aad-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4aad-126">NOTES</span></span>

## <span data-ttu-id="a4aad-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4aad-127">RELATED LINKS</span></span>
