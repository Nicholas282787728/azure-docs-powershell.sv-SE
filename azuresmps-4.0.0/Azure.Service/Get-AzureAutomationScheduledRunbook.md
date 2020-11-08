---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099587"
---
# <span data-ttu-id="19388-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="19388-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="19388-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19388-102">SYNOPSIS</span></span>

<span data-ttu-id="19388-103">Får Azure Automation-runbooks och associerade scheman.</span><span class="sxs-lookup"><span data-stu-id="19388-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="19388-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19388-104">SYNTAX</span></span>

### <span data-ttu-id="19388-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="19388-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="19388-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="19388-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19388-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="19388-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19388-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="19388-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19388-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="19388-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="19388-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19388-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="19388-111">**Get-AzureAutomationScheduledRunbook** får en eller flera Azure Automation-runbooks och tillhör ande scheman.</span><span class="sxs-lookup"><span data-stu-id="19388-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="19388-112">Som standard returneras alla schemalagda Runbooks.</span><span class="sxs-lookup"><span data-stu-id="19388-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="19388-113">Om du vill hämta en specifik schemalagd Runbook anger du Runbook-namnet och schema namnet.</span><span class="sxs-lookup"><span data-stu-id="19388-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="19388-114">Om du vill hämta alla scheman som är kopplade till en Runbook anger du bara Runbook-namnet.</span><span class="sxs-lookup"><span data-stu-id="19388-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="19388-115">Om du vill att alla Runbooks ska vara kopplade till ett schema anger du bara schema namnet.</span><span class="sxs-lookup"><span data-stu-id="19388-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="19388-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19388-116">EXAMPLES</span></span>

### <span data-ttu-id="19388-117">Exempel 1: få alla schemalagda Runbooks</span><span class="sxs-lookup"><span data-stu-id="19388-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="19388-118">Det här kommandot får alla schemalagda Runbooks i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="19388-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="19388-119">Exempel 2: Hämta alla scheman som är kopplade till en Runbook</span><span class="sxs-lookup"><span data-stu-id="19388-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="19388-120">Med det här kommandot hämtas alla schemalagda Runbooks för Runbook-Runbk01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="19388-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="19388-121">Exempel 3: Hämta alla Runbooks som är kopplade till ett schema</span><span class="sxs-lookup"><span data-stu-id="19388-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="19388-122">Med det här kommandot hämtas alla schemalagda Runbooks för schemaläggning Schedule01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="19388-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="19388-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19388-123">PARAMETERS</span></span>

### <span data-ttu-id="19388-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19388-124">-AutomationAccountName</span></span>
<span data-ttu-id="19388-125">Anger namnet på ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="19388-125">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19388-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="19388-126">-JobScheduleId</span></span>
<span data-ttu-id="19388-127">Anger ID för ett schemalagt jobb.</span><span class="sxs-lookup"><span data-stu-id="19388-127">Specifies the ID of a scheduled job.</span></span>

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

### <span data-ttu-id="19388-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="19388-128">-Profile</span></span>
<span data-ttu-id="19388-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="19388-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19388-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="19388-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19388-131">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="19388-131">-RunbookName</span></span>
<span data-ttu-id="19388-132">Anger namnet på en Runbook.</span><span class="sxs-lookup"><span data-stu-id="19388-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19388-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="19388-133">-ScheduleName</span></span>
<span data-ttu-id="19388-134">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="19388-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19388-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19388-135">CommonParameters</span></span>
<span data-ttu-id="19388-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19388-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19388-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19388-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19388-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19388-138">INPUTS</span></span>

## <span data-ttu-id="19388-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19388-139">OUTPUTS</span></span>

### <span data-ttu-id="19388-140">Microsoft. Azure. commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="19388-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="19388-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19388-141">NOTES</span></span>

## <span data-ttu-id="19388-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19388-142">RELATED LINKS</span></span>

[<span data-ttu-id="19388-143">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="19388-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="19388-144">Avregistrera-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="19388-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


