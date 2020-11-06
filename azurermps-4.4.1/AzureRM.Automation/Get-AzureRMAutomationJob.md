---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 4509190a8417379c9d5bc9eae9d6d12609def4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586263"
---
# <span data-ttu-id="b79f9-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b79f9-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="b79f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b79f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b79f9-103">Hämtar automatiserings Runbook-jobb.</span><span class="sxs-lookup"><span data-stu-id="b79f9-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b79f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b79f9-104">SYNTAX</span></span>

### <span data-ttu-id="b79f9-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="b79f9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b79f9-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="b79f9-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b79f9-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="b79f9-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b79f9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b79f9-108">DESCRIPTION</span></span>
<span data-ttu-id="b79f9-109">Cmdleten **Get-AzureRmAutomationJob** får Runbook-jobb i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b79f9-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="b79f9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b79f9-110">EXAMPLES</span></span>

### <span data-ttu-id="b79f9-111">Exempel 1: Hämta ett specifikt Runbook-jobb</span><span class="sxs-lookup"><span data-stu-id="b79f9-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="b79f9-112">Det här kommandot får jobbet med angiven GUID.</span><span class="sxs-lookup"><span data-stu-id="b79f9-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="b79f9-113">Exempel 2: Hämta alla jobb för en Runbook</span><span class="sxs-lookup"><span data-stu-id="b79f9-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="b79f9-114">Med det här kommandot hämtas alla jobb som är kopplade till en Runbook som heter Runbook02.</span><span class="sxs-lookup"><span data-stu-id="b79f9-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="b79f9-115">Exempel 3: Hämta alla jobb som körs</span><span class="sxs-lookup"><span data-stu-id="b79f9-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="b79f9-116">Det här kommandot hämtar alla jobb som körs i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b79f9-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b79f9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b79f9-117">PARAMETERS</span></span>

### <span data-ttu-id="b79f9-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b79f9-118">-AutomationAccountName</span></span>
<span data-ttu-id="b79f9-119">Anger namnet på ett Automation-konto som den här cmdleten får jobb för.</span><span class="sxs-lookup"><span data-stu-id="b79f9-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="b79f9-120">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="b79f9-120">-EndTime</span></span>
<span data-ttu-id="b79f9-121">Anger slut tiden för ett jobb som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b79f9-121">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b79f9-122">Du kan ange en sträng som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="b79f9-122">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="b79f9-123">Denna cmdlet får jobb som har slut tid på eller före det värde som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b79f9-123">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="b79f9-124">-ID</span><span class="sxs-lookup"><span data-stu-id="b79f9-124">-Id</span></span>
<span data-ttu-id="b79f9-125">Anger ID för ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="b79f9-125">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b79f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b79f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="b79f9-127">Anger namnet på en resurs grupp där denna cmdlet hämtar jobb.</span><span class="sxs-lookup"><span data-stu-id="b79f9-127">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="b79f9-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="b79f9-128">-RunbookName</span></span>
<span data-ttu-id="b79f9-129">Anger namnet på en Runbook för vilken denna cmdlet hämtar jobb.</span><span class="sxs-lookup"><span data-stu-id="b79f9-129">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="b79f9-130">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b79f9-130">-StartTime</span></span>
<span data-ttu-id="b79f9-131">Anger start tiden för ett jobb som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b79f9-131">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b79f9-132">Denna cmdlet får jobb som har en start tid på eller efter det värde som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b79f9-132">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="b79f9-133">-Status</span><span class="sxs-lookup"><span data-stu-id="b79f9-133">-Status</span></span>
<span data-ttu-id="b79f9-134">Anger statusen för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="b79f9-134">Specifies the status of a job.</span></span>
<span data-ttu-id="b79f9-135">Denna cmdlet får jobb som har en status som matchar den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b79f9-135">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="b79f9-136">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="b79f9-136">Valid values are:</span></span> 

- <span data-ttu-id="b79f9-137">Aktivera</span><span class="sxs-lookup"><span data-stu-id="b79f9-137">Activating</span></span>
- <span data-ttu-id="b79f9-138">Rätta</span><span class="sxs-lookup"><span data-stu-id="b79f9-138">Completed</span></span>
- <span data-ttu-id="b79f9-139">Startade</span><span class="sxs-lookup"><span data-stu-id="b79f9-139">Failed</span></span>
- <span data-ttu-id="b79f9-140">I kö</span><span class="sxs-lookup"><span data-stu-id="b79f9-140">Queued</span></span>
- <span data-ttu-id="b79f9-141">Återupptas</span><span class="sxs-lookup"><span data-stu-id="b79f9-141">Resuming</span></span>
- <span data-ttu-id="b79f9-142">Aktiv</span><span class="sxs-lookup"><span data-stu-id="b79f9-142">Running</span></span>
- <span data-ttu-id="b79f9-143">Sidnumrering</span><span class="sxs-lookup"><span data-stu-id="b79f9-143">Starting</span></span>
- <span data-ttu-id="b79f9-144">Igång</span><span class="sxs-lookup"><span data-stu-id="b79f9-144">Stopped</span></span>
- <span data-ttu-id="b79f9-145">Stänger</span><span class="sxs-lookup"><span data-stu-id="b79f9-145">Stopping</span></span>
- <span data-ttu-id="b79f9-146">Hängande</span><span class="sxs-lookup"><span data-stu-id="b79f9-146">Suspended</span></span>
- <span data-ttu-id="b79f9-147">Pausa</span><span class="sxs-lookup"><span data-stu-id="b79f9-147">Suspending</span></span>

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

### <span data-ttu-id="b79f9-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79f9-148">-DefaultProfile</span></span>
<span data-ttu-id="b79f9-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b79f9-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b79f9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79f9-150">CommonParameters</span></span>
<span data-ttu-id="b79f9-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b79f9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79f9-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b79f9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79f9-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b79f9-153">INPUTS</span></span>

## <span data-ttu-id="b79f9-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b79f9-154">OUTPUTS</span></span>

### <span data-ttu-id="b79f9-155">Microsoft. Azure. commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="b79f9-155">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="b79f9-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b79f9-156">NOTES</span></span>

## <span data-ttu-id="b79f9-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b79f9-157">RELATED LINKS</span></span>

[<span data-ttu-id="b79f9-158">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b79f9-158">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="b79f9-159">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b79f9-159">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="b79f9-160">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b79f9-160">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="b79f9-161">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b79f9-161">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


