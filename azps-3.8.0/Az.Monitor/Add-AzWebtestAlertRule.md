---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092744"
---
# <span data-ttu-id="ae2c4-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae2c4-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="ae2c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2c4-103">Lägger till eller uppdaterar en aviserings regel för en webtest.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="ae2c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae2c4-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae2c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae2c4-105">DESCRIPTION</span></span>
<span data-ttu-id="ae2c4-106">Cmdleten **Add-AzWebtestAlertRule** lägger till eller uppdaterar en notifieringsregel för antingen Metric, event eller webtest.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="ae2c4-107">Den tillagda regeln associeras med en resurs grupp och har ett namn.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="ae2c4-108">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ae2c4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae2c4-109">EXAMPLES</span></span>

### <span data-ttu-id="ae2c4-110">Exempel 1: Lägg till en aviserings regel för webtest</span><span class="sxs-lookup"><span data-stu-id="ae2c4-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="ae2c4-111">Det här kommandot lägger till eller uppdaterar en aviserings regel för webtest.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="ae2c4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae2c4-112">PARAMETERS</span></span>

### <span data-ttu-id="ae2c4-113">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="ae2c4-113">-Action</span></span>
<span data-ttu-id="ae2c4-114">Anger en kommaavgränsad lista med åtgärder.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="ae2c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2c4-115">-DefaultProfile</span></span>
<span data-ttu-id="ae2c4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ae2c4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae2c4-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ae2c4-117">-Description</span></span>
<span data-ttu-id="ae2c4-118">Anger en beskrivning av regeln.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="ae2c4-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="ae2c4-119">-DisableRule</span></span>
<span data-ttu-id="ae2c4-120">Inaktiverar regeln.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-120">Disables the rule.</span></span>
<span data-ttu-id="ae2c4-121">Om du inte anger den här parametern aktive ras regeln.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="ae2c4-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="ae2c4-122">-FailedLocationCount</span></span>
<span data-ttu-id="ae2c4-123">Anger det misslyckade plats antalet för test reglerna.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="ae2c4-124">Detta liknar den tröskel som gäller för andra typer av regler.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae2c4-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="ae2c4-125">-Location</span></span>
<span data-ttu-id="ae2c4-126">Anger platsen där regeln är definierad.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="ae2c4-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="ae2c4-127">-MetricName</span></span>
<span data-ttu-id="ae2c4-128">Anger namnet på måttet.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="ae2c4-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="ae2c4-129">-MetricNamespace</span></span>
<span data-ttu-id="ae2c4-130">Anger mått namn området för regeln.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="ae2c4-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae2c4-131">-Name</span></span>
<span data-ttu-id="ae2c4-132">Anger namnet på regeln.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="ae2c4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2c4-133">-ResourceGroupName</span></span>
<span data-ttu-id="ae2c4-134">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ae2c4-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="ae2c4-135">-TargetResourceUri</span></span>
<span data-ttu-id="ae2c4-136">Anger webbtestets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="ae2c4-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="ae2c4-137">-WindowSize</span></span>
<span data-ttu-id="ae2c4-138">Anger tidsfönstrets storlek för regeln för att beräkna dess data.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="ae2c4-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae2c4-139">-Confirm</span></span>
<span data-ttu-id="ae2c4-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae2c4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae2c4-141">-WhatIf</span></span>
<span data-ttu-id="ae2c4-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae2c4-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae2c4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2c4-144">CommonParameters</span></span>
<span data-ttu-id="ae2c4-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae2c4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2c4-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae2c4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2c4-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae2c4-147">INPUTS</span></span>

### <span data-ttu-id="ae2c4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ae2c4-148">System.String</span></span>

### <span data-ttu-id="ae2c4-149">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="ae2c4-149">System.TimeSpan</span></span>

### <span data-ttu-id="ae2c4-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ae2c4-150">System.Int32</span></span>

### <span data-ttu-id="ae2c4-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ae2c4-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ae2c4-152">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitoring. Management. Models. RuleAction, Microsoft. Azure. PowerShell. cmdletar. Monitor, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ae2c4-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ae2c4-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae2c4-153">OUTPUTS</span></span>

### <span data-ttu-id="ae2c4-154">Microsoft. Azure. commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ae2c4-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="ae2c4-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae2c4-155">NOTES</span></span>

## <span data-ttu-id="ae2c4-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae2c4-156">RELATED LINKS</span></span>

[<span data-ttu-id="ae2c4-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ae2c4-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="ae2c4-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae2c4-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="ae2c4-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="ae2c4-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="ae2c4-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="ae2c4-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


