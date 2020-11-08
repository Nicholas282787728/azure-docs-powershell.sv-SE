---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088927"
---
# <span data-ttu-id="7656b-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="7656b-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="7656b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7656b-102">SYNOPSIS</span></span>
<span data-ttu-id="7656b-103">Hämtar information om aviserings Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7656b-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="7656b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7656b-104">SYNTAX</span></span>

### <span data-ttu-id="7656b-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="7656b-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7656b-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="7656b-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7656b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7656b-107">DESCRIPTION</span></span>
<span data-ttu-id="7656b-108">**Mått – AzAlertStatistic** cmdlet får information om aviserings Sammanfattning.</span><span class="sxs-lookup"><span data-stu-id="7656b-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="7656b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7656b-109">EXAMPLES</span></span>

### <span data-ttu-id="7656b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7656b-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="7656b-111">Summera antalet aviseringar grupperade efter allvarlighets grad och status filtrerat efter aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="7656b-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="7656b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7656b-112">PARAMETERS</span></span>

### <span data-ttu-id="7656b-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="7656b-113">-AlertRuleId</span></span>
<span data-ttu-id="7656b-114">Filter för ID för notifieringsregel</span><span class="sxs-lookup"><span data-stu-id="7656b-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="7656b-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="7656b-115">-CustomTimeRange</span></span>
<span data-ttu-id="7656b-116">Format som stöds-Start-Time-Time-Time \< \> / \< \> i ISO-8601-format</span><span class="sxs-lookup"><span data-stu-id="7656b-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="7656b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7656b-117">-DefaultProfile</span></span>
<span data-ttu-id="7656b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7656b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7656b-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="7656b-119">-GroupBy</span></span>
<span data-ttu-id="7656b-120">Egenskapen sammanfatta efter</span><span class="sxs-lookup"><span data-stu-id="7656b-120">Summarize by property</span></span>

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

### <span data-ttu-id="7656b-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="7656b-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="7656b-122">Inkludera antal SmartGroups</span><span class="sxs-lookup"><span data-stu-id="7656b-122">Include SmartGroups Count</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7656b-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="7656b-123">-MonitorCondition</span></span>
<span data-ttu-id="7656b-124">Filtrerar på Monitor villkor</span><span class="sxs-lookup"><span data-stu-id="7656b-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="7656b-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="7656b-125">-MonitorService</span></span>
<span data-ttu-id="7656b-126">Filtrera på moniter-tjänsten</span><span class="sxs-lookup"><span data-stu-id="7656b-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="7656b-127">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="7656b-127">-Severity</span></span>
<span data-ttu-id="7656b-128">Filtrera på allvarlighets graden för aviseringar</span><span class="sxs-lookup"><span data-stu-id="7656b-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="7656b-129">-State</span><span class="sxs-lookup"><span data-stu-id="7656b-129">-State</span></span>
<span data-ttu-id="7656b-130">Filtrera efter status för avisering</span><span class="sxs-lookup"><span data-stu-id="7656b-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="7656b-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7656b-131">-TargetResourceGroup</span></span>
<span data-ttu-id="7656b-132">Filtrera efter resurs grupp namn för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="7656b-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7656b-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7656b-133">-TargetResourceId</span></span>
<span data-ttu-id="7656b-134">Filtrera efter resurs-ID för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="7656b-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7656b-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="7656b-135">-TargetResourceType</span></span>
<span data-ttu-id="7656b-136">Filtrera efter resurs typen för mål resursen för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="7656b-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7656b-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="7656b-137">-TimeRange</span></span>
<span data-ttu-id="7656b-138">Tidsintervalls värden som stöds – 1H, 1d, 7d, 30d (standard är 1d)</span><span class="sxs-lookup"><span data-stu-id="7656b-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="7656b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7656b-139">CommonParameters</span></span>
<span data-ttu-id="7656b-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7656b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7656b-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7656b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7656b-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7656b-142">INPUTS</span></span>

### <span data-ttu-id="7656b-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="7656b-143">None</span></span>

## <span data-ttu-id="7656b-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7656b-144">OUTPUTS</span></span>

### <span data-ttu-id="7656b-145">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="7656b-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="7656b-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7656b-146">NOTES</span></span>

## <span data-ttu-id="7656b-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7656b-147">RELATED LINKS</span></span>
