---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: 415a4156831d00672aba5709d3f915625adac106
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525571"
---
# <span data-ttu-id="fbfc6-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fbfc6-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="fbfc6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbfc6-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfc6-103">Ta bort en analys.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-103">Delete an Analytic.</span></span>

## <span data-ttu-id="fbfc6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbfc6-104">SYNTAX</span></span>

### <span data-ttu-id="fbfc6-105">AlertRuleId (standard)</span><span class="sxs-lookup"><span data-stu-id="fbfc6-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbfc6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fbfc6-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbfc6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbfc6-107">DESCRIPTION</span></span>
<span data-ttu-id="fbfc6-108">Cmdleten **Remove-AzSentinelAlertRule** tar permanent bort en notifieringsregel från en angiven arbets yta.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="fbfc6-109">Du kan skicka ett **AlertRule** -objekt med pipeline-operatorn eller så kan du ange de parametrar som krävs.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="fbfc6-110">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="fbfc6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbfc6-111">EXAMPLES</span></span>

### <span data-ttu-id="fbfc6-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fbfc6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="fbfc6-113">Det här kommandot tar bort notifieringsregeln från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="fbfc6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbfc6-114">PARAMETERS</span></span>

### <span data-ttu-id="fbfc6-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="fbfc6-115">-AlertRuleId</span></span>
<span data-ttu-id="fbfc6-116">ID för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbfc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfc6-117">-DefaultProfile</span></span>
<span data-ttu-id="fbfc6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbfc6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbfc6-119">-InputObject</span></span>
<span data-ttu-id="fbfc6-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbfc6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbfc6-121">-PassThru</span></span>
<span data-ttu-id="fbfc6-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="fbfc6-122">PassThru</span></span>

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

### <span data-ttu-id="fbfc6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbfc6-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbfc6-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbfc6-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbfc6-125">-WorkspaceName</span></span>
<span data-ttu-id="fbfc6-126">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbfc6-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fbfc6-127">-Confirm</span></span>
<span data-ttu-id="fbfc6-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbfc6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbfc6-129">-WhatIf</span></span>
<span data-ttu-id="fbfc6-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbfc6-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbfc6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfc6-132">CommonParameters</span></span>
<span data-ttu-id="fbfc6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbfc6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfc6-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbfc6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfc6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbfc6-135">INPUTS</span></span>

### <span data-ttu-id="fbfc6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fbfc6-136">System.String</span></span>
### <span data-ttu-id="fbfc6-137">Microsoft. Azure. commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fbfc6-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="fbfc6-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbfc6-138">OUTPUTS</span></span>

### <span data-ttu-id="fbfc6-139">Microsoft. Azure. commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fbfc6-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="fbfc6-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbfc6-140">NOTES</span></span>

## <span data-ttu-id="fbfc6-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbfc6-141">RELATED LINKS</span></span>
