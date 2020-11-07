---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: c969d24a894165e23628b91cda640f676ec3f3d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920118"
---
# <span data-ttu-id="9db6d-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9db6d-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="9db6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9db6d-102">SYNOPSIS</span></span>
<span data-ttu-id="9db6d-103">Hämta en lista över tillämpliga `ReservationOrder` ID: n.</span><span class="sxs-lookup"><span data-stu-id="9db6d-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="9db6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9db6d-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9db6d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9db6d-105">DESCRIPTION</span></span>
<span data-ttu-id="9db6d-106">Skaffa ID: n `ReservationOrder` som kan tillämpas på det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9db6d-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="9db6d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9db6d-107">EXAMPLES</span></span>

### <span data-ttu-id="9db6d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9db6d-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="9db6d-109">Använda `ReservationOrder` för standard abonnemang</span><span class="sxs-lookup"><span data-stu-id="9db6d-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="9db6d-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9db6d-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="9db6d-111">Använda `ReservationOrder` för angivet abonnemang</span><span class="sxs-lookup"><span data-stu-id="9db6d-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="9db6d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9db6d-112">PARAMETERS</span></span>

### <span data-ttu-id="9db6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db6d-113">-DefaultProfile</span></span>
<span data-ttu-id="9db6d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9db6d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9db6d-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9db6d-115">-SubscriptionId</span></span>
<span data-ttu-id="9db6d-116">ID för abonnemanget för att få det använda `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="9db6d-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="9db6d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db6d-117">CommonParameters</span></span>
<span data-ttu-id="9db6d-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db6d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db6d-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db6d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db6d-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9db6d-120">INPUTS</span></span>

### <span data-ttu-id="9db6d-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="9db6d-121">None</span></span>

## <span data-ttu-id="9db6d-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9db6d-122">OUTPUTS</span></span>

### <span data-ttu-id="9db6d-123">Microsoft. Azure. Management. reservations. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="9db6d-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="9db6d-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9db6d-124">NOTES</span></span>

## <span data-ttu-id="9db6d-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9db6d-125">RELATED LINKS</span></span>
