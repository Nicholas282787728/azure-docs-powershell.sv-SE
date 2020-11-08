---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099103"
---
# <span data-ttu-id="00faa-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="00faa-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="00faa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00faa-102">SYNOPSIS</span></span>

<span data-ttu-id="00faa-103">Associerar en Runbook med ett schema.</span><span class="sxs-lookup"><span data-stu-id="00faa-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="00faa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00faa-104">SYNTAX</span></span>

### <span data-ttu-id="00faa-105">ByRunbookName (standard)</span><span class="sxs-lookup"><span data-stu-id="00faa-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="00faa-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="00faa-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00faa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00faa-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="00faa-108">**Register-AzureAutomationScheduledRunbook** cmdlet associerar en Runbook med ett schema.</span><span class="sxs-lookup"><span data-stu-id="00faa-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="00faa-109">Runbook-flödet börjar utifrån det schema du anger med hjälp av parametern *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="00faa-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="00faa-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00faa-110">EXAMPLES</span></span>

### <span data-ttu-id="00faa-111">Exempel 1: associera en Runbook med ett schema</span><span class="sxs-lookup"><span data-stu-id="00faa-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="00faa-112">Det här kommandot associerar Runbook-flödet med namnet Runbk01 med schemat med namnet Sched01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00faa-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="00faa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00faa-113">PARAMETERS</span></span>

### <span data-ttu-id="00faa-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00faa-114">-AutomationAccountName</span></span>
<span data-ttu-id="00faa-115">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="00faa-115">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="00faa-116">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="00faa-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00faa-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="00faa-117">-Profile</span></span>
<span data-ttu-id="00faa-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="00faa-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00faa-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="00faa-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00faa-120">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="00faa-120">-RunbookName</span></span>
<span data-ttu-id="00faa-121">Anger namnet på Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="00faa-121">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="00faa-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="00faa-122">-ScheduleName</span></span>
<span data-ttu-id="00faa-123">Anger namnet på schemat.</span><span class="sxs-lookup"><span data-stu-id="00faa-123">Specifies the name of the schedule.</span></span>

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

### <span data-ttu-id="00faa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00faa-124">CommonParameters</span></span>
<span data-ttu-id="00faa-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00faa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00faa-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00faa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00faa-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00faa-127">INPUTS</span></span>

## <span data-ttu-id="00faa-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00faa-128">OUTPUTS</span></span>

### <span data-ttu-id="00faa-129">Microsoft. Azure. commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="00faa-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="00faa-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00faa-130">NOTES</span></span>

## <span data-ttu-id="00faa-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00faa-131">RELATED LINKS</span></span>

[<span data-ttu-id="00faa-132">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="00faa-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="00faa-133">Avregistrera-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="00faa-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


