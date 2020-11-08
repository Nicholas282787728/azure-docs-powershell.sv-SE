---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090531"
---
# <span data-ttu-id="48538-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="48538-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="48538-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48538-102">SYNOPSIS</span></span>
<span data-ttu-id="48538-103">Ange daglig data volym Cap för en program Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="48538-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="48538-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48538-104">SYNTAX</span></span>

### <span data-ttu-id="48538-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="48538-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48538-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48538-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48538-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48538-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48538-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48538-108">DESCRIPTION</span></span>
<span data-ttu-id="48538-109">Ange daglig data volym Cap för en program Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="48538-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="48538-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48538-110">EXAMPLES</span></span>

### <span data-ttu-id="48538-111">Exempel 1 Ange daglig data volym Cap för en program Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="48538-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="48538-112">Ange daglig data volym Cap till 400 GB per dag och sluta skicka meddelande när du trycker på "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="48538-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="48538-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48538-113">PARAMETERS</span></span>

### <span data-ttu-id="48538-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="48538-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="48538-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="48538-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="48538-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="48538-116">-DailyCapGB</span></span>
<span data-ttu-id="48538-117">Dags kap.</span><span class="sxs-lookup"><span data-stu-id="48538-117">Daily Cap.</span></span>

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

### <span data-ttu-id="48538-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48538-118">-DefaultProfile</span></span>
<span data-ttu-id="48538-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48538-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48538-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="48538-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="48538-121">Stoppa skicka meddelande när du är på.</span><span class="sxs-lookup"><span data-stu-id="48538-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="48538-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="48538-122">-Name</span></span>
<span data-ttu-id="48538-123">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="48538-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="48538-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48538-124">-ResourceGroupName</span></span>
<span data-ttu-id="48538-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="48538-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="48538-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48538-126">-ResourceId</span></span>
<span data-ttu-id="48538-127">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="48538-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="48538-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48538-128">-Confirm</span></span>
<span data-ttu-id="48538-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48538-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48538-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48538-130">-WhatIf</span></span>
<span data-ttu-id="48538-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48538-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48538-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48538-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48538-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48538-133">CommonParameters</span></span>
<span data-ttu-id="48538-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48538-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48538-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48538-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48538-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48538-136">INPUTS</span></span>

### <span data-ttu-id="48538-137">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="48538-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="48538-138">System. String</span><span class="sxs-lookup"><span data-stu-id="48538-138">System.String</span></span>

## <span data-ttu-id="48538-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48538-139">OUTPUTS</span></span>

### <span data-ttu-id="48538-140">Microsoft. Azure. commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="48538-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="48538-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48538-141">NOTES</span></span>

## <span data-ttu-id="48538-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48538-142">RELATED LINKS</span></span>
