---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 12e76c3412f54ba840528f9ff1a40acd388cd109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575128"
---
# <span data-ttu-id="bec38-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="bec38-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="bec38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bec38-102">SYNOPSIS</span></span>
<span data-ttu-id="bec38-103">Lära `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="bec38-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bec38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bec38-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bec38-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bec38-105">DESCRIPTION</span></span>
<span data-ttu-id="bec38-106">Lista över alla `ReservationOrder` s som användaren har till gång till i den aktuella klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="bec38-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="bec38-107">Om ReservationOrderId parameter är aktive rad ska du hämta specifika ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="bec38-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="bec38-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bec38-108">EXAMPLES</span></span>

### <span data-ttu-id="bec38-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bec38-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="bec38-110">Visa alla `ReservationOrder` som användaren har åtkomst till i den aktuella klient organisationen</span><span class="sxs-lookup"><span data-stu-id="bec38-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="bec38-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bec38-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="bec38-112">Få `ReservationOrder` med angiven ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="bec38-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="bec38-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bec38-113">PARAMETERS</span></span>

### <span data-ttu-id="bec38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec38-114">-DefaultProfile</span></span>
<span data-ttu-id="bec38-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bec38-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec38-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="bec38-116">-ReservationOrderId</span></span>
<span data-ttu-id="bec38-117">ID för den specifika ReservationOrder som användaren vill se</span><span class="sxs-lookup"><span data-stu-id="bec38-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="bec38-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec38-118">CommonParameters</span></span>
<span data-ttu-id="bec38-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec38-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec38-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec38-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec38-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bec38-121">INPUTS</span></span>

### <span data-ttu-id="bec38-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="bec38-122">None</span></span>

## <span data-ttu-id="bec38-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bec38-123">OUTPUTS</span></span>

### <span data-ttu-id="bec38-124">Microsoft. Azure. commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="bec38-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="bec38-125">Microsoft. Azure. commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="bec38-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="bec38-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bec38-126">NOTES</span></span>

## <span data-ttu-id="bec38-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bec38-127">RELATED LINKS</span></span>
