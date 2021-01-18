---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525569"
---
# <span data-ttu-id="95bbb-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="95bbb-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="95bbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="95bbb-103">Ta bort ett automatiskt svar från en analys.</span><span class="sxs-lookup"><span data-stu-id="95bbb-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="95bbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95bbb-104">SYNTAX</span></span>

### <span data-ttu-id="95bbb-105">ActionId (standard)</span><span class="sxs-lookup"><span data-stu-id="95bbb-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95bbb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="95bbb-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95bbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95bbb-107">DESCRIPTION</span></span>
<span data-ttu-id="95bbb-108">Cmdleten **Remove-AzSentinelAlertRuleAction** tar permanent bort ett automatiskt svar från notifieringsregeln på en angiven arbets yta.</span><span class="sxs-lookup"><span data-stu-id="95bbb-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="95bbb-109">Du kan skicka ett **AlertRuleAction** -objekt med pipeline-operatorn eller så kan du ange de parametrar som krävs.</span><span class="sxs-lookup"><span data-stu-id="95bbb-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="95bbb-110">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="95bbb-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="95bbb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95bbb-111">EXAMPLES</span></span>

### <span data-ttu-id="95bbb-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="95bbb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="95bbb-113">Det här kommandot tar bort notifieringsregeln från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="95bbb-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="95bbb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95bbb-114">PARAMETERS</span></span>

### <span data-ttu-id="95bbb-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="95bbb-115">-ActionId</span></span>
<span data-ttu-id="95bbb-116">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="95bbb-116">Action Id.</span></span>

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

### <span data-ttu-id="95bbb-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="95bbb-117">-AlertRuleId</span></span>
<span data-ttu-id="95bbb-118">ID för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="95bbb-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bbb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95bbb-119">-DefaultProfile</span></span>
<span data-ttu-id="95bbb-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95bbb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95bbb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95bbb-121">-InputObject</span></span>
<span data-ttu-id="95bbb-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="95bbb-122">InputObject.</span></span>

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

### <span data-ttu-id="95bbb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95bbb-123">-PassThru</span></span>
<span data-ttu-id="95bbb-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="95bbb-124">PassThru</span></span>

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

### <span data-ttu-id="95bbb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95bbb-125">-ResourceGroupName</span></span>
<span data-ttu-id="95bbb-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="95bbb-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bbb-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="95bbb-127">-WorkspaceName</span></span>
<span data-ttu-id="95bbb-128">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="95bbb-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bbb-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="95bbb-129">-Confirm</span></span>
<span data-ttu-id="95bbb-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95bbb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95bbb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95bbb-131">-WhatIf</span></span>
<span data-ttu-id="95bbb-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="95bbb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95bbb-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="95bbb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95bbb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bbb-134">CommonParameters</span></span>
<span data-ttu-id="95bbb-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95bbb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bbb-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95bbb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bbb-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95bbb-137">INPUTS</span></span>

### <span data-ttu-id="95bbb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="95bbb-138">System.String</span></span>
### <span data-ttu-id="95bbb-139">Microsoft. Azure. commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="95bbb-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="95bbb-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95bbb-140">OUTPUTS</span></span>

### <span data-ttu-id="95bbb-141">Microsoft. Azure. commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="95bbb-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="95bbb-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95bbb-142">NOTES</span></span>

## <span data-ttu-id="95bbb-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95bbb-143">RELATED LINKS</span></span>
