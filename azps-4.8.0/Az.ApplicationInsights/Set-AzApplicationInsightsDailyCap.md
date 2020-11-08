---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101203"
---
# <span data-ttu-id="efeef-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="efeef-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="efeef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="efeef-102">SYNOPSIS</span></span>
<span data-ttu-id="efeef-103">Ange daglig data volym Cap för en program Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="efeef-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="efeef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="efeef-104">SYNTAX</span></span>

### <span data-ttu-id="efeef-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="efeef-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efeef-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efeef-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efeef-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efeef-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efeef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="efeef-108">DESCRIPTION</span></span>
<span data-ttu-id="efeef-109">Ange daglig data volym Cap för en program Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="efeef-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="efeef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="efeef-110">EXAMPLES</span></span>

### <span data-ttu-id="efeef-111">Exempel 1 Ange daglig data volym Cap för en program Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="efeef-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="efeef-112">Ange daglig data volym Cap till 400 GB per dag och sluta skicka meddelande när du trycker på "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="efeef-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="efeef-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="efeef-113">PARAMETERS</span></span>

### <span data-ttu-id="efeef-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="efeef-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="efeef-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="efeef-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="efeef-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="efeef-116">-DailyCapGB</span></span>
<span data-ttu-id="efeef-117">Dags kap.</span><span class="sxs-lookup"><span data-stu-id="efeef-117">Daily Cap.</span></span>

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

### <span data-ttu-id="efeef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efeef-118">-DefaultProfile</span></span>
<span data-ttu-id="efeef-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="efeef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efeef-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="efeef-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="efeef-121">Stoppa skicka meddelande när du är på.</span><span class="sxs-lookup"><span data-stu-id="efeef-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="efeef-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="efeef-122">-Name</span></span>
<span data-ttu-id="efeef-123">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="efeef-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="efeef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efeef-124">-ResourceGroupName</span></span>
<span data-ttu-id="efeef-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="efeef-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="efeef-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efeef-126">-ResourceId</span></span>
<span data-ttu-id="efeef-127">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="efeef-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="efeef-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="efeef-128">-Confirm</span></span>
<span data-ttu-id="efeef-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="efeef-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efeef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efeef-130">-WhatIf</span></span>
<span data-ttu-id="efeef-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="efeef-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efeef-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="efeef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efeef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efeef-133">CommonParameters</span></span>
<span data-ttu-id="efeef-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efeef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efeef-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efeef-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efeef-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="efeef-136">INPUTS</span></span>

### <span data-ttu-id="efeef-137">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="efeef-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="efeef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="efeef-138">System.String</span></span>

## <span data-ttu-id="efeef-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="efeef-139">OUTPUTS</span></span>

### <span data-ttu-id="efeef-140">Microsoft. Azure. commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="efeef-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="efeef-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="efeef-141">NOTES</span></span>

## <span data-ttu-id="efeef-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="efeef-142">RELATED LINKS</span></span>
