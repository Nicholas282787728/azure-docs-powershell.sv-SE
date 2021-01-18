---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525585"
---
# <span data-ttu-id="3ab3f-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="3ab3f-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="3ab3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ab3f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab3f-103">Lägga till ett automatiskt svar på en Analatic.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="3ab3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ab3f-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ab3f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ab3f-105">DESCRIPTION</span></span>
<span data-ttu-id="3ab3f-106">Cmdleten **New-AzSentinelAlertRuleAction** skapar ett automatiskt svar för en notifieringsregel på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="3ab3f-107">Du måste ange ID för logik programmet resorce och utlösa URI som kan hittas med programmet logik app.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="3ab3f-108">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3ab3f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ab3f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ab3f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3ab3f-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="3ab3f-111">I det här exemplet skapas en **AlertRuleAction** för den angivna notifieringsregeln med egenskaper för logik programmet och lagrar den sedan i $AlertRuleAction variabel.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="3ab3f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ab3f-112">PARAMETERS</span></span>

### <span data-ttu-id="3ab3f-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="3ab3f-113">-ActionId</span></span>
<span data-ttu-id="3ab3f-114">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-114">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab3f-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="3ab3f-115">-AlertRuleId</span></span>
<span data-ttu-id="3ab3f-116">ID för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="3ab3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab3f-117">-DefaultProfile</span></span>
<span data-ttu-id="3ab3f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ab3f-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="3ab3f-119">-LogicAppResourceId</span></span>
<span data-ttu-id="3ab3f-120">Program resurs-ID för åtgärds logik.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="3ab3f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab3f-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ab3f-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-122">Resource group name.</span></span>

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

### <span data-ttu-id="3ab3f-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="3ab3f-123">-TriggerUri</span></span>
<span data-ttu-id="3ab3f-124">Program utlösare URI för åtgärds logik.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="3ab3f-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ab3f-125">-WorkspaceName</span></span>
<span data-ttu-id="3ab3f-126">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-126">Workspace Name.</span></span>

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

### <span data-ttu-id="3ab3f-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ab3f-127">-Confirm</span></span>
<span data-ttu-id="3ab3f-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab3f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab3f-129">-WhatIf</span></span>
<span data-ttu-id="3ab3f-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ab3f-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab3f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab3f-132">CommonParameters</span></span>
<span data-ttu-id="3ab3f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ab3f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab3f-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ab3f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab3f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ab3f-135">INPUTS</span></span>

### <span data-ttu-id="3ab3f-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ab3f-136">None</span></span>
## <span data-ttu-id="3ab3f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ab3f-137">OUTPUTS</span></span>

### <span data-ttu-id="3ab3f-138">Microsoft. Azure. commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="3ab3f-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="3ab3f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ab3f-139">NOTES</span></span>

## <span data-ttu-id="3ab3f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ab3f-140">RELATED LINKS</span></span>
