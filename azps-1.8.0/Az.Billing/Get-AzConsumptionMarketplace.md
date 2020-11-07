---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: 4533ed3c522cbd1633184b86de68288a3c8dd1ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917609"
---
# <span data-ttu-id="839e3-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="839e3-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="839e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="839e3-102">SYNOPSIS</span></span>
<span data-ttu-id="839e3-103">Skaffa marknads plats för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="839e3-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="839e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="839e3-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="839e3-105">DESCRIPTION</span></span>
<span data-ttu-id="839e3-106">Cmdleten **Get-AzConsumptionMarketplace** får plats för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="839e3-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="839e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="839e3-107">EXAMPLES</span></span>

### <span data-ttu-id="839e3-108">Exempel 1: få användning av Marketplace</span><span class="sxs-lookup"><span data-stu-id="839e3-108">Example 1: Get marketplaces usage</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

### <span data-ttu-id="839e3-109">Exempel 2: skaffa användning av Marketplace med datum intervall</span><span class="sxs-lookup"><span data-stu-id="839e3-109">Example 2: Get marketplace usage with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -StartDate 2018-01-03 -EndDate 2018-01-20 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1/providers/Microsoft.Consumption/marketplaces/0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-01-04T00:00:00Z
UsageStart:  2018-01-03T00:00:00Z
```

### <span data-ttu-id="839e3-110">Exempel 3: skaffa Marketplace-användning för BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="839e3-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -BillingPeriodName 201801-1 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1/providers/Microsoft.Consumption/marketplaces/ea82233a-9f76-7eaa-4478-42bd61cf6287
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  ea82233a-9f76-7eaa-4478-42bd61cf6287
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2017-10-29T00:00:00Z
UsageStart:  2017-10-28T00:00:00Z
```

### <span data-ttu-id="839e3-111">Exempel 4: Hämta användning av Marketplace med filtret instans namn</span><span class="sxs-lookup"><span data-stu-id="839e3-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -InstanceName TestVM -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

## <span data-ttu-id="839e3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="839e3-112">PARAMETERS</span></span>

### <span data-ttu-id="839e3-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="839e3-113">-BillingPeriodName</span></span>
<span data-ttu-id="839e3-114">Namnet på en viss fakturerings period för att få den Marketplace som är associerad med.</span><span class="sxs-lookup"><span data-stu-id="839e3-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="839e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839e3-115">-DefaultProfile</span></span>
<span data-ttu-id="839e3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="839e3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="839e3-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="839e3-117">-EndDate</span></span>
<span data-ttu-id="839e3-118">Slutdatumet (i UTC) för att filtrera.</span><span class="sxs-lookup"><span data-stu-id="839e3-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="839e3-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="839e3-119">-InstanceId</span></span>
<span data-ttu-id="839e3-120">Instans-ID för de Marketplace som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="839e3-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="839e3-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="839e3-121">-InstanceName</span></span>
<span data-ttu-id="839e3-122">Instans namnet på den marknads plats som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="839e3-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="839e3-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="839e3-123">-ResourceGroup</span></span>
<span data-ttu-id="839e3-124">Resurs gruppen för marknads platser som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="839e3-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="839e3-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="839e3-125">-StartDate</span></span>
<span data-ttu-id="839e3-126">Start datumet (i UTC) för de marknads platser som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="839e3-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="839e3-127">-Överst</span><span class="sxs-lookup"><span data-stu-id="839e3-127">-Top</span></span>
<span data-ttu-id="839e3-128">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="839e3-128">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839e3-129">CommonParameters</span></span>
<span data-ttu-id="839e3-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="839e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839e3-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="839e3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839e3-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="839e3-132">INPUTS</span></span>

### <span data-ttu-id="839e3-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="839e3-133">None</span></span>

## <span data-ttu-id="839e3-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="839e3-134">OUTPUTS</span></span>

### <span data-ttu-id="839e3-135">Microsoft. Azure. commands. förbrukning. Models. PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="839e3-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="839e3-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="839e3-136">NOTES</span></span>

## <span data-ttu-id="839e3-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="839e3-137">RELATED LINKS</span></span>
