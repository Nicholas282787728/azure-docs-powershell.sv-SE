---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273131"
---
# <span data-ttu-id="1d431-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1d431-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="1d431-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d431-102">SYNOPSIS</span></span>
<span data-ttu-id="1d431-103">Tar bort en regel för loggnings varningar</span><span class="sxs-lookup"><span data-stu-id="1d431-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="1d431-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d431-104">SYNTAX</span></span>

### <span data-ttu-id="1d431-105">ByRuleName (standard)</span><span class="sxs-lookup"><span data-stu-id="1d431-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d431-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d431-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d431-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d431-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d431-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d431-108">DESCRIPTION</span></span>
<span data-ttu-id="1d431-109">Tar bort en regel för loggnings varningar</span><span class="sxs-lookup"><span data-stu-id="1d431-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="1d431-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d431-110">EXAMPLES</span></span>

### <span data-ttu-id="1d431-111">Exempel 1: ta bort efter regel namn</span><span class="sxs-lookup"><span data-stu-id="1d431-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="1d431-112">Exempel 2: ta bort med indatavärdet</span><span class="sxs-lookup"><span data-stu-id="1d431-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="1d431-113">Exempel 3: ta bort efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="1d431-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="1d431-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d431-114">PARAMETERS</span></span>

### <span data-ttu-id="1d431-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d431-115">-DefaultProfile</span></span>
<span data-ttu-id="1d431-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d431-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d431-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d431-117">-InputObject</span></span>
<span data-ttu-id="1d431-118">Resursen för regel för schemaläggning</span><span class="sxs-lookup"><span data-stu-id="1d431-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d431-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d431-119">-Name</span></span>
<span data-ttu-id="1d431-120">Aviseringens namn</span><span class="sxs-lookup"><span data-stu-id="1d431-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d431-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d431-121">-PassThru</span></span>
<span data-ttu-id="1d431-122">Returnera ett värde som anger om det lyckades eller inte.</span><span class="sxs-lookup"><span data-stu-id="1d431-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="1d431-123">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1d431-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1d431-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d431-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d431-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="1d431-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d431-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d431-126">-ResourceId</span></span>
<span data-ttu-id="1d431-127">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="1d431-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d431-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d431-128">-Confirm</span></span>
<span data-ttu-id="1d431-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d431-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d431-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d431-130">-WhatIf</span></span>
<span data-ttu-id="1d431-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d431-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d431-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d431-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d431-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d431-133">CommonParameters</span></span>
<span data-ttu-id="1d431-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d431-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d431-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d431-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d431-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d431-136">INPUTS</span></span>

### <span data-ttu-id="1d431-137">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="1d431-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="1d431-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1d431-138">System.String</span></span>

## <span data-ttu-id="1d431-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d431-139">OUTPUTS</span></span>

### <span data-ttu-id="1d431-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d431-140">System.Boolean</span></span>

## <span data-ttu-id="1d431-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d431-141">NOTES</span></span>

## <span data-ttu-id="1d431-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d431-142">RELATED LINKS</span></span>
