---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: 94a35c3923debf5ea983e9d1ad276b124ae8c89c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578484"
---
# <span data-ttu-id="cde24-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cde24-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="cde24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cde24-102">SYNOPSIS</span></span>
<span data-ttu-id="cde24-103">Skapar ett jobb i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cde24-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cde24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cde24-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde24-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cde24-105">DESCRIPTION</span></span>
<span data-ttu-id="cde24-106">Cmdleten **New-AzureBatchJob** skapar ett jobb i Azure Batch-tjänsten på det konto som anges av parametern *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="cde24-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="cde24-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cde24-107">EXAMPLES</span></span>

### <span data-ttu-id="cde24-108">Exempel 1: skapa ett jobb</span><span class="sxs-lookup"><span data-stu-id="cde24-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="cde24-109">Det första kommandot skapar ett **PSPoolInformation** -objekt med hjälp av New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cde24-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="cde24-110">Kommandot lagrar objektet i $PoolInformation variabel.</span><span class="sxs-lookup"><span data-stu-id="cde24-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="cde24-111">Det andra kommandot tilldelar ID-Pool22 till egenskapen **PoolId** för objektet i $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="cde24-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="cde24-112">Med kommandot slut skapas ett jobb med ID-ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="cde24-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="cde24-113">Aktiviteter som lagts till i jobbet körs på poolen med ID-Pool22.</span><span class="sxs-lookup"><span data-stu-id="cde24-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="cde24-114">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="cde24-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cde24-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cde24-115">PARAMETERS</span></span>

### <span data-ttu-id="cde24-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cde24-116">-BatchContext</span></span>
<span data-ttu-id="cde24-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cde24-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cde24-118">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cde24-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-119">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="cde24-119">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="cde24-120">Anger de vanligaste miljövariablerna, som nycklar/värde par, som denna cmdlet ställer in för alla aktiviteter i jobbet.</span><span class="sxs-lookup"><span data-stu-id="cde24-120">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="cde24-121">Knappen är Miljövariabelns namn.</span><span class="sxs-lookup"><span data-stu-id="cde24-121">The key is the environment variable name.</span></span>
<span data-ttu-id="cde24-122">Värdet är Miljövariabelns värde.</span><span class="sxs-lookup"><span data-stu-id="cde24-122">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-123">-Begränsningar</span><span class="sxs-lookup"><span data-stu-id="cde24-123">-Constraints</span></span>
<span data-ttu-id="cde24-124">Anger körnings begränsningarna för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cde24-124">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cde24-125">-DisplayName</span></span>
<span data-ttu-id="cde24-126">Anger visnings namnet för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cde24-126">Specifies the display name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-127">-ID</span><span class="sxs-lookup"><span data-stu-id="cde24-127">-Id</span></span>
<span data-ttu-id="cde24-128">Anger ett ID för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cde24-128">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="cde24-129">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="cde24-129">-JobManagerTask</span></span>
<span data-ttu-id="cde24-130">Anger jobb chefs uppgiften.</span><span class="sxs-lookup"><span data-stu-id="cde24-130">Specifies the Job Manager task.</span></span>
<span data-ttu-id="cde24-131">Kommando tjänsten Kör jobb chefs aktiviteten när jobbet startas.</span><span class="sxs-lookup"><span data-stu-id="cde24-131">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-132">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="cde24-132">-JobPreparationTask</span></span>
<span data-ttu-id="cde24-133">Anger jobb förberedelse uppgiften.</span><span class="sxs-lookup"><span data-stu-id="cde24-133">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="cde24-134">Batch-tjänsten kör uppgiften för jobb Preparation på en datornod innan den påbörjar aktiviteter för det jobbet på den noden.</span><span class="sxs-lookup"><span data-stu-id="cde24-134">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-135">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="cde24-135">-JobReleaseTask</span></span>
<span data-ttu-id="cde24-136">Anger uppgiften för jobb släpp.</span><span class="sxs-lookup"><span data-stu-id="cde24-136">Specifies the Job Release task.</span></span>
<span data-ttu-id="cde24-137">Kommando tjänsten kör jobbet för jobb släpp när jobbet slutar.</span><span class="sxs-lookup"><span data-stu-id="cde24-137">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="cde24-138">Kommando tjänsten kör jobbet för jobb släppning på varje datornod där aktiviteten kördes.</span><span class="sxs-lookup"><span data-stu-id="cde24-138">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-139">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cde24-139">-Metadata</span></span>
<span data-ttu-id="cde24-140">Anger metadata, som nycklar/värde par, som ska läggas till i jobbet.</span><span class="sxs-lookup"><span data-stu-id="cde24-140">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="cde24-141">Det här är namnet på metadata.</span><span class="sxs-lookup"><span data-stu-id="cde24-141">The key is the metadata name.</span></span>
<span data-ttu-id="cde24-142">Värdet är metadata.</span><span class="sxs-lookup"><span data-stu-id="cde24-142">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-143">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="cde24-143">-OnAllTasksComplete</span></span>
<span data-ttu-id="cde24-144">Anger en åtgärd som ska utföras av kommando tjänsten om alla aktiviteter i jobbet är slutförda.</span><span class="sxs-lookup"><span data-stu-id="cde24-144">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-145">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="cde24-145">-OnTaskFailure</span></span>
<span data-ttu-id="cde24-146">Anger en åtgärd som kommando tjänsten tar om en aktivitet i jobbet Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="cde24-146">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-147">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="cde24-147">-PoolInformation</span></span>
<span data-ttu-id="cde24-148">Anger information om den pool där kommando tjänsten kör jobbets aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="cde24-148">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-149">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="cde24-149">-Priority</span></span>
<span data-ttu-id="cde24-150">Anger prioriteten för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cde24-150">Specifies the priority of the job.</span></span>
<span data-ttu-id="cde24-151">Giltiga värden är: heltal från-1000 till 1000.</span><span class="sxs-lookup"><span data-stu-id="cde24-151">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="cde24-152">Värdet-1000 är lägst prioritet.</span><span class="sxs-lookup"><span data-stu-id="cde24-152">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="cde24-153">Värdet 1000 är den högsta prioriteten.</span><span class="sxs-lookup"><span data-stu-id="cde24-153">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="cde24-154">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="cde24-154">The default value is 0.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde24-155">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="cde24-155">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="cde24-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde24-156">-DefaultProfile</span></span>
<span data-ttu-id="cde24-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cde24-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cde24-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde24-158">CommonParameters</span></span>
<span data-ttu-id="cde24-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde24-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde24-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde24-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde24-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cde24-161">INPUTS</span></span>

### <span data-ttu-id="cde24-162">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cde24-162">BatchAccountContext</span></span>
<span data-ttu-id="cde24-163">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="cde24-163">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="cde24-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cde24-164">OUTPUTS</span></span>

## <span data-ttu-id="cde24-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cde24-165">NOTES</span></span>

## <span data-ttu-id="cde24-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cde24-166">RELATED LINKS</span></span>

[<span data-ttu-id="cde24-167">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cde24-167">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="cde24-168">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cde24-168">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="cde24-169">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cde24-169">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cde24-170">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cde24-170">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="cde24-171">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cde24-171">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="cde24-172">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cde24-172">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="cde24-173">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="cde24-173">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="cde24-174">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="cde24-174">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


