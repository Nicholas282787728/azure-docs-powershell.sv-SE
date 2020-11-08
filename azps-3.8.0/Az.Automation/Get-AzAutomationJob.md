---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090405"
---
# <span data-ttu-id="949e2-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="949e2-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="949e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="949e2-102">SYNOPSIS</span></span>
<span data-ttu-id="949e2-103">Hämtar automatiserings Runbook-jobb.</span><span class="sxs-lookup"><span data-stu-id="949e2-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="949e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="949e2-104">SYNTAX</span></span>

### <span data-ttu-id="949e2-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="949e2-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="949e2-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="949e2-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949e2-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="949e2-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="949e2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="949e2-108">DESCRIPTION</span></span>
<span data-ttu-id="949e2-109">Cmdleten **Get-AzAutomationJob** får Runbook-jobb i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="949e2-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="949e2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="949e2-110">EXAMPLES</span></span>

### <span data-ttu-id="949e2-111">Exempel 1: Hämta ett specifikt Runbook-jobb</span><span class="sxs-lookup"><span data-stu-id="949e2-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="949e2-112">Det här kommandot får jobbet med angiven GUID.</span><span class="sxs-lookup"><span data-stu-id="949e2-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="949e2-113">Exempel 2: Hämta alla jobb för en Runbook</span><span class="sxs-lookup"><span data-stu-id="949e2-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="949e2-114">Med det här kommandot hämtas alla jobb som är kopplade till en Runbook som heter Runbook02.</span><span class="sxs-lookup"><span data-stu-id="949e2-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="949e2-115">Exempel 3: Hämta alla jobb som körs</span><span class="sxs-lookup"><span data-stu-id="949e2-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="949e2-116">Det här kommandot hämtar alla jobb som körs i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="949e2-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="949e2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="949e2-117">PARAMETERS</span></span>

### <span data-ttu-id="949e2-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="949e2-118">-AutomationAccountName</span></span>
<span data-ttu-id="949e2-119">Anger namnet på ett Automation-konto som den här cmdleten får jobb för.</span><span class="sxs-lookup"><span data-stu-id="949e2-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="949e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="949e2-120">-DefaultProfile</span></span>
<span data-ttu-id="949e2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="949e2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="949e2-122">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="949e2-122">-EndTime</span></span>
<span data-ttu-id="949e2-123">Anger slut tiden för ett jobb som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="949e2-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="949e2-124">Du kan ange en sträng som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="949e2-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="949e2-125">Denna cmdlet får jobb som har slut tid på eller före det värde som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="949e2-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949e2-126">-ID</span><span class="sxs-lookup"><span data-stu-id="949e2-126">-Id</span></span>
<span data-ttu-id="949e2-127">Anger ID för ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="949e2-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="949e2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="949e2-128">-ResourceGroupName</span></span>
<span data-ttu-id="949e2-129">Anger namnet på en resurs grupp där denna cmdlet hämtar jobb.</span><span class="sxs-lookup"><span data-stu-id="949e2-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="949e2-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="949e2-130">-RunbookName</span></span>
<span data-ttu-id="949e2-131">Anger namnet på en Runbook för vilken denna cmdlet hämtar jobb.</span><span class="sxs-lookup"><span data-stu-id="949e2-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949e2-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="949e2-132">-StartTime</span></span>
<span data-ttu-id="949e2-133">Anger start tiden för ett jobb som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="949e2-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="949e2-134">Denna cmdlet får jobb som har en start tid på eller efter det värde som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="949e2-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949e2-135">-Status</span><span class="sxs-lookup"><span data-stu-id="949e2-135">-Status</span></span>
<span data-ttu-id="949e2-136">Anger statusen för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="949e2-136">Specifies the status of a job.</span></span>
<span data-ttu-id="949e2-137">Denna cmdlet får jobb som har en status som matchar den här parametern.</span><span class="sxs-lookup"><span data-stu-id="949e2-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="949e2-138">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="949e2-138">Valid values are:</span></span> 
- <span data-ttu-id="949e2-139">Aktivera</span><span class="sxs-lookup"><span data-stu-id="949e2-139">Activating</span></span>
- <span data-ttu-id="949e2-140">Rätta</span><span class="sxs-lookup"><span data-stu-id="949e2-140">Completed</span></span>
- <span data-ttu-id="949e2-141">Startade</span><span class="sxs-lookup"><span data-stu-id="949e2-141">Failed</span></span>
- <span data-ttu-id="949e2-142">I kö</span><span class="sxs-lookup"><span data-stu-id="949e2-142">Queued</span></span>
- <span data-ttu-id="949e2-143">Återupptas</span><span class="sxs-lookup"><span data-stu-id="949e2-143">Resuming</span></span>
- <span data-ttu-id="949e2-144">Aktiv</span><span class="sxs-lookup"><span data-stu-id="949e2-144">Running</span></span>
- <span data-ttu-id="949e2-145">Sidnumrering</span><span class="sxs-lookup"><span data-stu-id="949e2-145">Starting</span></span>
- <span data-ttu-id="949e2-146">Igång</span><span class="sxs-lookup"><span data-stu-id="949e2-146">Stopped</span></span>
- <span data-ttu-id="949e2-147">Stänger</span><span class="sxs-lookup"><span data-stu-id="949e2-147">Stopping</span></span>
- <span data-ttu-id="949e2-148">Hängande</span><span class="sxs-lookup"><span data-stu-id="949e2-148">Suspended</span></span>
- <span data-ttu-id="949e2-149">Pausa</span><span class="sxs-lookup"><span data-stu-id="949e2-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949e2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="949e2-150">CommonParameters</span></span>
<span data-ttu-id="949e2-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="949e2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="949e2-152">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="949e2-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="949e2-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="949e2-153">INPUTS</span></span>

### <span data-ttu-id="949e2-154">System. GUID</span><span class="sxs-lookup"><span data-stu-id="949e2-154">System.Guid</span></span>

### <span data-ttu-id="949e2-155">System. String</span><span class="sxs-lookup"><span data-stu-id="949e2-155">System.String</span></span>

## <span data-ttu-id="949e2-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="949e2-156">OUTPUTS</span></span>

### <span data-ttu-id="949e2-157">Microsoft. Azure. commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="949e2-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="949e2-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="949e2-158">NOTES</span></span>

## <span data-ttu-id="949e2-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="949e2-159">RELATED LINKS</span></span>

[<span data-ttu-id="949e2-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="949e2-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="949e2-161">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="949e2-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="949e2-162">Stopp-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="949e2-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="949e2-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="949e2-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


