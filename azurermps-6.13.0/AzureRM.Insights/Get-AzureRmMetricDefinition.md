---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: 8dea2e61d6d64fbb59363d157dc0b8c1096ba259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755952"
---
# <span data-ttu-id="5cfbf-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="5cfbf-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="5cfbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cfbf-102">SYNOPSIS</span></span>
<span data-ttu-id="5cfbf-103">Hämtar mått definitioner.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cfbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cfbf-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cfbf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cfbf-105">DESCRIPTION</span></span>
<span data-ttu-id="5cfbf-106">Cmdleten **Get-AzureRmMetricDefinition** hämtar mått definitioner.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="5cfbf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cfbf-107">EXAMPLES</span></span>

### <span data-ttu-id="5cfbf-108">Exempel 1: Hämta mått definitioner för en resurs</span><span class="sxs-lookup"><span data-stu-id="5cfbf-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="5cfbf-109">Det här kommandot får Mät definitioner för den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="5cfbf-110">Exempel 2: Hämta mått definitioner med detaljerad utskrift</span><span class="sxs-lookup"><span data-stu-id="5cfbf-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="5cfbf-111">Det här kommandot hämtar mått definitioner för webbplats2.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="5cfbf-112">Resultatet är detaljerat.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-112">The output is detailed.</span></span>

### <span data-ttu-id="5cfbf-113">Exempel 3: Hämta mått definitioner efter namn</span><span class="sxs-lookup"><span data-stu-id="5cfbf-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="5cfbf-114">Det här kommandot får definitioner för måtten BytesSent och CpuTime.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="5cfbf-115">Resultatet är detaljerat.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-115">The output is detailed.</span></span>

## <span data-ttu-id="5cfbf-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cfbf-116">PARAMETERS</span></span>

### <span data-ttu-id="5cfbf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cfbf-117">-DefaultProfile</span></span>
<span data-ttu-id="5cfbf-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5cfbf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cfbf-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="5cfbf-119">-DetailedOutput</span></span>
<span data-ttu-id="5cfbf-120">Anger att den här åtgärden innehöll detaljerade utdata.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="5cfbf-121">Om du inte anger den här parametern sammanfattas utdata.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="5cfbf-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="5cfbf-122">-MetricName</span></span>
<span data-ttu-id="5cfbf-123">Anger en matris med namn på mått.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfbf-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="5cfbf-124">-MetricNamespace</span></span>
<span data-ttu-id="5cfbf-125">Anger mått namn området för att fråga efter mått definitioner för.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfbf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cfbf-126">-ResourceId</span></span>
<span data-ttu-id="5cfbf-127">Anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-127">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfbf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cfbf-128">CommonParameters</span></span>
<span data-ttu-id="5cfbf-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cfbf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cfbf-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cfbf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cfbf-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cfbf-131">INPUTS</span></span>

### <span data-ttu-id="5cfbf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5cfbf-132">System.String</span></span>

### <span data-ttu-id="5cfbf-133">System. string []</span><span class="sxs-lookup"><span data-stu-id="5cfbf-133">System.String[]</span></span>

## <span data-ttu-id="5cfbf-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cfbf-134">OUTPUTS</span></span>

### <span data-ttu-id="5cfbf-135">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="5cfbf-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="5cfbf-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cfbf-136">NOTES</span></span>

## <span data-ttu-id="5cfbf-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cfbf-137">RELATED LINKS</span></span>

<span data-ttu-id="5cfbf-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="5cfbf-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>

