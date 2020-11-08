---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273132"
---
# <span data-ttu-id="cbd4e-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cbd4e-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="cbd4e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd4e-103">Tar bort en regel för ett v2 (icke-klassiskt) mått.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="cbd4e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbd4e-104">SYNTAX</span></span>

### <span data-ttu-id="cbd4e-105">ByMetricRuleResourceName (standard)</span><span class="sxs-lookup"><span data-stu-id="cbd4e-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd4e-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd4e-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd4e-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="cbd4e-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbd4e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbd4e-108">DESCRIPTION</span></span>
<span data-ttu-id="cbd4e-109">Cmdleten **Remove-AzMetricAlertRuleV2** tar bort en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="cbd4e-110">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="cbd4e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbd4e-111">EXAMPLES</span></span>

### <span data-ttu-id="cbd4e-112">Exempel 1: ta bort en notifieringsregel efter namn</span><span class="sxs-lookup"><span data-stu-id="cbd4e-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="cbd4e-113">Det här kommandot tar bort notifieringsregeln som heter PsSdk</span><span class="sxs-lookup"><span data-stu-id="cbd4e-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="cbd4e-114">Exempel 2: ta bort en notifieringsregel efter ID</span><span class="sxs-lookup"><span data-stu-id="cbd4e-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="cbd4e-115">Det här kommandot tar bort notifieringsregeln med resurs-ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="cbd4e-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="cbd4e-116">Exempel 3: få ett varnings meddelande och ta bort det</span><span class="sxs-lookup"><span data-stu-id="cbd4e-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="cbd4e-117">Det här kommandot får en avisering och tar bort det.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="cbd4e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbd4e-118">PARAMETERS</span></span>

### <span data-ttu-id="cbd4e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbd4e-119">-AsJob</span></span>
<span data-ttu-id="cbd4e-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cbd4e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbd4e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd4e-121">-DefaultProfile</span></span>
<span data-ttu-id="cbd4e-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbd4e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbd4e-123">-InputObject</span></span>
<span data-ttu-id="cbd4e-124">Mått regel objekt</span><span class="sxs-lookup"><span data-stu-id="cbd4e-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd4e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbd4e-125">-Name</span></span>
<span data-ttu-id="cbd4e-126">Namnet på varnings regeln för mått</span><span class="sxs-lookup"><span data-stu-id="cbd4e-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd4e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbd4e-127">-PassThru</span></span>
<span data-ttu-id="cbd4e-128">Returnerar true när du har tagit bort den.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="cbd4e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd4e-129">-ResourceGroupName</span></span>
<span data-ttu-id="cbd4e-130">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd4e-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd4e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd4e-131">-ResourceId</span></span>
<span data-ttu-id="cbd4e-132">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd4e-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd4e-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbd4e-133">-Confirm</span></span>
<span data-ttu-id="cbd4e-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd4e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd4e-135">-WhatIf</span></span>
<span data-ttu-id="cbd4e-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbd4e-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd4e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd4e-138">CommonParameters</span></span>
<span data-ttu-id="cbd4e-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd4e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd4e-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbd4e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd4e-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbd4e-141">INPUTS</span></span>

### <span data-ttu-id="cbd4e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cbd4e-142">System.String</span></span>

### <span data-ttu-id="cbd4e-143">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cbd4e-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="cbd4e-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbd4e-144">OUTPUTS</span></span>

### <span data-ttu-id="cbd4e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbd4e-145">System.Boolean</span></span>

## <span data-ttu-id="cbd4e-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbd4e-146">NOTES</span></span>

## <span data-ttu-id="cbd4e-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbd4e-147">RELATED LINKS</span></span>
