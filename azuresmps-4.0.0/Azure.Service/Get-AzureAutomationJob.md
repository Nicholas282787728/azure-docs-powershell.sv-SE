---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099599"
---
# <span data-ttu-id="f3ac6-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f3ac6-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="f3ac6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3ac6-102">SYNOPSIS</span></span>

<span data-ttu-id="f3ac6-103">Får ett eller flera Azure Automation Runbook-jobb.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="f3ac6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3ac6-104">SYNTAX</span></span>

### <span data-ttu-id="f3ac6-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="f3ac6-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f3ac6-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="f3ac6-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ac6-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="f3ac6-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3ac6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3ac6-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f3ac6-109">Cmdleten **Get-AzureAutomationJob** får ett eller flera Runbook-jobb i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="f3ac6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3ac6-110">EXAMPLES</span></span>

### <span data-ttu-id="f3ac6-111">Exempel 1: Hämta ett specifikt Runbook-jobb</span><span class="sxs-lookup"><span data-stu-id="f3ac6-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="f3ac6-112">Det här kommandot får jobbet med angiven GUID.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="f3ac6-113">Exempel 2: Hämta alla jobb för en Runbook</span><span class="sxs-lookup"><span data-stu-id="f3ac6-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="f3ac6-114">Med det här kommandot hämtas alla jobb som är kopplade till en Runbook som heter MyRunbook.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="f3ac6-115">Exempel 2: Hämta alla jobb som körs</span><span class="sxs-lookup"><span data-stu-id="f3ac6-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="f3ac6-116">Det här kommandot hämtar alla jobb som körs i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="f3ac6-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3ac6-117">PARAMETERS</span></span>

### <span data-ttu-id="f3ac6-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3ac6-118">-AutomationAccountName</span></span>
<span data-ttu-id="f3ac6-119">Anger namnet på ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-119">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="f3ac6-120">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="f3ac6-120">-EndTime</span></span>
<span data-ttu-id="f3ac6-121">Anger slut tiden för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-121">Specifies the end time for a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ac6-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f3ac6-122">-Id</span></span>
<span data-ttu-id="f3ac6-123">Anger ID för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-123">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ac6-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="f3ac6-124">-Profile</span></span>
<span data-ttu-id="f3ac6-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3ac6-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3ac6-127">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="f3ac6-127">-RunbookName</span></span>
<span data-ttu-id="f3ac6-128">Anger namnet på en Runbook.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-128">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ac6-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f3ac6-129">-StartTime</span></span>
<span data-ttu-id="f3ac6-130">Anger start tiden för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-130">Specifies the start time of a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ac6-131">-Status</span><span class="sxs-lookup"><span data-stu-id="f3ac6-131">-Status</span></span>
<span data-ttu-id="f3ac6-132">Anger statusen för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-132">Specifies the status of a job.</span></span>
<span data-ttu-id="f3ac6-133">Denna cmdlet får jobb som har en status som matchar den här parametern.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="f3ac6-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="f3ac6-134">Valid values are:</span></span> 

- <span data-ttu-id="f3ac6-135">Rätta</span><span class="sxs-lookup"><span data-stu-id="f3ac6-135">Completed</span></span>
- <span data-ttu-id="f3ac6-136">Startade</span><span class="sxs-lookup"><span data-stu-id="f3ac6-136">Failed</span></span>
- <span data-ttu-id="f3ac6-137">I kö</span><span class="sxs-lookup"><span data-stu-id="f3ac6-137">Queued</span></span>
- <span data-ttu-id="f3ac6-138">Sidnumrering</span><span class="sxs-lookup"><span data-stu-id="f3ac6-138">Starting</span></span>
- <span data-ttu-id="f3ac6-139">Återupptas</span><span class="sxs-lookup"><span data-stu-id="f3ac6-139">Resuming</span></span>
- <span data-ttu-id="f3ac6-140">Aktiv</span><span class="sxs-lookup"><span data-stu-id="f3ac6-140">Running</span></span>
- <span data-ttu-id="f3ac6-141">Igång</span><span class="sxs-lookup"><span data-stu-id="f3ac6-141">Stopped</span></span>
- <span data-ttu-id="f3ac6-142">Stänger</span><span class="sxs-lookup"><span data-stu-id="f3ac6-142">Stopping</span></span>
- <span data-ttu-id="f3ac6-143">Hängande</span><span class="sxs-lookup"><span data-stu-id="f3ac6-143">Suspended</span></span>
- <span data-ttu-id="f3ac6-144">Pausa</span><span class="sxs-lookup"><span data-stu-id="f3ac6-144">Suspending</span></span>
- <span data-ttu-id="f3ac6-145">Aktivera</span><span class="sxs-lookup"><span data-stu-id="f3ac6-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ac6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ac6-146">CommonParameters</span></span>
<span data-ttu-id="f3ac6-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ac6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ac6-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ac6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ac6-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3ac6-149">INPUTS</span></span>

## <span data-ttu-id="f3ac6-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3ac6-150">OUTPUTS</span></span>

### <span data-ttu-id="f3ac6-151">Microsoft. Azure. commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="f3ac6-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="f3ac6-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3ac6-152">NOTES</span></span>

## <span data-ttu-id="f3ac6-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3ac6-153">RELATED LINKS</span></span>

[<span data-ttu-id="f3ac6-154">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f3ac6-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="f3ac6-155">Stopp-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f3ac6-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="f3ac6-156">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f3ac6-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


