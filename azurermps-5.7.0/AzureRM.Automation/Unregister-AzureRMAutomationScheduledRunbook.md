---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: a8e79dfcd505de6cb1a539f0b194f549835a95f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582116"
---
# <span data-ttu-id="c4572-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c4572-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="c4572-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4572-102">SYNOPSIS</span></span>
<span data-ttu-id="c4572-103">Tar bort en association mellan en Runbook och ett schema.</span><span class="sxs-lookup"><span data-stu-id="c4572-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4572-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4572-104">SYNTAX</span></span>

### <span data-ttu-id="c4572-105">ByJobScheduleId (standard)</span><span class="sxs-lookup"><span data-stu-id="c4572-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4572-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="c4572-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4572-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4572-107">DESCRIPTION</span></span>
<span data-ttu-id="c4572-108">**AzureRmAutomationScheduledRunbook cmdlet avregistrerar sig** kopplingen mellan en Azure Automation-Runbook och ett schema.</span><span class="sxs-lookup"><span data-stu-id="c4572-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="c4572-109">Schemat startar inte längre Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="c4572-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="c4572-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4572-110">EXAMPLES</span></span>

### <span data-ttu-id="c4572-111">Exempel 1: ta bort kopplingen mellan en Runbook och ett schema</span><span class="sxs-lookup"><span data-stu-id="c4572-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="c4572-112">Det här kommandot tar bort associationen mellan Runbook-flödet med namnet Runbk01 och schemat med namnet Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="c4572-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="c4572-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4572-113">PARAMETERS</span></span>

### <span data-ttu-id="c4572-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4572-114">-AutomationAccountName</span></span>
<span data-ttu-id="c4572-115">Anger ett Automation-konto för den Runbook som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="c4572-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4572-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4572-116">-DefaultProfile</span></span>
<span data-ttu-id="c4572-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c4572-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4572-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c4572-118">-Force</span></span>
<span data-ttu-id="c4572-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="c4572-119">ps_force</span></span>

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

### <span data-ttu-id="c4572-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="c4572-120">-JobScheduleId</span></span>
<span data-ttu-id="c4572-121">Anger ID för en schemalagd Runbook.</span><span class="sxs-lookup"><span data-stu-id="c4572-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4572-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4572-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4572-123">Anger namnet på en resurs grupp för den schemalagda Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="c4572-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4572-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c4572-124">-RunbookName</span></span>
<span data-ttu-id="c4572-125">Anger namnet på den Runbook som denna cmdlet kopplas från ett schema.</span><span class="sxs-lookup"><span data-stu-id="c4572-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4572-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="c4572-126">-ScheduleName</span></span>
<span data-ttu-id="c4572-127">Anger namnet på det schema som den här cmdleten kopplas från med en Runbook.</span><span class="sxs-lookup"><span data-stu-id="c4572-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4572-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4572-128">-Confirm</span></span>
<span data-ttu-id="c4572-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4572-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4572-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4572-130">-WhatIf</span></span>
<span data-ttu-id="c4572-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4572-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4572-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4572-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4572-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4572-133">CommonParameters</span></span>
<span data-ttu-id="c4572-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4572-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4572-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4572-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4572-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4572-136">INPUTS</span></span>

### <span data-ttu-id="c4572-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="c4572-137">None</span></span>
<span data-ttu-id="c4572-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c4572-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4572-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4572-139">OUTPUTS</span></span>

## <span data-ttu-id="c4572-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4572-140">NOTES</span></span>

## <span data-ttu-id="c4572-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4572-141">RELATED LINKS</span></span>

[<span data-ttu-id="c4572-142">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c4572-142">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="c4572-143">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c4572-143">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


