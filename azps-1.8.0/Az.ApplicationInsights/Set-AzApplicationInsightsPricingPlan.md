---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 33b55c70d88daf8493012945f49794c25e62b474
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754884"
---
# <span data-ttu-id="47ab5-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="47ab5-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="47ab5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="47ab5-103">Ange information om ett pris och daglig data volym för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="47ab5-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="47ab5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47ab5-104">SYNTAX</span></span>

### <span data-ttu-id="47ab5-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="47ab5-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ab5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47ab5-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ab5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47ab5-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47ab5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47ab5-108">DESCRIPTION</span></span>
<span data-ttu-id="47ab5-109">Ange information om ett pris och daglig data volym för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="47ab5-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="47ab5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47ab5-110">EXAMPLES</span></span>

### <span data-ttu-id="47ab5-111">Exempel 1 Ange prissättnings-och daglig data volym information för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="47ab5-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="47ab5-112">Ställ in pris modellen till "grundläggande", Ställ in den dagliga data volymen Cap till 400 GB per dag och sluta skicka avisering när du är klar med resursen "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="47ab5-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="47ab5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47ab5-113">PARAMETERS</span></span>

### <span data-ttu-id="47ab5-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="47ab5-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="47ab5-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="47ab5-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="47ab5-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="47ab5-116">-DailyCapGB</span></span>
<span data-ttu-id="47ab5-117">Dags kap.</span><span class="sxs-lookup"><span data-stu-id="47ab5-117">Daily Cap.</span></span>

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

### <span data-ttu-id="47ab5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ab5-118">-DefaultProfile</span></span>
<span data-ttu-id="47ab5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47ab5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47ab5-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="47ab5-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="47ab5-121">Stoppa skicka meddelande när du är på.</span><span class="sxs-lookup"><span data-stu-id="47ab5-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="47ab5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="47ab5-122">-Name</span></span>
<span data-ttu-id="47ab5-123">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="47ab5-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="47ab5-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="47ab5-124">-PricingPlan</span></span>
<span data-ttu-id="47ab5-125">Namn på prissättnings abonnemang.</span><span class="sxs-lookup"><span data-stu-id="47ab5-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="47ab5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47ab5-126">-ResourceGroupName</span></span>
<span data-ttu-id="47ab5-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="47ab5-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="47ab5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47ab5-128">-ResourceId</span></span>
<span data-ttu-id="47ab5-129">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="47ab5-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="47ab5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="47ab5-130">-Confirm</span></span>
<span data-ttu-id="47ab5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47ab5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ab5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ab5-132">-WhatIf</span></span>
<span data-ttu-id="47ab5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="47ab5-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47ab5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="47ab5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ab5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ab5-135">CommonParameters</span></span>
<span data-ttu-id="47ab5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ab5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ab5-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ab5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ab5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47ab5-138">INPUTS</span></span>

### <span data-ttu-id="47ab5-139">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="47ab5-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="47ab5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="47ab5-140">System.String</span></span>

## <span data-ttu-id="47ab5-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47ab5-141">OUTPUTS</span></span>

### <span data-ttu-id="47ab5-142">Microsoft. Azure. commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="47ab5-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="47ab5-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47ab5-143">NOTES</span></span>

## <span data-ttu-id="47ab5-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47ab5-144">RELATED LINKS</span></span>
