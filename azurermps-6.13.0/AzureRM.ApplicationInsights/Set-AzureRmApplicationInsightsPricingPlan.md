---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 03c1a556f6b3fc207fbbb612f31d172705e4f42b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575362"
---
# <span data-ttu-id="14bc1-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="14bc1-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="14bc1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="14bc1-103">Ange information om ett pris och daglig data volym för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="14bc1-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14bc1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14bc1-104">SYNTAX</span></span>

### <span data-ttu-id="14bc1-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="14bc1-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14bc1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14bc1-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14bc1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14bc1-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14bc1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14bc1-108">DESCRIPTION</span></span>
<span data-ttu-id="14bc1-109">Ange information om ett pris och daglig data volym för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="14bc1-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="14bc1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14bc1-110">EXAMPLES</span></span>

### <span data-ttu-id="14bc1-111">Exempel 1 Ange prissättnings-och daglig data volym information för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="14bc1-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="14bc1-112">Ställ in pris modellen till "grundläggande", Ställ in den dagliga data volymen Cap till 400 GB per dag och sluta skicka avisering när du är klar med resursen "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="14bc1-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="14bc1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14bc1-113">PARAMETERS</span></span>

### <span data-ttu-id="14bc1-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="14bc1-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="14bc1-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="14bc1-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="14bc1-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="14bc1-116">-DailyCapGB</span></span>
<span data-ttu-id="14bc1-117">Dags kap.</span><span class="sxs-lookup"><span data-stu-id="14bc1-117">Daily Cap.</span></span>

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

### <span data-ttu-id="14bc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14bc1-118">-DefaultProfile</span></span>
<span data-ttu-id="14bc1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14bc1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14bc1-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="14bc1-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="14bc1-121">Stoppa skicka meddelande när du är på.</span><span class="sxs-lookup"><span data-stu-id="14bc1-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="14bc1-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="14bc1-122">-Name</span></span>
<span data-ttu-id="14bc1-123">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="14bc1-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="14bc1-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="14bc1-124">-PricingPlan</span></span>
<span data-ttu-id="14bc1-125">Namn på prissättnings abonnemang.</span><span class="sxs-lookup"><span data-stu-id="14bc1-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="14bc1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14bc1-126">-ResourceGroupName</span></span>
<span data-ttu-id="14bc1-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="14bc1-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="14bc1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14bc1-128">-ResourceId</span></span>
<span data-ttu-id="14bc1-129">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="14bc1-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="14bc1-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="14bc1-130">-Confirm</span></span>
<span data-ttu-id="14bc1-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14bc1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14bc1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14bc1-132">-WhatIf</span></span>
<span data-ttu-id="14bc1-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14bc1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14bc1-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="14bc1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14bc1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14bc1-135">CommonParameters</span></span>
<span data-ttu-id="14bc1-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14bc1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14bc1-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14bc1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14bc1-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14bc1-138">INPUTS</span></span>

### <span data-ttu-id="14bc1-139">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="14bc1-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="14bc1-140">Parametrar: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="14bc1-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="14bc1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="14bc1-141">System.String</span></span>

## <span data-ttu-id="14bc1-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14bc1-142">OUTPUTS</span></span>

### <span data-ttu-id="14bc1-143">Microsoft. Azure. commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="14bc1-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="14bc1-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14bc1-144">NOTES</span></span>

## <span data-ttu-id="14bc1-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14bc1-145">RELATED LINKS</span></span>
