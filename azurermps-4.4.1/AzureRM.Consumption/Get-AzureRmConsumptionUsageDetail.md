---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: f8347fca355080f11e69bae9793cc0367325ce98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758119"
---
# <span data-ttu-id="4420a-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="4420a-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="4420a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4420a-102">SYNOPSIS</span></span>
<span data-ttu-id="4420a-103">Få användnings information för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4420a-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4420a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4420a-104">SYNTAX</span></span>

### <span data-ttu-id="4420a-105">Abonnemang (standard)</span><span class="sxs-lookup"><span data-stu-id="4420a-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4420a-106">Fakturadeklaration</span><span class="sxs-lookup"><span data-stu-id="4420a-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4420a-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="4420a-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4420a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4420a-108">DESCRIPTION</span></span>
<span data-ttu-id="4420a-109">Cmdleten **Get-AzureRmConsumptionUsageDetail** hämtar användnings information för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4420a-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="4420a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4420a-110">EXAMPLES</span></span>

### <span data-ttu-id="4420a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4420a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="4420a-112">Få användnings information för fakturan med angivet namn och inkludera egenskapen MeterDetails i resultatet.</span><span class="sxs-lookup"><span data-stu-id="4420a-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="4420a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4420a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="4420a-114">Få användnings information om fakturerings perioden med angivet namn och inkludera egenskapen AdditionalProperties i resultatet.</span><span class="sxs-lookup"><span data-stu-id="4420a-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="4420a-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="4420a-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="4420a-116">Få användnings information för abonnemanget som är mellan 2017-01-17 och 2017-01-19.</span><span class="sxs-lookup"><span data-stu-id="4420a-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="4420a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4420a-117">PARAMETERS</span></span>

### <span data-ttu-id="4420a-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="4420a-118">-BillingPeriodName</span></span>
<span data-ttu-id="4420a-119">Namnet på en viss fakturerings period för att få de användnings uppgifter som är kopplade till.</span><span class="sxs-lookup"><span data-stu-id="4420a-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4420a-120">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4420a-120">-EndDate</span></span>
<span data-ttu-id="4420a-121">Slutdatumet (i UTC) för användningarna.</span><span class="sxs-lookup"><span data-stu-id="4420a-121">The end date (in UTC) of the usages.</span></span>

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

### <span data-ttu-id="4420a-122">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="4420a-122">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="4420a-123">Ta med ytterligare egenskaper för användningarna.</span><span class="sxs-lookup"><span data-stu-id="4420a-123">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="4420a-124">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="4420a-124">-IncludeMeterDetails</span></span>
<span data-ttu-id="4420a-125">Ta med mätar detaljer i användningarna.</span><span class="sxs-lookup"><span data-stu-id="4420a-125">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="4420a-126">-InvoiceName</span><span class="sxs-lookup"><span data-stu-id="4420a-126">-InvoiceName</span></span>
<span data-ttu-id="4420a-127">Namnet på en specifik faktura för att få användnings informationen som är associerad med.</span><span class="sxs-lookup"><span data-stu-id="4420a-127">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4420a-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4420a-128">-MaxCount</span></span>
<span data-ttu-id="4420a-129">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="4420a-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="4420a-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4420a-130">-StartDate</span></span>
<span data-ttu-id="4420a-131">Start datumet (i UTC) för användningarna.</span><span class="sxs-lookup"><span data-stu-id="4420a-131">The start date (in UTC) of the usages.</span></span>

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

### <span data-ttu-id="4420a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4420a-132">-DefaultProfile</span></span>
<span data-ttu-id="4420a-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4420a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4420a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4420a-134">CommonParameters</span></span>
<span data-ttu-id="4420a-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4420a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4420a-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4420a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4420a-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4420a-137">INPUTS</span></span>

### <span data-ttu-id="4420a-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="4420a-138">None</span></span>

## <span data-ttu-id="4420a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4420a-139">OUTPUTS</span></span>

### <span data-ttu-id="4420a-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. förbrukning. Models. PSUsageDetail, Microsoft. Azure. commands. förbrukning, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4420a-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4420a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4420a-141">NOTES</span></span>

## <span data-ttu-id="4420a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4420a-142">RELATED LINKS</span></span>

