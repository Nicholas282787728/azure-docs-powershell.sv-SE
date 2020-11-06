---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 2694ce516b1bb3202fc194e1c1eec55610f7b92a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573492"
---
# <span data-ttu-id="c8446-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="c8446-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="c8446-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8446-102">SYNOPSIS</span></span>
<span data-ttu-id="c8446-103">Få användnings information för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c8446-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8446-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8446-104">SYNTAX</span></span>

### <span data-ttu-id="c8446-105">Abonnemang (standard)</span><span class="sxs-lookup"><span data-stu-id="c8446-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8446-106">Fakturadeklaration</span><span class="sxs-lookup"><span data-stu-id="c8446-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8446-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="c8446-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8446-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8446-108">DESCRIPTION</span></span>
<span data-ttu-id="c8446-109">Cmdleten **Get-AzureRmConsumptionUsageDetail** hämtar användnings information för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c8446-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="c8446-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8446-110">EXAMPLES</span></span>

### <span data-ttu-id="c8446-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c8446-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="c8446-112">Få användnings information för fakturan med angivet namn och inkludera egenskapen MeterDetails i resultatet.</span><span class="sxs-lookup"><span data-stu-id="c8446-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="c8446-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c8446-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="c8446-114">Få användnings information om fakturerings perioden med angivet namn och inkludera egenskapen AdditionalProperties i resultatet.</span><span class="sxs-lookup"><span data-stu-id="c8446-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="c8446-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c8446-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="c8446-116">Få användnings information för abonnemanget som är mellan 2017-01-17 och 2017-01-19.</span><span class="sxs-lookup"><span data-stu-id="c8446-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="c8446-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8446-117">PARAMETERS</span></span>

### <span data-ttu-id="c8446-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="c8446-118">-BillingPeriodName</span></span>
<span data-ttu-id="c8446-119">Namnet på en viss fakturerings period för att få de användnings uppgifter som är kopplade till.</span><span class="sxs-lookup"><span data-stu-id="c8446-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8446-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8446-120">-DefaultProfile</span></span>
<span data-ttu-id="c8446-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c8446-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8446-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c8446-122">-EndDate</span></span>
<span data-ttu-id="c8446-123">Slutdatumet (i UTC) för användningarna.</span><span class="sxs-lookup"><span data-stu-id="c8446-123">The end date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8446-124">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="c8446-124">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="c8446-125">Ta med ytterligare egenskaper för användningarna.</span><span class="sxs-lookup"><span data-stu-id="c8446-125">Include additional properties in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8446-126">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="c8446-126">-IncludeMeterDetails</span></span>
<span data-ttu-id="c8446-127">Ta med mätar detaljer i användningarna.</span><span class="sxs-lookup"><span data-stu-id="c8446-127">Include meter details in the usages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8446-128">-InvoiceName</span><span class="sxs-lookup"><span data-stu-id="c8446-128">-InvoiceName</span></span>
<span data-ttu-id="c8446-129">Namnet på en specifik faktura för att få användnings informationen som är associerad med.</span><span class="sxs-lookup"><span data-stu-id="c8446-129">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8446-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c8446-130">-MaxCount</span></span>
<span data-ttu-id="c8446-131">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="c8446-131">Determine the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8446-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c8446-132">-StartDate</span></span>
<span data-ttu-id="c8446-133">Start datumet (i UTC) för användningarna.</span><span class="sxs-lookup"><span data-stu-id="c8446-133">The start date (in UTC) of the usages.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8446-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8446-134">CommonParameters</span></span>
<span data-ttu-id="c8446-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8446-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8446-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8446-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8446-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8446-137">INPUTS</span></span>

### <span data-ttu-id="c8446-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="c8446-138">None</span></span>

## <span data-ttu-id="c8446-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8446-139">OUTPUTS</span></span>

### <span data-ttu-id="c8446-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. förbrukning. Models. PSUsageDetail, Microsoft. Azure. commands. förbrukning, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c8446-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c8446-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8446-141">NOTES</span></span>

## <span data-ttu-id="c8446-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8446-142">RELATED LINKS</span></span>

