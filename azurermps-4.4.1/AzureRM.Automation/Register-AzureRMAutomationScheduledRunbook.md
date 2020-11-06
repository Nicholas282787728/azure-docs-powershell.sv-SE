---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: e58f3d429d036afa13f82e8e140ca8195eed612a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573737"
---
# <span data-ttu-id="78cb4-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="78cb4-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="78cb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="78cb4-103">Associerar en Runbook till ett schema.</span><span class="sxs-lookup"><span data-stu-id="78cb4-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78cb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78cb4-104">SYNTAX</span></span>

### <span data-ttu-id="78cb4-105">ByRunbookName (standard)</span><span class="sxs-lookup"><span data-stu-id="78cb4-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78cb4-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="78cb4-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78cb4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78cb4-107">DESCRIPTION</span></span>
<span data-ttu-id="78cb4-108">**Register-AzureRmAutomationScheduledRunbook** cmdlet associerar en Azure Automation-Runbook till ett schema.</span><span class="sxs-lookup"><span data-stu-id="78cb4-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="78cb4-109">Runbook-flödet börjar utifrån det schema du anger med hjälp av parametern *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="78cb4-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="78cb4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78cb4-110">EXAMPLES</span></span>

### <span data-ttu-id="78cb4-111">Exempel 1: associera en Runbook med ett schema</span><span class="sxs-lookup"><span data-stu-id="78cb4-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="78cb4-112">Det här kommandot associerar Runbook-flödet med namnet Runbk01 med schemat med namnet Sched01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="78cb4-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="78cb4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78cb4-113">PARAMETERS</span></span>

### <span data-ttu-id="78cb4-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78cb4-114">-AutomationAccountName</span></span>
<span data-ttu-id="78cb4-115">Anger ett Automation-konto för den Runbook som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="78cb4-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="78cb4-116">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="78cb4-116">-Parameters</span></span>
<span data-ttu-id="78cb4-117">Anger en hash-tabell med nycklar/värde-par.</span><span class="sxs-lookup"><span data-stu-id="78cb4-117">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="78cb4-118">Nycklarna är parameter namn för Runbook.</span><span class="sxs-lookup"><span data-stu-id="78cb4-118">The keys are runbook parameter names.</span></span>
<span data-ttu-id="78cb4-119">Värdena är parameter värden för Runbook.</span><span class="sxs-lookup"><span data-stu-id="78cb4-119">The values are runbook parameter values.</span></span>
<span data-ttu-id="78cb4-120">När Runbook startar som svar på det associerade schemat skickas dessa parametrar till Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="78cb4-120">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="78cb4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cb4-121">-ResourceGroupName</span></span>
<span data-ttu-id="78cb4-122">Anger namnet på en resurs grupp för den schemalagda Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="78cb4-122">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="78cb4-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="78cb4-123">-RunbookName</span></span>
<span data-ttu-id="78cb4-124">Anger namnet på den Runbook som denna cmdlet associerar till ett schema.</span><span class="sxs-lookup"><span data-stu-id="78cb4-124">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="78cb4-125">-RunOn</span><span class="sxs-lookup"><span data-stu-id="78cb4-125">-RunOn</span></span>
<span data-ttu-id="78cb4-126">Namnet på Hybrid Runbook Worker-gruppen.</span><span class="sxs-lookup"><span data-stu-id="78cb4-126">The name of the hybrid runbook worker group.</span></span>

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

### <span data-ttu-id="78cb4-127">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="78cb4-127">-ScheduleName</span></span>
<span data-ttu-id="78cb4-128">Anger namnet på det schema som denna cmdlet ska kopplas till för en Runbook.</span><span class="sxs-lookup"><span data-stu-id="78cb4-128">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="78cb4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78cb4-129">-DefaultProfile</span></span>
<span data-ttu-id="78cb4-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78cb4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78cb4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cb4-131">CommonParameters</span></span>
<span data-ttu-id="78cb4-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78cb4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78cb4-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78cb4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cb4-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78cb4-134">INPUTS</span></span>

## <span data-ttu-id="78cb4-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78cb4-135">OUTPUTS</span></span>

### <span data-ttu-id="78cb4-136">Microsoft. Azure. commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="78cb4-136">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="78cb4-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78cb4-137">NOTES</span></span>

## <span data-ttu-id="78cb4-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78cb4-138">RELATED LINKS</span></span>

[<span data-ttu-id="78cb4-139">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="78cb4-139">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="78cb4-140">Avregistrera-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="78cb4-140">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


