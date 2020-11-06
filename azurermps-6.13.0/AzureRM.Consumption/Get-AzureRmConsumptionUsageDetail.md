---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 92e132d6ef35d4a085abc2d1bc80ec4ab433036a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582755"
---
# <span data-ttu-id="55315-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="55315-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="55315-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55315-102">SYNOPSIS</span></span>
<span data-ttu-id="55315-103">Få användnings information för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="55315-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55315-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55315-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-InvoiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55315-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55315-105">DESCRIPTION</span></span>
<span data-ttu-id="55315-106">Cmdleten **Get-AzureRmConsumptionUsageDetail** hämtar användnings information för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="55315-106">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="55315-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55315-107">EXAMPLES</span></span>

### <span data-ttu-id="55315-108">Exempel 1: Hämta information om användning med MeterDetails</span><span class="sxs-lookup"><span data-stu-id="55315-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionUsageDetail -Expand MeterDetails -Top 10
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

### <span data-ttu-id="55315-109">Exempel 2: Hämta information om användning med datum intervall</span><span class="sxs-lookup"><span data-stu-id="55315-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
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

### <span data-ttu-id="55315-110">Exempel 3: Hämta information om användning av BillingPeriodName med filtret InstanceName</span><span class="sxs-lookup"><span data-stu-id="55315-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
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

## <span data-ttu-id="55315-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55315-111">PARAMETERS</span></span>

### <span data-ttu-id="55315-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="55315-112">-BillingPeriodName</span></span>
<span data-ttu-id="55315-113">Namnet på en viss fakturerings period för att få de användnings uppgifter som är kopplade till.</span><span class="sxs-lookup"><span data-stu-id="55315-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="55315-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55315-114">-DefaultProfile</span></span>
<span data-ttu-id="55315-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55315-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55315-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="55315-116">-EndDate</span></span>
<span data-ttu-id="55315-117">Slutdatumet (i UTC) för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="55315-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="55315-118">-Expandera</span><span class="sxs-lookup"><span data-stu-id="55315-118">-Expand</span></span>
<span data-ttu-id="55315-119">Utöka användningarna baserat på MeterDetails eller AdditionalInfo.</span><span class="sxs-lookup"><span data-stu-id="55315-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="55315-120">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="55315-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="55315-121">Ta med ytterligare egenskaper för användningarna.</span><span class="sxs-lookup"><span data-stu-id="55315-121">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="55315-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="55315-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="55315-123">Ta med mätar detaljer i användningarna.</span><span class="sxs-lookup"><span data-stu-id="55315-123">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="55315-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="55315-124">-InstanceId</span></span>
<span data-ttu-id="55315-125">Instans-ID för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="55315-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="55315-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="55315-126">-InstanceName</span></span>
<span data-ttu-id="55315-127">Instans namnet på den användning som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="55315-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="55315-128">-InvoiceName</span><span class="sxs-lookup"><span data-stu-id="55315-128">-InvoiceName</span></span>
<span data-ttu-id="55315-129">Namnet på en specifik faktura för att få användnings informationen som är associerad med.</span><span class="sxs-lookup"><span data-stu-id="55315-129">Name of a specific invoice to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="55315-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="55315-130">-MaxCount</span></span>
<span data-ttu-id="55315-131">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="55315-131">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="55315-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="55315-132">-ResourceGroup</span></span>
<span data-ttu-id="55315-133">Resurs gruppen för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="55315-133">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="55315-134">-StartDate</span><span class="sxs-lookup"><span data-stu-id="55315-134">-StartDate</span></span>
<span data-ttu-id="55315-135">Start datumet (i UTC) för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="55315-135">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="55315-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="55315-136">-Tag</span></span>
<span data-ttu-id="55315-137">Taggen för de användningar som ska filtreras.</span><span class="sxs-lookup"><span data-stu-id="55315-137">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="55315-138">-Överst</span><span class="sxs-lookup"><span data-stu-id="55315-138">-Top</span></span>
<span data-ttu-id="55315-139">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="55315-139">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="55315-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55315-140">CommonParameters</span></span>
<span data-ttu-id="55315-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55315-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55315-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55315-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55315-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55315-143">INPUTS</span></span>

### <span data-ttu-id="55315-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="55315-144">None</span></span>

## <span data-ttu-id="55315-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55315-145">OUTPUTS</span></span>

### <span data-ttu-id="55315-146">Microsoft. Azure. commands. förbrukning. Models. PSUsageDetail</span><span class="sxs-lookup"><span data-stu-id="55315-146">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="55315-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55315-147">NOTES</span></span>

## <span data-ttu-id="55315-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55315-148">RELATED LINKS</span></span>
