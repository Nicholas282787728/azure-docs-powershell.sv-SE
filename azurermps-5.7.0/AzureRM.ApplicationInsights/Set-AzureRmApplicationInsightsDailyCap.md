---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 12e8e4f76f623391e6046f4f8b0bd424e7b9334d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755621"
---
# <span data-ttu-id="b8eb6-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="b8eb6-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="b8eb6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="b8eb6-103">Ange daglig data volym Cap för en program Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="b8eb6-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8eb6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8eb6-104">SYNTAX</span></span>

### <span data-ttu-id="b8eb6-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b8eb6-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8eb6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8eb6-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8eb6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8eb6-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8eb6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8eb6-108">DESCRIPTION</span></span>
<span data-ttu-id="b8eb6-109">Ange daglig data volym Cap för en program Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="b8eb6-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="b8eb6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8eb6-110">EXAMPLES</span></span>

### <span data-ttu-id="b8eb6-111">Exempel 1 Ange daglig data volym Cap för en program Insights-resurs</span><span class="sxs-lookup"><span data-stu-id="b8eb6-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="b8eb6-112">Ställ in den dagliga data volymen Cap till 400 GB per dag och sluta skicka meddelande när du trycker på resurs "test" i resurs gruppen "testgroup"</span><span class="sxs-lookup"><span data-stu-id="b8eb6-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="b8eb6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8eb6-113">PARAMETERS</span></span>

### <span data-ttu-id="b8eb6-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b8eb6-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b8eb6-115">Komponent objekt för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="b8eb6-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8eb6-116">-Confirm</span></span>
<span data-ttu-id="b8eb6-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8eb6-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="b8eb6-118">-DailyCapGB</span></span>
<span data-ttu-id="b8eb6-119">Dags kap.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-119">Daily Cap.</span></span>

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

### <span data-ttu-id="b8eb6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8eb6-120">-DefaultProfile</span></span>
<span data-ttu-id="b8eb6-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8eb6-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="b8eb6-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="b8eb6-123">Stoppa skicka meddelande när du är på.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-123">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="b8eb6-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8eb6-124">-Name</span></span>
<span data-ttu-id="b8eb6-125">Komponent namn för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-125">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="b8eb6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8eb6-126">-ResourceGroupName</span></span>
<span data-ttu-id="b8eb6-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b8eb6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8eb6-128">-ResourceId</span></span>
<span data-ttu-id="b8eb6-129">Komponent resurs-ID för Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="b8eb6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8eb6-130">-WhatIf</span></span>
<span data-ttu-id="b8eb6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8eb6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8eb6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8eb6-133">CommonParameters</span></span>
<span data-ttu-id="b8eb6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8eb6-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8eb6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8eb6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8eb6-136">INPUTS</span></span>

### <span data-ttu-id="b8eb6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b8eb6-137">System.String</span></span>
<span data-ttu-id="b8eb6-138">System. Double system. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8eb6-138">System.Double System.Boolean</span></span>

## <span data-ttu-id="b8eb6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8eb6-139">OUTPUTS</span></span>

### <span data-ttu-id="b8eb6-140">Microsoft. Azure. commands. ApplicationInsights. Models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="b8eb6-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="b8eb6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8eb6-141">NOTES</span></span>

## <span data-ttu-id="b8eb6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8eb6-142">RELATED LINKS</span></span>

