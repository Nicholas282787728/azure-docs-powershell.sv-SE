---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585531"
---
# <span data-ttu-id="ed1bd-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed1bd-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="ed1bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1bd-103">Lägger till eller uppdaterar en aviserings regel för en webtest.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed1bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed1bd-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed1bd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed1bd-105">DESCRIPTION</span></span>
<span data-ttu-id="ed1bd-106">Cmdleten **Add-AzureRmWebtestAlertRule** lägger till eller uppdaterar en notifieringsregel för antingen Metric, event eller webtest.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="ed1bd-107">Den tillagda regeln associeras med en resurs grupp och har ett namn.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="ed1bd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed1bd-108">EXAMPLES</span></span>

### <span data-ttu-id="ed1bd-109">Exempel 1: Lägg till en aviserings regel för webtest</span><span class="sxs-lookup"><span data-stu-id="ed1bd-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="ed1bd-110">Det här kommandot lägger till eller uppdaterar en aviserings regel för webtest.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="ed1bd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed1bd-111">PARAMETERS</span></span>

### <span data-ttu-id="ed1bd-112">-Åtgärder</span><span class="sxs-lookup"><span data-stu-id="ed1bd-112">-Actions</span></span>
<span data-ttu-id="ed1bd-113">Anger en kommaavgränsad lista med åtgärder.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-113">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="ed1bd-114">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ed1bd-114">-Description</span></span>
<span data-ttu-id="ed1bd-115">Anger en beskrivning av regeln.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="ed1bd-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="ed1bd-116">-DisableRule</span></span>
<span data-ttu-id="ed1bd-117">Inaktiverar regeln.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-117">Disables the rule.</span></span>
<span data-ttu-id="ed1bd-118">Om du inte anger den här parametern aktive ras regeln.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-118">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="ed1bd-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="ed1bd-119">-FailedLocationCount</span></span>
<span data-ttu-id="ed1bd-120">Anger det misslyckade plats antalet för test reglerna.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="ed1bd-121">Detta liknar den tröskel som gäller för andra typer av regler.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-121">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="ed1bd-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="ed1bd-122">-Location</span></span>
<span data-ttu-id="ed1bd-123">Anger platsen där regeln är definierad.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-123">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="ed1bd-124">-MetricName</span><span class="sxs-lookup"><span data-stu-id="ed1bd-124">-MetricName</span></span>
<span data-ttu-id="ed1bd-125">Anger namnet på måttet.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-125">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="ed1bd-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="ed1bd-126">-MetricNamespace</span></span>
<span data-ttu-id="ed1bd-127">Anger mått namn området för regeln.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="ed1bd-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed1bd-128">-Name</span></span>
<span data-ttu-id="ed1bd-129">Anger namnet på regeln.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-129">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="ed1bd-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed1bd-130">-ResourceGroup</span></span>
<span data-ttu-id="ed1bd-131">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ed1bd-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="ed1bd-132">-TargetResourceUri</span></span>
<span data-ttu-id="ed1bd-133">Anger webbtestets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-133">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="ed1bd-134">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="ed1bd-134">-WindowSize</span></span>
<span data-ttu-id="ed1bd-135">Anger tidsfönstrets storlek för regeln för att beräkna dess data.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-135">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="ed1bd-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1bd-136">-DefaultProfile</span></span>
<span data-ttu-id="ed1bd-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed1bd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1bd-138">CommonParameters</span></span>
<span data-ttu-id="ed1bd-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed1bd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1bd-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed1bd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1bd-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed1bd-141">INPUTS</span></span>

## <span data-ttu-id="ed1bd-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed1bd-142">OUTPUTS</span></span>

### <span data-ttu-id="ed1bd-143">Microsoft. Azure. commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ed1bd-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="ed1bd-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed1bd-144">NOTES</span></span>

## <span data-ttu-id="ed1bd-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed1bd-145">RELATED LINKS</span></span>

[<span data-ttu-id="ed1bd-146">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed1bd-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="ed1bd-147">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed1bd-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="ed1bd-148">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="ed1bd-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="ed1bd-149">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="ed1bd-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


