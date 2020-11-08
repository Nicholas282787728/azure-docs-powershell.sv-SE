---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 132726601b429819fa0d90186fd0d6448719df70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092672"
---
# <span data-ttu-id="f27a9-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="f27a9-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="f27a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f27a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f27a9-103">Associerar en Runbook till ett schema.</span><span class="sxs-lookup"><span data-stu-id="f27a9-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="f27a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f27a9-104">SYNTAX</span></span>

### <span data-ttu-id="f27a9-105">ByRunbookName (standard)</span><span class="sxs-lookup"><span data-stu-id="f27a9-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f27a9-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="f27a9-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f27a9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f27a9-107">DESCRIPTION</span></span>
<span data-ttu-id="f27a9-108">**Register-AzAutomationScheduledRunbook** cmdlet associerar en Azure Automation-Runbook till ett schema.</span><span class="sxs-lookup"><span data-stu-id="f27a9-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="f27a9-109">Runbook-flödet börjar utifrån det schema du anger med hjälp av parametern *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="f27a9-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="f27a9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f27a9-110">EXAMPLES</span></span>

### <span data-ttu-id="f27a9-111">Exempel 1: associera en Runbook med ett schema</span><span class="sxs-lookup"><span data-stu-id="f27a9-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f27a9-112">Det här kommandot associerar Runbook-flödet med namnet Runbk01 med schemat med namnet Sched01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f27a9-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f27a9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f27a9-113">PARAMETERS</span></span>

### <span data-ttu-id="f27a9-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f27a9-114">-AutomationAccountName</span></span>
<span data-ttu-id="f27a9-115">Anger ett Automation-konto för den Runbook som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="f27a9-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f27a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27a9-116">-DefaultProfile</span></span>
<span data-ttu-id="f27a9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f27a9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f27a9-118">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="f27a9-118">-Parameters</span></span>
<span data-ttu-id="f27a9-119">Anger en hash-tabell med nycklar/värde-par.</span><span class="sxs-lookup"><span data-stu-id="f27a9-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="f27a9-120">Nycklarna är parameter namn för Runbook.</span><span class="sxs-lookup"><span data-stu-id="f27a9-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="f27a9-121">Värdena är parameter värden för Runbook.</span><span class="sxs-lookup"><span data-stu-id="f27a9-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="f27a9-122">När Runbook startar som svar på det associerade schemat skickas dessa parametrar till Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="f27a9-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f27a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f27a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="f27a9-124">Anger namnet på en resurs grupp för den schemalagda Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="f27a9-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="f27a9-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="f27a9-125">-RunbookName</span></span>
<span data-ttu-id="f27a9-126">Anger namnet på den Runbook som denna cmdlet associerar till ett schema.</span><span class="sxs-lookup"><span data-stu-id="f27a9-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="f27a9-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="f27a9-127">-RunOn</span></span>
<span data-ttu-id="f27a9-128">Namnet på Hybrid Runbook Worker-gruppen.</span><span class="sxs-lookup"><span data-stu-id="f27a9-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f27a9-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="f27a9-129">-ScheduleName</span></span>
<span data-ttu-id="f27a9-130">Anger namnet på det schema som denna cmdlet ska kopplas till för en Runbook.</span><span class="sxs-lookup"><span data-stu-id="f27a9-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="f27a9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27a9-131">CommonParameters</span></span>
<span data-ttu-id="f27a9-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f27a9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27a9-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f27a9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27a9-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f27a9-134">INPUTS</span></span>

### <span data-ttu-id="f27a9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f27a9-135">System.String</span></span>

## <span data-ttu-id="f27a9-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f27a9-136">OUTPUTS</span></span>

### <span data-ttu-id="f27a9-137">Microsoft. Azure. commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="f27a9-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="f27a9-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f27a9-138">NOTES</span></span>

## <span data-ttu-id="f27a9-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f27a9-139">RELATED LINKS</span></span>

[<span data-ttu-id="f27a9-140">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="f27a9-140">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="f27a9-141">Avregistrera-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="f27a9-141">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


