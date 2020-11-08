---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
ms.openlocfilehash: 8eeee753fda32f40dfabf156b352724b0bd87b92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090132"
---
# <span data-ttu-id="9b851-101">Get-AzConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="9b851-101">Get-AzConsumptionUsageDetail</span></span>

## <span data-ttu-id="9b851-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b851-102">SYNOPSIS</span></span>
<span data-ttu-id="9b851-103">Få användnings information för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9b851-103">Get usage details of the subscription.</span></span>

## <span data-ttu-id="9b851-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b851-104">SYNTAX</span></span>

```
Get-AzConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b851-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b851-105">DESCRIPTION</span></span>
<span data-ttu-id="9b851-106">Cmdleten **Get-AzConsumptionUsageDetail** hämtar användnings information för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9b851-106">The **Get-AzConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="9b851-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b851-107">EXAMPLES</span></span>

### <span data-ttu-id="9b851-108">Exempel 1: Hämta information om användning med MeterDetails</span><span class="sxs-lookup"><span data-stu-id="9b851-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -Expand MeterDetails -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
ConsumedService:  Microsoft.Compute
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/usageDetails/24b9dff0-f022-55a1-886b-17b330000db3
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/MAR-CCM/providers/Microsoft.Compute/disks/mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
InstanceLocation:  usnorthcentral
InstanceName:  mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
IsEstimated:  true
MeterDetails:  MeterCategory:  Data Management
               MeterLocation:  usnorthcentral
               MeterName:  Standard Managed Disk Operations (in 10,000s)
               MeterSubCategory:  Data Management
               Unit:  Operations
MeterId:  82cd70ab-1aee-4b30-bc04-8b71e1204dbc
Name:  24b9dff0-f022-55a1-886b-17b330000db3
PretaxCost:  0
Product:  Data Management Standard Managed Disk Operations
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  6/1/2018 11:59:59 PM
UsageQuantity:  3.8218
UsageStart:  6/1/2018 12:00:00 AM
```

### <span data-ttu-id="9b851-109">Exempel 2: Hämta information om användning med datum intervall</span><span class="sxs-lookup"><span data-stu-id="9b851-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/732582e5-40ad-bb23-7a69-ca1ff7c8b004
InstanceId:  storsimplezc9q6r2t7f
InstanceLocation:  US West Central
InstanceName:  storsimplezc9q6r2t7f
IsEstimated:  false
MeterId:  ad22fac8-9da5-4577-8683-56ae94d39e42
Name:  732582e5-40ad-bb23-7a69-ca1ff7c8b004
PretaxCost:  0
Product:  Data Management Geo Redundant Standard IO - Table Write
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/2/2017 11:59:59 PM
UsageQuantity:  0.0006
UsageStart:  10/2/2017 12:00:00 AM
```

### <span data-ttu-id="9b851-110">Exempel 3: Hämta information om användning av BillingPeriodName med filtret InstanceName</span><span class="sxs-lookup"><span data-stu-id="9b851-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Microsoft.Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/8abc8b65-e8f1-31e1-f02b-058a7572363f
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/securitydata/providers/Microsoft.Storage/storageAccounts/1c2052westus
InstanceLocation:  uswest
InstanceName:  1c2052westus
IsEstimated:  false
MeterId:  9995d93a-7d35-4d3f-9c69-7a7fea447ef4
Name:  8abc8b65-e8f1-31e1-f02b-058a7572363f
PretaxCost:  0.000000693016692
Product:  Data Transfer Out - Zone 1
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/1/2017 11:59:59 PM
UsageQuantity:  0.000009
UsageStart:  10/1/2017 12:00:00 AM
```

## <span data-ttu-id="9b851-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b851-111">PARAMETERS</span></span>

### <span data-ttu-id="9b851-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="9b851-112">-BillingPeriodName</span></span>
<span data-ttu-id="9b851-113">Namnet på en viss fakturerings period för att få de användnings uppgifter som är kopplade till.</span><span class="sxs-lookup"><span data-stu-id="9b851-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="9b851-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b851-114">-DefaultProfile</span></span>
<span data-ttu-id="9b851-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b851-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b851-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9b851-116">-EndDate</span></span>
<span data-ttu-id="9b851-117">Slutdatumet (i UTC) för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="9b851-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="9b851-118">-Expandera</span><span class="sxs-lookup"><span data-stu-id="9b851-118">-Expand</span></span>
<span data-ttu-id="9b851-119">Utöka användningarna baserat på MeterDetails eller AdditionalInfo.</span><span class="sxs-lookup"><span data-stu-id="9b851-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="9b851-120">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="9b851-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="9b851-121">Ta med ytterligare egenskaper för användningarna.</span><span class="sxs-lookup"><span data-stu-id="9b851-121">Include additional properties in the usages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b851-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="9b851-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="9b851-123">Ta med mätar detaljer i användningarna.</span><span class="sxs-lookup"><span data-stu-id="9b851-123">Include meter details in the usages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b851-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9b851-124">-InstanceId</span></span>
<span data-ttu-id="9b851-125">Instans-ID för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="9b851-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="9b851-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9b851-126">-InstanceName</span></span>
<span data-ttu-id="9b851-127">Instans namnet på den användning som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="9b851-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="9b851-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9b851-128">-MaxCount</span></span>
<span data-ttu-id="9b851-129">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="9b851-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="9b851-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b851-130">-ResourceGroup</span></span>
<span data-ttu-id="9b851-131">Resurs gruppen för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="9b851-131">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="9b851-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9b851-132">-StartDate</span></span>
<span data-ttu-id="9b851-133">Start datumet (i UTC) för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="9b851-133">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="9b851-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9b851-134">-Tag</span></span>
<span data-ttu-id="9b851-135">Taggen för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="9b851-135">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="9b851-136">-Överst</span><span class="sxs-lookup"><span data-stu-id="9b851-136">-Top</span></span>
<span data-ttu-id="9b851-137">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="9b851-137">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="9b851-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b851-138">CommonParameters</span></span>
<span data-ttu-id="9b851-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b851-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b851-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b851-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b851-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b851-141">INPUTS</span></span>

### <span data-ttu-id="9b851-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="9b851-142">None</span></span>

## <span data-ttu-id="9b851-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b851-143">OUTPUTS</span></span>

### <span data-ttu-id="9b851-144">Microsoft. Azure. commands. förbrukning. Models. PSUsageDetail</span><span class="sxs-lookup"><span data-stu-id="9b851-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="9b851-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b851-145">NOTES</span></span>

## <span data-ttu-id="9b851-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b851-146">RELATED LINKS</span></span>