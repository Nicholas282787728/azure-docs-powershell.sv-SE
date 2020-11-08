---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: f997c1574a81badf9d97bb4afecc104990aa725b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103296"
---
# <span data-ttu-id="d7c1f-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d7c1f-101">New-AzBatchJob</span></span>

## <span data-ttu-id="d7c1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c1f-103">Skapar ett jobb i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="d7c1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7c1f-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7c1f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c1f-106">Cmdleten **New-AzBatchJob** skapar ett jobb i Azure Batch-tjänsten på det konto som anges av parametern *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="d7c1f-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="d7c1f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c1f-108">Exempel 1: skapa ett jobb</span><span class="sxs-lookup"><span data-stu-id="d7c1f-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $PoolInformation.PoolId = "Pool22"
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="d7c1f-109">Det första kommandot skapar ett **PSPoolInformation** -objekt med hjälp av New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="d7c1f-110">Kommandot lagrar objektet i $PoolInformation variabel.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="d7c1f-111">Det andra kommandot tilldelar ID-Pool22 till egenskapen **PoolId** för objektet i $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="d7c1f-112">Med kommandot slut skapas ett jobb med ID-ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="d7c1f-113">Aktiviteter som lagts till i jobbet körs på poolen med ID-Pool22.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="d7c1f-114">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d7c1f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7c1f-115">PARAMETERS</span></span>

### <span data-ttu-id="d7c1f-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d7c1f-116">-BatchContext</span></span>
<span data-ttu-id="d7c1f-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d7c1f-118">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d7c1f-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d7c1f-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d7c1f-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d7c1f-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="d7c1f-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="d7c1f-123">Anger de vanligaste miljövariablerna, som nycklar/värde par, som denna cmdlet ställer in för alla aktiviteter i jobbet.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="d7c1f-124">Knappen är Miljövariabelns namn.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-124">The key is the environment variable name.</span></span>
<span data-ttu-id="d7c1f-125">Värdet är Miljövariabelns värde.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c1f-126">-Begränsningar</span><span class="sxs-lookup"><span data-stu-id="d7c1f-126">-Constraints</span></span>
<span data-ttu-id="d7c1f-127">Anger körnings begränsningarna för jobbet.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="d7c1f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c1f-128">-DefaultProfile</span></span>
<span data-ttu-id="d7c1f-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7c1f-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d7c1f-130">-DisplayName</span></span>
<span data-ttu-id="d7c1f-131">Anger visnings namnet för jobbet.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="d7c1f-132">-ID</span><span class="sxs-lookup"><span data-stu-id="d7c1f-132">-Id</span></span>
<span data-ttu-id="d7c1f-133">Anger ett ID för jobbet.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="d7c1f-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="d7c1f-134">-JobManagerTask</span></span>
<span data-ttu-id="d7c1f-135">Anger jobb chefs uppgiften.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="d7c1f-136">Kommando tjänsten Kör jobb chefs aktiviteten när jobbet startas.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="d7c1f-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="d7c1f-137">-JobPreparationTask</span></span>
<span data-ttu-id="d7c1f-138">Anger jobb förberedelse uppgiften.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="d7c1f-139">Batch-tjänsten kör uppgiften för jobb Preparation på en datornod innan den påbörjar aktiviteter för det jobbet på den noden.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="d7c1f-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="d7c1f-140">-JobReleaseTask</span></span>
<span data-ttu-id="d7c1f-141">Anger uppgiften för jobb släpp.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="d7c1f-142">Kommando tjänsten kör jobbet för jobb släpp när jobbet slutar.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="d7c1f-143">Kommando tjänsten kör jobbet för jobb släppning på varje datornod där aktiviteten kördes.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="d7c1f-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d7c1f-144">-Metadata</span></span>
<span data-ttu-id="d7c1f-145">Anger metadata, som nycklar/värde par, som ska läggas till i jobbet.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="d7c1f-146">Det här är namnet på metadata.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-146">The key is the metadata name.</span></span>
<span data-ttu-id="d7c1f-147">Värdet är metadata.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="d7c1f-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="d7c1f-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="d7c1f-149">Anger en åtgärd som ska utföras av kommando tjänsten om alla aktiviteter i jobbet är slutförda.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="d7c1f-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="d7c1f-150">-OnTaskFailure</span></span>
<span data-ttu-id="d7c1f-151">Anger en åtgärd som kommando tjänsten tar om en aktivitet i jobbet Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="d7c1f-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="d7c1f-152">-PoolInformation</span></span>
<span data-ttu-id="d7c1f-153">Anger information om den pool där kommando tjänsten kör jobbets aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="d7c1f-154">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="d7c1f-154">-Priority</span></span>
<span data-ttu-id="d7c1f-155">Anger prioriteten för jobbet.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="d7c1f-156">Giltiga värden är: heltal från-1000 till 1000.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="d7c1f-157">Värdet-1000 är lägst prioritet.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="d7c1f-158">Värdet 1000 är den högsta prioriteten.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="d7c1f-159">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-159">The default value is 0.</span></span>

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

### <span data-ttu-id="d7c1f-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="d7c1f-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="d7c1f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c1f-161">CommonParameters</span></span>
<span data-ttu-id="d7c1f-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7c1f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c1f-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7c1f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c1f-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7c1f-164">INPUTS</span></span>

### <span data-ttu-id="d7c1f-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d7c1f-165">System.String</span></span>

### <span data-ttu-id="d7c1f-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d7c1f-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d7c1f-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7c1f-167">OUTPUTS</span></span>

### <span data-ttu-id="d7c1f-168">System. Void</span><span class="sxs-lookup"><span data-stu-id="d7c1f-168">System.Void</span></span>

## <span data-ttu-id="d7c1f-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7c1f-169">NOTES</span></span>

## <span data-ttu-id="d7c1f-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7c1f-170">RELATED LINKS</span></span>

[<span data-ttu-id="d7c1f-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d7c1f-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="d7c1f-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d7c1f-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="d7c1f-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d7c1f-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d7c1f-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d7c1f-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="d7c1f-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d7c1f-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="d7c1f-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d7c1f-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="d7c1f-177">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d7c1f-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="d7c1f-178">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d7c1f-178">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
