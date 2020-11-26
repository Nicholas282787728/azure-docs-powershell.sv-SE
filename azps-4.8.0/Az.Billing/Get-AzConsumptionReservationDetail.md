---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 2a49cb88fc25643cd26e7ed75d226b8abf6ee50f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260311"
---
# <span data-ttu-id="91d1d-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="91d1d-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="91d1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="91d1d-103">Få information om reservationer för angivet datum intervall.</span><span class="sxs-lookup"><span data-stu-id="91d1d-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="91d1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91d1d-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91d1d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91d1d-105">DESCRIPTION</span></span>
<span data-ttu-id="91d1d-106">Cmdleten **Get-AzConsumptionReservationDetail** hämtar information om reservationer för angivet datum intervall.</span><span class="sxs-lookup"><span data-stu-id="91d1d-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="91d1d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91d1d-107">EXAMPLES</span></span>

### <span data-ttu-id="91d1d-108">Exempel 1: Hämta reservations uppgifter med reservations order-ID för angivet datum intervall</span><span class="sxs-lookup"><span data-stu-id="91d1d-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="91d1d-109">Exempel 2: Hämta reservations uppgifter med reservations order-ID och reservations-ID för det datum intervall som anges</span><span class="sxs-lookup"><span data-stu-id="91d1d-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="91d1d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91d1d-110">PARAMETERS</span></span>

### <span data-ttu-id="91d1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d1d-111">-DefaultProfile</span></span>
<span data-ttu-id="91d1d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91d1d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d1d-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="91d1d-113">-EndDate</span></span>
<span data-ttu-id="91d1d-114">Slutdatumet (ÅÅÅÅ-MM-DD i UTC) av reservations informationen.</span><span class="sxs-lookup"><span data-stu-id="91d1d-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d1d-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="91d1d-115">-ReservationId</span></span>
<span data-ttu-id="91d1d-116">ID för en reservation i en reservations order.</span><span class="sxs-lookup"><span data-stu-id="91d1d-116">The identifier of a reservation within a reservation order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d1d-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="91d1d-117">-ReservationOrderId</span></span>
<span data-ttu-id="91d1d-118">ID för ett reservations köp.</span><span class="sxs-lookup"><span data-stu-id="91d1d-118">The identifier of a reservation purchase.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d1d-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="91d1d-119">-StartDate</span></span>
<span data-ttu-id="91d1d-120">Start data (ÅÅÅÅ-MM-DD i UTC) av reservations informationen.</span><span class="sxs-lookup"><span data-stu-id="91d1d-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d1d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d1d-121">CommonParameters</span></span>
<span data-ttu-id="91d1d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d1d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d1d-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91d1d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d1d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91d1d-124">INPUTS</span></span>

### <span data-ttu-id="91d1d-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="91d1d-125">None</span></span>

## <span data-ttu-id="91d1d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91d1d-126">OUTPUTS</span></span>

### <span data-ttu-id="91d1d-127">Microsoft. Azure. commands. förbrukning. Models. PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="91d1d-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="91d1d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91d1d-128">NOTES</span></span>

## <span data-ttu-id="91d1d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91d1d-129">RELATED LINKS</span></span>