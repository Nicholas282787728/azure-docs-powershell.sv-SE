---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 5eab973f7a5c5f6221d4c02d94702a4d4a549204
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922598"
---
# <span data-ttu-id="0900c-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="0900c-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="0900c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0900c-102">SYNOPSIS</span></span>
<span data-ttu-id="0900c-103">Hämtar mått definitioner.</span><span class="sxs-lookup"><span data-stu-id="0900c-103">Gets metric definitions.</span></span>

## <span data-ttu-id="0900c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0900c-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0900c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0900c-105">DESCRIPTION</span></span>
<span data-ttu-id="0900c-106">Cmdleten **Get-AzMetricDefinition** hämtar mått definitioner.</span><span class="sxs-lookup"><span data-stu-id="0900c-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="0900c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0900c-107">EXAMPLES</span></span>

### <span data-ttu-id="0900c-108">Exempel 1: Hämta mått definitioner för en resurs</span><span class="sxs-lookup"><span data-stu-id="0900c-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
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

<span data-ttu-id="0900c-109">Det här kommandot får Mät definitioner för den angivna resursen.</span><span class="sxs-lookup"><span data-stu-id="0900c-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="0900c-110">Exempel 2: Hämta mått definitioner med detaljerad utskrift</span><span class="sxs-lookup"><span data-stu-id="0900c-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
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

<span data-ttu-id="0900c-111">Det här kommandot hämtar mått definitioner för webbplats2.</span><span class="sxs-lookup"><span data-stu-id="0900c-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="0900c-112">Resultatet är detaljerat.</span><span class="sxs-lookup"><span data-stu-id="0900c-112">The output is detailed.</span></span>

### <span data-ttu-id="0900c-113">Exempel 3: Hämta mått definitioner efter namn</span><span class="sxs-lookup"><span data-stu-id="0900c-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
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

<span data-ttu-id="0900c-114">Det här kommandot får definitioner för måtten BytesSent och CpuTime.</span><span class="sxs-lookup"><span data-stu-id="0900c-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="0900c-115">Resultatet är detaljerat.</span><span class="sxs-lookup"><span data-stu-id="0900c-115">The output is detailed.</span></span>

## <span data-ttu-id="0900c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0900c-116">PARAMETERS</span></span>

### <span data-ttu-id="0900c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0900c-117">-DefaultProfile</span></span>
<span data-ttu-id="0900c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0900c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0900c-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="0900c-119">-DetailedOutput</span></span>
<span data-ttu-id="0900c-120">Anger att den här åtgärden innehöll detaljerade utdata.</span><span class="sxs-lookup"><span data-stu-id="0900c-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="0900c-121">Om du inte anger den här parametern sammanfattas utdata.</span><span class="sxs-lookup"><span data-stu-id="0900c-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="0900c-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="0900c-122">-MetricName</span></span>
<span data-ttu-id="0900c-123">Anger en matris med namn på mått.</span><span class="sxs-lookup"><span data-stu-id="0900c-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="0900c-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="0900c-124">-MetricNamespace</span></span>
<span data-ttu-id="0900c-125">Anger mått namn området för att fråga efter mått definitioner för.</span><span class="sxs-lookup"><span data-stu-id="0900c-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="0900c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0900c-126">-ResourceId</span></span>
<span data-ttu-id="0900c-127">Anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0900c-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="0900c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0900c-128">CommonParameters</span></span>
<span data-ttu-id="0900c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0900c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0900c-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0900c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0900c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0900c-131">INPUTS</span></span>

### <span data-ttu-id="0900c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0900c-132">System.String</span></span>

### <span data-ttu-id="0900c-133">System. string []</span><span class="sxs-lookup"><span data-stu-id="0900c-133">System.String[]</span></span>

## <span data-ttu-id="0900c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0900c-134">OUTPUTS</span></span>

### <span data-ttu-id="0900c-135">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="0900c-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="0900c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0900c-136">NOTES</span></span>

<span data-ttu-id="0900c-137">Mer information om de mät värden som stöds finns i: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="0900c-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="0900c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0900c-138">RELATED LINKS</span></span>

<span data-ttu-id="0900c-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="0900c-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


