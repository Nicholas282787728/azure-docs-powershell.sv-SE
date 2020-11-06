---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: de839f4b56f4aa1111e130bdf6396875f9aeb185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577220"
---
# <span data-ttu-id="7bce3-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="7bce3-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="7bce3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bce3-102">SYNOPSIS</span></span>
<span data-ttu-id="7bce3-103">Hämtar mått definitioner.</span><span class="sxs-lookup"><span data-stu-id="7bce3-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bce3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bce3-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bce3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bce3-105">DESCRIPTION</span></span>
<span data-ttu-id="7bce3-106">Cmdleten **Get-AzureRmMetricDefinition** hämtar mått definitioner.</span><span class="sxs-lookup"><span data-stu-id="7bce3-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="7bce3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bce3-107">EXAMPLES</span></span>

### <span data-ttu-id="7bce3-108">Exempel 1: Hämta mått definitioner för en resurs</span><span class="sxs-lookup"><span data-stu-id="7bce3-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="7bce3-109">Det här kommandot får Mät definitioner för den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="7bce3-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="7bce3-110">Exempel 2: Hämta mått definitioner med detaljerad utskrift</span><span class="sxs-lookup"><span data-stu-id="7bce3-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="7bce3-111">Det här kommandot hämtar mått definitioner för webbplats2.</span><span class="sxs-lookup"><span data-stu-id="7bce3-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="7bce3-112">Resultatet är detaljerat.</span><span class="sxs-lookup"><span data-stu-id="7bce3-112">The output is detailed.</span></span>

### <span data-ttu-id="7bce3-113">Exempel 3: Hämta mått definitioner efter namn</span><span class="sxs-lookup"><span data-stu-id="7bce3-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="7bce3-114">Det här kommandot får definitioner för måtten BytesSent och CpuTime.</span><span class="sxs-lookup"><span data-stu-id="7bce3-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="7bce3-115">Resultatet är detaljerat.</span><span class="sxs-lookup"><span data-stu-id="7bce3-115">The output is detailed.</span></span>

## <span data-ttu-id="7bce3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bce3-116">PARAMETERS</span></span>

### <span data-ttu-id="7bce3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bce3-117">-DefaultProfile</span></span>
<span data-ttu-id="7bce3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7bce3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bce3-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="7bce3-119">-DetailedOutput</span></span>
<span data-ttu-id="7bce3-120">Anger att den här åtgärden innehöll detaljerade utdata.</span><span class="sxs-lookup"><span data-stu-id="7bce3-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="7bce3-121">Om du inte anger den här parametern sammanfattas utdata.</span><span class="sxs-lookup"><span data-stu-id="7bce3-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bce3-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="7bce3-122">-MetricName</span></span>
<span data-ttu-id="7bce3-123">Anger en matris med namn på mått.</span><span class="sxs-lookup"><span data-stu-id="7bce3-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bce3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bce3-124">-ResourceId</span></span>
<span data-ttu-id="7bce3-125">Anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7bce3-125">Specifies the resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bce3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bce3-126">CommonParameters</span></span>
<span data-ttu-id="7bce3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bce3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bce3-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bce3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bce3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bce3-129">INPUTS</span></span>

### <span data-ttu-id="7bce3-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="7bce3-130">None</span></span>
<span data-ttu-id="7bce3-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7bce3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7bce3-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bce3-132">OUTPUTS</span></span>

### <span data-ttu-id="7bce3-133">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricDefinition []</span><span class="sxs-lookup"><span data-stu-id="7bce3-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="7bce3-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bce3-134">NOTES</span></span>

## <span data-ttu-id="7bce3-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bce3-135">RELATED LINKS</span></span>

[<span data-ttu-id="7bce3-136">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="7bce3-136">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


