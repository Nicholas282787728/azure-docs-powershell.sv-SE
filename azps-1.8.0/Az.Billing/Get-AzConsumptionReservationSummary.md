---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a224157fb8a0740b49cd2b3576e57da9b45c993b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754676"
---
# <span data-ttu-id="b6332-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="b6332-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="b6332-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6332-102">SYNOPSIS</span></span>
<span data-ttu-id="b6332-103">Få reservations översikter för daglig eller månatlig kornig het.</span><span class="sxs-lookup"><span data-stu-id="b6332-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="b6332-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6332-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6332-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6332-105">DESCRIPTION</span></span>
<span data-ttu-id="b6332-106">Cmdleten **Get-AzConsumptionReservationSummay** hämtar reservations sammanfattningarna för varje dag eller månads kornig het.</span><span class="sxs-lookup"><span data-stu-id="b6332-106">The **Get-AzConsumptionReservationSummay** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="b6332-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6332-107">EXAMPLES</span></span>

### <span data-ttu-id="b6332-108">Exempel 1: få reservations översikter med reservations order-ID för månatlig kornig het</span><span class="sxs-lookup"><span data-stu-id="b6332-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="b6332-109">Exempel 2: få reservations översikter med reservations order-ID och reservations-ID för månatlig kornig het</span><span class="sxs-lookup"><span data-stu-id="b6332-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="b6332-110">Exempel 3: Hämta reservations översikter med reservations order-ID för daglig kornigt datum intervall</span><span class="sxs-lookup"><span data-stu-id="b6332-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="b6332-111">Exempel 4: Hämta reservations översikter med reservations order-ID och reservations-ID för daglig kornigt angivet datum intervall</span><span class="sxs-lookup"><span data-stu-id="b6332-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="b6332-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6332-112">PARAMETERS</span></span>

### <span data-ttu-id="b6332-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6332-113">-DefaultProfile</span></span>
<span data-ttu-id="b6332-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6332-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6332-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b6332-115">-EndDate</span></span>
<span data-ttu-id="b6332-116">Slutdatumet (ÅÅÅÅ-MM-DD i UTC) av reservations sammanfattningen, obligatoriskt för daglig kornig het.</span><span class="sxs-lookup"><span data-stu-id="b6332-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6332-117">Kornig het</span><span class="sxs-lookup"><span data-stu-id="b6332-117">-Grain</span></span>
<span data-ttu-id="b6332-118">Tids kornigheten för reservations sammanfattningen kan vara per dag eller månad.</span><span class="sxs-lookup"><span data-stu-id="b6332-118">The time grain of the reservation summaryy, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6332-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="b6332-119">-ReservationId</span></span>
<span data-ttu-id="b6332-120">ID för en reservation i en reservations order.</span><span class="sxs-lookup"><span data-stu-id="b6332-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="b6332-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="b6332-121">-ReservationOrderId</span></span>
<span data-ttu-id="b6332-122">ID för ett reservations köp.</span><span class="sxs-lookup"><span data-stu-id="b6332-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="b6332-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b6332-123">-StartDate</span></span>
<span data-ttu-id="b6332-124">Start data (ÅÅÅÅ-MM-DD i UTC) av reservations sammanfattningen, obligatoriskt för daglig kornig het.</span><span class="sxs-lookup"><span data-stu-id="b6332-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6332-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6332-125">CommonParameters</span></span>
<span data-ttu-id="b6332-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6332-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6332-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6332-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6332-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6332-128">INPUTS</span></span>

### <span data-ttu-id="b6332-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="b6332-129">None</span></span>

## <span data-ttu-id="b6332-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6332-130">OUTPUTS</span></span>

### <span data-ttu-id="b6332-131">Microsoft. Azure. commands. förbrukning. Models. PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="b6332-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="b6332-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6332-132">NOTES</span></span>

## <span data-ttu-id="b6332-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6332-133">RELATED LINKS</span></span>