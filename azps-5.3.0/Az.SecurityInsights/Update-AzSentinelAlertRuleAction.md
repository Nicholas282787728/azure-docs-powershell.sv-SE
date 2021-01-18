---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 03eb85c423b06642a15db616b1ba1e0343c94963
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525560"
---
# <span data-ttu-id="ac395-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="ac395-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="ac395-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac395-102">SYNOPSIS</span></span>
<span data-ttu-id="ac395-103">Uppdatera ett automatiskt svar (varnings regel åtgärd).</span><span class="sxs-lookup"><span data-stu-id="ac395-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="ac395-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac395-104">SYNTAX</span></span>

### <span data-ttu-id="ac395-105">ActionId (standard)</span><span class="sxs-lookup"><span data-stu-id="ac395-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac395-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ac395-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac395-107">ID</span><span class="sxs-lookup"><span data-stu-id="ac395-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac395-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac395-108">DESCRIPTION</span></span>
<span data-ttu-id="ac395-109">Cmdleten **Update-AzSentinelAlertRuleAction** uppdaterar bok märket på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="ac395-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="ac395-110">Du kan skicka ett **AlertRuleAction** -objekt som en parameter eller med hjälp av pipeline-operatorn eller så kan du ange parametrarna *AlertRuleId* och *ActionId* .</span><span class="sxs-lookup"><span data-stu-id="ac395-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="ac395-111">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ac395-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ac395-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac395-112">EXAMPLES</span></span>

### <span data-ttu-id="ac395-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ac395-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="ac395-114">Det här exemplet uppdaterar en **AlertRuleAction** som ersätter en befintlig *åtgärd* med nya egenskaper.</span><span class="sxs-lookup"><span data-stu-id="ac395-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="ac395-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ac395-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="ac395-116">Det här exemplet uppdaterar en **AlertRuleAction** med hjälp av en InputObject som ersätter en befintlig *åtgärd* med nya egenskaper.</span><span class="sxs-lookup"><span data-stu-id="ac395-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="ac395-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac395-117">PARAMETERS</span></span>

### <span data-ttu-id="ac395-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="ac395-118">-ActionId</span></span>
<span data-ttu-id="ac395-119">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="ac395-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac395-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="ac395-120">-AlertRuleId</span></span>
<span data-ttu-id="ac395-121">ID för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="ac395-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac395-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac395-122">-DefaultProfile</span></span>
<span data-ttu-id="ac395-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac395-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac395-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac395-124">-InputObject</span></span>
<span data-ttu-id="ac395-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="ac395-125">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac395-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="ac395-126">-LogicAppResourceId</span></span>
<span data-ttu-id="ac395-127">Program resurs-ID för åtgärds logik.</span><span class="sxs-lookup"><span data-stu-id="ac395-127">Action Logic App Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac395-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac395-128">-ResourceGroupName</span></span>
<span data-ttu-id="ac395-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ac395-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac395-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac395-130">-ResourceId</span></span>
<span data-ttu-id="ac395-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ac395-131">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac395-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="ac395-132">-TriggerUri</span></span>
<span data-ttu-id="ac395-133">Program utlösare URI för åtgärds logik.</span><span class="sxs-lookup"><span data-stu-id="ac395-133">Action Logic App Trigger Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac395-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ac395-134">-WorkspaceName</span></span>
<span data-ttu-id="ac395-135">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="ac395-135">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac395-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ac395-136">-Confirm</span></span>
<span data-ttu-id="ac395-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ac395-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac395-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac395-138">-WhatIf</span></span>
<span data-ttu-id="ac395-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ac395-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac395-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ac395-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac395-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac395-141">CommonParameters</span></span>
<span data-ttu-id="ac395-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac395-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac395-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac395-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac395-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac395-144">INPUTS</span></span>

### <span data-ttu-id="ac395-145">Microsoft. Azure. commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="ac395-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="ac395-146">Microsoft. Azure. commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="ac395-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="ac395-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ac395-147">System.String</span></span>

## <span data-ttu-id="ac395-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac395-148">OUTPUTS</span></span>

### <span data-ttu-id="ac395-149">Microsoft. Azure. commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="ac395-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="ac395-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac395-150">NOTES</span></span>

## <span data-ttu-id="ac395-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac395-151">RELATED LINKS</span></span>
