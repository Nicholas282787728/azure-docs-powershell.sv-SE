---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 4785abb883c262273d8d3b0798067e76092511fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583219"
---
# <span data-ttu-id="db5f4-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="db5f4-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="db5f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="db5f4-103">Ange information om ett pris och daglig data volym för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="db5f4-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db5f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db5f4-104">SYNTAX</span></span>

### <span data-ttu-id="db5f4-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="db5f4-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5f4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5f4-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5f4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5f4-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db5f4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db5f4-108">DESCRIPTION</span></span>
<span data-ttu-id="db5f4-109">Ange information om ett pris och daglig data volym för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="db5f4-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="db5f4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db5f4-110">EXAMPLES</span></span>

### <span data-ttu-id="db5f4-111">Exempel 1 Ange prissättnings-och daglig data volym information för en Application Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="db5f4-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="db5f4-112">Ställ in pris modellen till "grundläggande", Ställ in den dagliga data volymen Cap till 400 GB per dag och sluta skicka avisering när du är klar med resursen "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="db5f4-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="db5f4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db5f4-113">PARAMETERS</span></span>

### <span data-ttu-id="db5f4-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="db5f4-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="db5f4-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="db5f4-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db5f4-116">-Confirm</span></span>
<span data-ttu-id="db5f4-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db5f4-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="db5f4-118">-DailyCapGB</span></span>
<span data-ttu-id="db5f4-119">Dags kap.</span><span class="sxs-lookup"><span data-stu-id="db5f4-119">Daily Cap.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5f4-120">-DefaultProfile</span></span>
<span data-ttu-id="db5f4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db5f4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="db5f4-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="db5f4-123">Stoppa skicka meddelande när du är på.</span><span class="sxs-lookup"><span data-stu-id="db5f4-123">Stop send notification when hit cap.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="db5f4-124">-Name</span></span>
<span data-ttu-id="db5f4-125">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="db5f4-125">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-126">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="db5f4-126">-PricingPlan</span></span>
<span data-ttu-id="db5f4-127">Namn på prissättnings abonnemang.</span><span class="sxs-lookup"><span data-stu-id="db5f4-127">Pricing plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db5f4-128">-ResourceGroupName</span></span>
<span data-ttu-id="db5f4-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="db5f4-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db5f4-130">-ResourceId</span></span>
<span data-ttu-id="db5f4-131">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="db5f4-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db5f4-132">-WhatIf</span></span>
<span data-ttu-id="db5f4-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db5f4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db5f4-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db5f4-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5f4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5f4-135">CommonParameters</span></span>
<span data-ttu-id="db5f4-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db5f4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5f4-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db5f4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5f4-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db5f4-138">INPUTS</span></span>

### <span data-ttu-id="db5f4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="db5f4-139">System.String</span></span>
<span data-ttu-id="db5f4-140">System. Double system. Boolean</span><span class="sxs-lookup"><span data-stu-id="db5f4-140">System.Double System.Boolean</span></span>

## <span data-ttu-id="db5f4-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db5f4-141">OUTPUTS</span></span>

### <span data-ttu-id="db5f4-142">Microsoft. Azure. commands. ApplicationInsights. Models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="db5f4-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="db5f4-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db5f4-143">NOTES</span></span>

## <span data-ttu-id="db5f4-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db5f4-144">RELATED LINKS</span></span>

