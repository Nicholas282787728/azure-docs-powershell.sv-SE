---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: 698f05840df6578d8595e2ca8e31c9f0a11bc722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754021"
---
# <span data-ttu-id="63974-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="63974-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="63974-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63974-102">SYNOPSIS</span></span>
<span data-ttu-id="63974-103">Tar bort en regel för ett v2 (icke-klassiskt) mått.</span><span class="sxs-lookup"><span data-stu-id="63974-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="63974-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63974-104">SYNTAX</span></span>

### <span data-ttu-id="63974-105">ByMetricRuleResourceName</span><span class="sxs-lookup"><span data-stu-id="63974-105">ByMetricRuleResourceName</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63974-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="63974-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63974-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="63974-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63974-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63974-108">DESCRIPTION</span></span>
<span data-ttu-id="63974-109">Cmdleten **Remove-AzMetricAlertRuleV2** tar bort en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="63974-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="63974-110">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="63974-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="63974-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63974-111">EXAMPLES</span></span>

### <span data-ttu-id="63974-112">Exempel 1: ta bort en notifieringsregel efter namn</span><span class="sxs-lookup"><span data-stu-id="63974-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="63974-113">Det här kommandot tar bort notifieringsregeln som heter PsSdk</span><span class="sxs-lookup"><span data-stu-id="63974-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="63974-114">Exempel 2: ta bort en notifieringsregel efter ID</span><span class="sxs-lookup"><span data-stu-id="63974-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="63974-115">Det här kommandot tar bort notifieringsregeln med resurs-ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="63974-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>
### <span data-ttu-id="63974-116">Exempel 3: få ett varnings meddelande och ta bort det</span><span class="sxs-lookup"><span data-stu-id="63974-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="63974-117">Det här kommandot får en avisering och tar bort det.</span><span class="sxs-lookup"><span data-stu-id="63974-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="63974-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63974-118">PARAMETERS</span></span>

### <span data-ttu-id="63974-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63974-119">-AsJob</span></span>
<span data-ttu-id="63974-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="63974-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63974-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63974-121">-Confirm</span></span>
<span data-ttu-id="63974-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63974-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63974-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63974-123">-DefaultProfile</span></span>
<span data-ttu-id="63974-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63974-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63974-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63974-125">-InputObject</span></span>
<span data-ttu-id="63974-126">Mått regel objekt</span><span class="sxs-lookup"><span data-stu-id="63974-126">The Metric rule object</span></span>

```yaml
Type: PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63974-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="63974-127">-Name</span></span>
<span data-ttu-id="63974-128">Namnet på varnings regeln för mått</span><span class="sxs-lookup"><span data-stu-id="63974-128">The name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63974-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63974-129">-PassThru</span></span>
<span data-ttu-id="63974-130">Returnerar true när du har tagit bort den.</span><span class="sxs-lookup"><span data-stu-id="63974-130">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="63974-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63974-131">-ResourceGroupName</span></span>
<span data-ttu-id="63974-132">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63974-132">The ResourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63974-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63974-133">-ResourceId</span></span>
<span data-ttu-id="63974-134">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="63974-134">The RuleResourceId</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63974-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63974-135">-WhatIf</span></span>
<span data-ttu-id="63974-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63974-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63974-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63974-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63974-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63974-138">CommonParameters</span></span>
<span data-ttu-id="63974-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63974-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="63974-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63974-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63974-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63974-141">INPUTS</span></span>

### <span data-ttu-id="63974-142">System. String</span><span class="sxs-lookup"><span data-stu-id="63974-142">System.String</span></span>

### <span data-ttu-id="63974-143">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="63974-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="63974-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63974-144">OUTPUTS</span></span>

### <span data-ttu-id="63974-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63974-145">System.Boolean</span></span>

## <span data-ttu-id="63974-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63974-146">NOTES</span></span>

## <span data-ttu-id="63974-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63974-147">RELATED LINKS</span></span>
