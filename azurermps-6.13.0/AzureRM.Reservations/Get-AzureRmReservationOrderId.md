---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: 1e60ca2ce1a845fa460e14a4e99b921fa4c085ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575126"
---
# <span data-ttu-id="e50db-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e50db-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="e50db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e50db-102">SYNOPSIS</span></span>
<span data-ttu-id="e50db-103">Hämta en lista över tillämpliga `ReservationOrder` ID: n.</span><span class="sxs-lookup"><span data-stu-id="e50db-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e50db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e50db-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e50db-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e50db-105">DESCRIPTION</span></span>
<span data-ttu-id="e50db-106">Skaffa ID: n `ReservationOrder` som kan tillämpas på det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e50db-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="e50db-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e50db-107">EXAMPLES</span></span>

### <span data-ttu-id="e50db-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e50db-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="e50db-109">Använda `ReservationOrder` för standard abonnemang</span><span class="sxs-lookup"><span data-stu-id="e50db-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="e50db-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e50db-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="e50db-111">Använda `ReservationOrder` för angivet abonnemang</span><span class="sxs-lookup"><span data-stu-id="e50db-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="e50db-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e50db-112">PARAMETERS</span></span>

### <span data-ttu-id="e50db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50db-113">-DefaultProfile</span></span>
<span data-ttu-id="e50db-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e50db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e50db-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e50db-115">-SubscriptionId</span></span>
<span data-ttu-id="e50db-116">ID för abonnemanget för att få det använda `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="e50db-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="e50db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50db-117">CommonParameters</span></span>
<span data-ttu-id="e50db-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e50db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50db-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50db-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50db-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e50db-120">INPUTS</span></span>

### <span data-ttu-id="e50db-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="e50db-121">None</span></span>

## <span data-ttu-id="e50db-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e50db-122">OUTPUTS</span></span>

### <span data-ttu-id="e50db-123">Microsoft. Azure. Management. reservations. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="e50db-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="e50db-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e50db-124">NOTES</span></span>

## <span data-ttu-id="e50db-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e50db-125">RELATED LINKS</span></span>
