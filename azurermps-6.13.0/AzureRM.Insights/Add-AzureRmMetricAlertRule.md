---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 155a34133b9fa03c1f056fd65a0ec202fc0aed72
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755712"
---
# <span data-ttu-id="fd215-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd215-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="fd215-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd215-102">SYNOPSIS</span></span>
<span data-ttu-id="fd215-103">Lägger till eller uppdaterar en Metric-baserad notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="fd215-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd215-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd215-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd215-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd215-105">DESCRIPTION</span></span>
<span data-ttu-id="fd215-106">Cmdleten **Add-AzureRmMetricAlertRule** lägger till eller uppdaterar en Metric-baserad notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="fd215-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="fd215-107">Den tillagda regeln associeras med en resurs grupp och har ett namn.</span><span class="sxs-lookup"><span data-stu-id="fd215-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="fd215-108">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="fd215-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="fd215-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd215-109">EXAMPLES</span></span>

### <span data-ttu-id="fd215-110">Exempel 1: lägga till en regel för att varna på en webbplats</span><span class="sxs-lookup"><span data-stu-id="fd215-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="fd215-111">Det här kommandot skapar en regel för att varna för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="fd215-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="fd215-112">Exempel 2: inaktivera en regel</span><span class="sxs-lookup"><span data-stu-id="fd215-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="fd215-113">Det här kommandot inaktiverar en regel.</span><span class="sxs-lookup"><span data-stu-id="fd215-113">This command disables a rule.</span></span>
<span data-ttu-id="fd215-114">Om regeln inte finns skapas den avaktiverad.</span><span class="sxs-lookup"><span data-stu-id="fd215-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="fd215-115">Om regeln finns inaktive ras den bara.</span><span class="sxs-lookup"><span data-stu-id="fd215-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="fd215-116">Exempel 3: lägga till en regel med åtgärder</span><span class="sxs-lookup"><span data-stu-id="fd215-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="fd215-117">Det här kommandot skapar en regel för att varna för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="fd215-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="fd215-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd215-118">PARAMETERS</span></span>

### <span data-ttu-id="fd215-119">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="fd215-119">-Action</span></span>
<span data-ttu-id="fd215-120">Anger en kommaavgränsad lista med åtgärder.</span><span class="sxs-lookup"><span data-stu-id="fd215-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="fd215-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd215-121">-DefaultProfile</span></span>
<span data-ttu-id="fd215-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fd215-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd215-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="fd215-123">-Description</span></span>
<span data-ttu-id="fd215-124">Anger en beskrivning av regeln.</span><span class="sxs-lookup"><span data-stu-id="fd215-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="fd215-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="fd215-125">-DisableRule</span></span>
<span data-ttu-id="fd215-126">Inaktiverar regeln.</span><span class="sxs-lookup"><span data-stu-id="fd215-126">Disables the rule.</span></span>
<span data-ttu-id="fd215-127">Om du inte anger den här parametern aktive ras regeln.</span><span class="sxs-lookup"><span data-stu-id="fd215-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="fd215-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="fd215-128">-Location</span></span>
<span data-ttu-id="fd215-129">Anger platsen där regeln är definierad.</span><span class="sxs-lookup"><span data-stu-id="fd215-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="fd215-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="fd215-130">-MetricName</span></span>
<span data-ttu-id="fd215-131">Anger namnet på det mått som regeln övervakar.</span><span class="sxs-lookup"><span data-stu-id="fd215-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="fd215-132">Ange endast den här parametern för Metric-baserade regler.</span><span class="sxs-lookup"><span data-stu-id="fd215-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="fd215-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="fd215-133">-Name</span></span>
<span data-ttu-id="fd215-134">Anger namnet på regeln.</span><span class="sxs-lookup"><span data-stu-id="fd215-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="fd215-135">-Operatör</span><span class="sxs-lookup"><span data-stu-id="fd215-135">-Operator</span></span>
<span data-ttu-id="fd215-136">Anger Relations operatorn för regelns villkor.</span><span class="sxs-lookup"><span data-stu-id="fd215-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="fd215-137">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fd215-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd215-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="fd215-138">GreaterThan</span></span>
- <span data-ttu-id="fd215-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="fd215-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="fd215-140">Mindreän</span><span class="sxs-lookup"><span data-stu-id="fd215-140">LessThan</span></span>
- <span data-ttu-id="fd215-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="fd215-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="fd215-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd215-142">-ResourceGroupName</span></span>
<span data-ttu-id="fd215-143">Anger namnet på resurs gruppen för regeln.</span><span class="sxs-lookup"><span data-stu-id="fd215-143">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd215-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="fd215-144">-TargetResourceId</span></span>
<span data-ttu-id="fd215-145">Anger ID för den resurs som regeln övervakar.</span><span class="sxs-lookup"><span data-stu-id="fd215-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="fd215-146">Obs! det går inte att uppdatera den här egenskapen för en befintlig notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="fd215-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="fd215-147">-Tröskel</span><span class="sxs-lookup"><span data-stu-id="fd215-147">-Threshold</span></span>
<span data-ttu-id="fd215-148">Anger tröskeln för regeln.</span><span class="sxs-lookup"><span data-stu-id="fd215-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="fd215-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="fd215-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="fd215-150">Anger den mängd operator som ska användas för tidsfönstret när regeln utvärderas.</span><span class="sxs-lookup"><span data-stu-id="fd215-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="fd215-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="fd215-151">-WindowSize</span></span>
<span data-ttu-id="fd215-152">Anger tidsfönstrets storlek för regeln för att beräkna dess data.</span><span class="sxs-lookup"><span data-stu-id="fd215-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="fd215-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd215-153">-Confirm</span></span>
<span data-ttu-id="fd215-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd215-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd215-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd215-155">-WhatIf</span></span>
<span data-ttu-id="fd215-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd215-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd215-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd215-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd215-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd215-158">CommonParameters</span></span>
<span data-ttu-id="fd215-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd215-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd215-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd215-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd215-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd215-161">INPUTS</span></span>

### <span data-ttu-id="fd215-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="fd215-162">System.TimeSpan</span></span>

### <span data-ttu-id="fd215-163">Microsoft. Azure. Management. Monitoring. Management. Models. ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="fd215-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="fd215-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="fd215-164">System.Double</span></span>

### <span data-ttu-id="fd215-165">System. String</span><span class="sxs-lookup"><span data-stu-id="fd215-165">System.String</span></span>

### <span data-ttu-id="fd215-166">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. TimeAggregationOperator, Microsoft. Azure. commands. Insights, version = 5.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fd215-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="fd215-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fd215-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fd215-168">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitoring. Management. Models. RuleAction, Microsoft. Azure. commands. Insights, version = 5.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fd215-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fd215-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd215-169">OUTPUTS</span></span>

### <span data-ttu-id="fd215-170">Microsoft. Azure. commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fd215-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="fd215-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd215-171">NOTES</span></span>

## <span data-ttu-id="fd215-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd215-172">RELATED LINKS</span></span>

[<span data-ttu-id="fd215-173">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fd215-173">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fd215-174">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd215-174">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="fd215-175">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="fd215-175">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="fd215-176">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd215-176">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="fd215-177">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="fd215-177">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="fd215-178">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="fd215-178">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="fd215-179">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd215-179">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


