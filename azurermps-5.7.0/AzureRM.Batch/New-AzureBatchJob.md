---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: bf96b5930895332de2e78ffdee71f9f6a2654b83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586116"
---
# <span data-ttu-id="fa2ce-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa2ce-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="fa2ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2ce-103">Skapar ett jobb i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa2ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa2ce-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa2ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="fa2ce-106">Cmdleten **New-AzureBatchJob** skapar ett jobb i Azure Batch-tjänsten på det konto som anges av parametern *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="fa2ce-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="fa2ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa2ce-107">EXAMPLES</span></span>

### <span data-ttu-id="fa2ce-108">Exempel 1: skapa ett jobb</span><span class="sxs-lookup"><span data-stu-id="fa2ce-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="fa2ce-109">Det första kommandot skapar ett **PSPoolInformation** -objekt med hjälp av New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="fa2ce-110">Kommandot lagrar objektet i $PoolInformation variabel.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="fa2ce-111">Det andra kommandot tilldelar ID-Pool22 till egenskapen **PoolId** för objektet i $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="fa2ce-112">Med kommandot slut skapas ett jobb med ID-ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="fa2ce-113">Aktiviteter som lagts till i jobbet körs på poolen med ID-Pool22.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="fa2ce-114">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="fa2ce-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa2ce-115">PARAMETERS</span></span>

### <span data-ttu-id="fa2ce-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fa2ce-116">-BatchContext</span></span>
<span data-ttu-id="fa2ce-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fa2ce-118">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fa2ce-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fa2ce-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fa2ce-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="fa2ce-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="fa2ce-123">Anger de vanligaste miljövariablerna, som nycklar/värde par, som denna cmdlet ställer in för alla aktiviteter i jobbet.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="fa2ce-124">Knappen är Miljövariabelns namn.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-124">The key is the environment variable name.</span></span>
<span data-ttu-id="fa2ce-125">Värdet är Miljövariabelns värde.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-125">The value is the environment variable value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-126">-Begränsningar</span><span class="sxs-lookup"><span data-stu-id="fa2ce-126">-Constraints</span></span>
<span data-ttu-id="fa2ce-127">Anger körnings begränsningarna för jobbet.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2ce-128">-DefaultProfile</span></span>
<span data-ttu-id="fa2ce-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa2ce-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fa2ce-130">-DisplayName</span></span>
<span data-ttu-id="fa2ce-131">Anger visnings namnet för jobbet.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-131">Specifies the display name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-132">-ID</span><span class="sxs-lookup"><span data-stu-id="fa2ce-132">-Id</span></span>
<span data-ttu-id="fa2ce-133">Anger ett ID för jobbet.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="fa2ce-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="fa2ce-134">-JobManagerTask</span></span>
<span data-ttu-id="fa2ce-135">Anger jobb chefs uppgiften.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="fa2ce-136">Kommando tjänsten Kör jobb chefs aktiviteten när jobbet startas.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="fa2ce-137">-JobPreparationTask</span></span>
<span data-ttu-id="fa2ce-138">Anger jobb förberedelse uppgiften.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="fa2ce-139">Batch-tjänsten kör uppgiften för jobb Preparation på en datornod innan den påbörjar aktiviteter för det jobbet på den noden.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="fa2ce-140">-JobReleaseTask</span></span>
<span data-ttu-id="fa2ce-141">Anger uppgiften för jobb släpp.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="fa2ce-142">Kommando tjänsten kör jobbet för jobb släpp när jobbet slutar.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="fa2ce-143">Kommando tjänsten kör jobbet för jobb släppning på varje datornod där aktiviteten kördes.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fa2ce-144">-Metadata</span></span>
<span data-ttu-id="fa2ce-145">Anger metadata, som nycklar/värde par, som ska läggas till i jobbet.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="fa2ce-146">Det här är namnet på metadata.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-146">The key is the metadata name.</span></span>
<span data-ttu-id="fa2ce-147">Värdet är metadata.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-147">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="fa2ce-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="fa2ce-149">Anger en åtgärd som ska utföras av kommando tjänsten om alla aktiviteter i jobbet är slutförda.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: OnAllTasksComplete
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="fa2ce-150">-OnTaskFailure</span></span>
<span data-ttu-id="fa2ce-151">Anger en åtgärd som kommando tjänsten tar om en aktivitet i jobbet Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: OnTaskFailure
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="fa2ce-152">-PoolInformation</span></span>
<span data-ttu-id="fa2ce-153">Anger information om den pool där kommando tjänsten kör jobbets aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-154">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="fa2ce-154">-Priority</span></span>
<span data-ttu-id="fa2ce-155">Anger prioriteten för jobbet.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="fa2ce-156">Giltiga värden är: heltal från-1000 till 1000.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="fa2ce-157">Värdet-1000 är lägst prioritet.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="fa2ce-158">Värdet 1000 är den högsta prioriteten.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="fa2ce-159">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-159">The default value is 0.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2ce-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="fa2ce-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="fa2ce-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2ce-161">CommonParameters</span></span>
<span data-ttu-id="fa2ce-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa2ce-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2ce-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa2ce-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2ce-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa2ce-164">INPUTS</span></span>

### <span data-ttu-id="fa2ce-165">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fa2ce-165">BatchAccountContext</span></span>
<span data-ttu-id="fa2ce-166">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fa2ce-166">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="fa2ce-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa2ce-167">OUTPUTS</span></span>

## <span data-ttu-id="fa2ce-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa2ce-168">NOTES</span></span>

## <span data-ttu-id="fa2ce-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa2ce-169">RELATED LINKS</span></span>

[<span data-ttu-id="fa2ce-170">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa2ce-170">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="fa2ce-171">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa2ce-171">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="fa2ce-172">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fa2ce-172">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fa2ce-173">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa2ce-173">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="fa2ce-174">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fa2ce-174">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="fa2ce-175">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa2ce-175">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="fa2ce-176">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa2ce-176">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="fa2ce-177">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="fa2ce-177">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

