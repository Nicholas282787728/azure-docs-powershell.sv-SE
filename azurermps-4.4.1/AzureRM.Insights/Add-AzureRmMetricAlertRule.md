---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758061"
---
# <span data-ttu-id="7d6ea-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7d6ea-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="7d6ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6ea-103">Lägger till eller uppdaterar en Metric-baserad notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d6ea-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d6ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d6ea-105">DESCRIPTION</span></span>
<span data-ttu-id="7d6ea-106">Cmdleten **Add-AzureRmMetricAlertRule** lägger till eller uppdaterar en Metric-baserad notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="7d6ea-107">Den tillagda regeln associeras med en resurs grupp och har ett namn.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="7d6ea-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d6ea-108">EXAMPLES</span></span>

### <span data-ttu-id="7d6ea-109">Exempel 1: lägga till en regel för att varna på en webbplats</span><span class="sxs-lookup"><span data-stu-id="7d6ea-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="7d6ea-110">Det här kommandot skapar en regel för att varna för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="7d6ea-111">Exempel 2: inaktivera en regel</span><span class="sxs-lookup"><span data-stu-id="7d6ea-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="7d6ea-112">Det här kommandot inaktiverar en regel.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-112">This command disables a rule.</span></span>
<span data-ttu-id="7d6ea-113">Om regeln inte finns skapas den avaktiverad.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="7d6ea-114">Om regeln finns inaktive ras den bara.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="7d6ea-115">Exempel 3: lägga till en regel med åtgärder</span><span class="sxs-lookup"><span data-stu-id="7d6ea-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="7d6ea-116">Det här kommandot skapar en regel för att varna för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="7d6ea-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d6ea-117">PARAMETERS</span></span>

### <span data-ttu-id="7d6ea-118">-Åtgärder</span><span class="sxs-lookup"><span data-stu-id="7d6ea-118">-Actions</span></span>
<span data-ttu-id="7d6ea-119">Anger en kommaavgränsad lista med åtgärder.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-119">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="7d6ea-120">-Description</span></span>
<span data-ttu-id="7d6ea-121">Anger en beskrivning av regeln.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-121">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="7d6ea-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="7d6ea-122">-DisableRule</span></span>
<span data-ttu-id="7d6ea-123">Inaktiverar regeln.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-123">Disables the rule.</span></span>
<span data-ttu-id="7d6ea-124">Om du inte anger den här parametern aktive ras regeln.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-124">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="7d6ea-125">-Location</span></span>
<span data-ttu-id="7d6ea-126">Anger platsen där regeln är definierad.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="7d6ea-127">-MetricName</span></span>
<span data-ttu-id="7d6ea-128">Anger namnet på det mått som regeln övervakar.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="7d6ea-129">Ange endast den här parametern för Metric-baserade regler.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-129">Specify this parameter only for metric-based rules.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d6ea-130">-Name</span></span>
<span data-ttu-id="7d6ea-131">Anger namnet på regeln.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-131">Specifies the name of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-132">-Operatör</span><span class="sxs-lookup"><span data-stu-id="7d6ea-132">-Operator</span></span>
<span data-ttu-id="7d6ea-133">Anger Relations operatorn för regelns villkor.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="7d6ea-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7d6ea-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d6ea-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="7d6ea-135">GreaterThan</span></span>
- <span data-ttu-id="7d6ea-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7d6ea-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="7d6ea-137">Mindreän</span><span class="sxs-lookup"><span data-stu-id="7d6ea-137">LessThan</span></span>
- <span data-ttu-id="7d6ea-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7d6ea-138">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-139">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7d6ea-139">-ResourceGroup</span></span>
<span data-ttu-id="7d6ea-140">Anger namnet på resurs gruppen för regeln.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-140">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-141">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7d6ea-141">-TargetResourceId</span></span>
<span data-ttu-id="7d6ea-142">Anger ID för den resurs som regeln övervakar.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="7d6ea-143">Obs! det går inte att uppdatera den här egenskapen för en befintlig notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-144">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="7d6ea-144">-Threshold</span></span>
<span data-ttu-id="7d6ea-145">Anger tröskeln för regeln.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-145">Specifies the threshold of the rule.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="7d6ea-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="7d6ea-147">Anger den mängd operator som ska användas för tidsfönstret när regeln utvärderas.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-148">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="7d6ea-148">-WindowSize</span></span>
<span data-ttu-id="7d6ea-149">Anger tidsfönstrets storlek för regeln för att beräkna dess data.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-149">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ea-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6ea-150">-DefaultProfile</span></span>
<span data-ttu-id="7d6ea-151">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d6ea-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6ea-152">CommonParameters</span></span>
<span data-ttu-id="7d6ea-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6ea-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6ea-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6ea-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6ea-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d6ea-155">INPUTS</span></span>

## <span data-ttu-id="7d6ea-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d6ea-156">OUTPUTS</span></span>

### <span data-ttu-id="7d6ea-157">Microsoft. Azure. commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7d6ea-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="7d6ea-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d6ea-158">NOTES</span></span>

## <span data-ttu-id="7d6ea-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d6ea-159">RELATED LINKS</span></span>

[<span data-ttu-id="7d6ea-160">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="7d6ea-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="7d6ea-161">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7d6ea-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="7d6ea-162">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="7d6ea-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="7d6ea-163">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7d6ea-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="7d6ea-164">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="7d6ea-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="7d6ea-165">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7d6ea-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="7d6ea-166">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7d6ea-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


