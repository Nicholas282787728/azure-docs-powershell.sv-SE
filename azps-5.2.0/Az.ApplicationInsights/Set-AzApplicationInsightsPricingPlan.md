---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406736"
---
# <span data-ttu-id="78d3b-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="78d3b-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="78d3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="78d3b-103">Ange information om ett pris och daglig data volym för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="78d3b-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="78d3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78d3b-104">SYNTAX</span></span>

### <span data-ttu-id="78d3b-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="78d3b-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d3b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d3b-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d3b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d3b-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78d3b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78d3b-108">DESCRIPTION</span></span>
<span data-ttu-id="78d3b-109">Ange prissättnings-och daglig data volym information för en Application Insights-resurs.</span><span class="sxs-lookup"><span data-stu-id="78d3b-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="78d3b-110">Pris plan för insikter från program som skapats efter april 2018 kan inte anges av denna cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="78d3b-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="78d3b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78d3b-111">EXAMPLES</span></span>

### <span data-ttu-id="78d3b-112">Exempel 1 Ange prissättnings-och daglig data volym information för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="78d3b-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="78d3b-113">Ställ in prissättningen på "grundläggande", ange daglig data volym Cap till 400 GB per dag och stoppa skicka-avisering när du är på resurs "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="78d3b-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="78d3b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78d3b-114">PARAMETERS</span></span>

### <span data-ttu-id="78d3b-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="78d3b-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="78d3b-116">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="78d3b-116">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78d3b-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="78d3b-117">-DailyCapGB</span></span>
<span data-ttu-id="78d3b-118">Dags kap.</span><span class="sxs-lookup"><span data-stu-id="78d3b-118">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d3b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d3b-119">-DefaultProfile</span></span>
<span data-ttu-id="78d3b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78d3b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78d3b-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="78d3b-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="78d3b-122">Stoppa skicka meddelande när du är på.</span><span class="sxs-lookup"><span data-stu-id="78d3b-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="78d3b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="78d3b-123">-Name</span></span>
<span data-ttu-id="78d3b-124">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="78d3b-124">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d3b-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="78d3b-125">-PricingPlan</span></span>
<span data-ttu-id="78d3b-126">Namn på prissättnings abonnemang.</span><span class="sxs-lookup"><span data-stu-id="78d3b-126">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d3b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d3b-127">-ResourceGroupName</span></span>
<span data-ttu-id="78d3b-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="78d3b-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d3b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78d3b-129">-ResourceId</span></span>
<span data-ttu-id="78d3b-130">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="78d3b-130">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d3b-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78d3b-131">-Confirm</span></span>
<span data-ttu-id="78d3b-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78d3b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d3b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d3b-133">-WhatIf</span></span>
<span data-ttu-id="78d3b-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78d3b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78d3b-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78d3b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d3b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d3b-136">CommonParameters</span></span>
<span data-ttu-id="78d3b-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d3b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d3b-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78d3b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d3b-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78d3b-139">INPUTS</span></span>

### <span data-ttu-id="78d3b-140">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="78d3b-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="78d3b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="78d3b-141">System.String</span></span>

## <span data-ttu-id="78d3b-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78d3b-142">OUTPUTS</span></span>

### <span data-ttu-id="78d3b-143">Microsoft. Azure. commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="78d3b-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="78d3b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78d3b-144">NOTES</span></span>

## <span data-ttu-id="78d3b-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78d3b-145">RELATED LINKS</span></span>
