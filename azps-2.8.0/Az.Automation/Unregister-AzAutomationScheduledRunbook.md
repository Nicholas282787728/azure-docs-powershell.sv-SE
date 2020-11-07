---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 203573856740e0e155e7dff0755ecad1b5399440
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745436"
---
# <span data-ttu-id="432ac-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="432ac-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="432ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="432ac-102">SYNOPSIS</span></span>
<span data-ttu-id="432ac-103">Tar bort en association mellan en Runbook och ett schema.</span><span class="sxs-lookup"><span data-stu-id="432ac-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="432ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="432ac-104">SYNTAX</span></span>

### <span data-ttu-id="432ac-105">ByJobScheduleId (standard)</span><span class="sxs-lookup"><span data-stu-id="432ac-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="432ac-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="432ac-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="432ac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="432ac-107">DESCRIPTION</span></span>
<span data-ttu-id="432ac-108">**AzAutomationScheduledRunbook cmdlet avregistrerar sig** kopplingen mellan en Azure Automation-Runbook och ett schema.</span><span class="sxs-lookup"><span data-stu-id="432ac-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="432ac-109">Schemat startar inte längre Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="432ac-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="432ac-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="432ac-110">EXAMPLES</span></span>

### <span data-ttu-id="432ac-111">Exempel 1: ta bort kopplingen mellan en Runbook och ett schema</span><span class="sxs-lookup"><span data-stu-id="432ac-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="432ac-112">Det här kommandot tar bort associationen mellan Runbook-flödet med namnet Runbk01 och schemat med namnet Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="432ac-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="432ac-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="432ac-113">PARAMETERS</span></span>

### <span data-ttu-id="432ac-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="432ac-114">-AutomationAccountName</span></span>
<span data-ttu-id="432ac-115">Anger ett Automation-konto för den Runbook som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="432ac-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="432ac-116">-DefaultProfile</span></span>
<span data-ttu-id="432ac-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="432ac-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="432ac-118">-Force</span><span class="sxs-lookup"><span data-stu-id="432ac-118">-Force</span></span>
<span data-ttu-id="432ac-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="432ac-119">ps_force</span></span>

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

### <span data-ttu-id="432ac-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="432ac-120">-JobScheduleId</span></span>
<span data-ttu-id="432ac-121">Anger ID för en schemalagd Runbook.</span><span class="sxs-lookup"><span data-stu-id="432ac-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432ac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="432ac-122">-ResourceGroupName</span></span>
<span data-ttu-id="432ac-123">Anger namnet på en resurs grupp för den schemalagda Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="432ac-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432ac-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="432ac-124">-RunbookName</span></span>
<span data-ttu-id="432ac-125">Anger namnet på den Runbook som denna cmdlet kopplas från ett schema.</span><span class="sxs-lookup"><span data-stu-id="432ac-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432ac-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="432ac-126">-ScheduleName</span></span>
<span data-ttu-id="432ac-127">Anger namnet på det schema som den här cmdleten kopplas från med en Runbook.</span><span class="sxs-lookup"><span data-stu-id="432ac-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="432ac-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="432ac-128">-Confirm</span></span>
<span data-ttu-id="432ac-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="432ac-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432ac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="432ac-130">-WhatIf</span></span>
<span data-ttu-id="432ac-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="432ac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="432ac-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="432ac-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="432ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="432ac-133">CommonParameters</span></span>
<span data-ttu-id="432ac-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="432ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="432ac-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="432ac-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="432ac-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="432ac-136">INPUTS</span></span>

### <span data-ttu-id="432ac-137">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="432ac-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="432ac-138">System. String</span><span class="sxs-lookup"><span data-stu-id="432ac-138">System.String</span></span>

## <span data-ttu-id="432ac-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="432ac-139">OUTPUTS</span></span>

### <span data-ttu-id="432ac-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="432ac-140">System.Void</span></span>

## <span data-ttu-id="432ac-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="432ac-141">NOTES</span></span>

## <span data-ttu-id="432ac-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="432ac-142">RELATED LINKS</span></span>

[<span data-ttu-id="432ac-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="432ac-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="432ac-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="432ac-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

