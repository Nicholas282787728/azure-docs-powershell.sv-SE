---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578479"
---
# <span data-ttu-id="510b3-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="510b3-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="510b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="510b3-102">SYNOPSIS</span></span>
<span data-ttu-id="510b3-103">Skapar en batchuppgiften under ett jobb.</span><span class="sxs-lookup"><span data-stu-id="510b3-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="510b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="510b3-104">SYNTAX</span></span>

### <span data-ttu-id="510b3-105">JobId_Single (standard)</span><span class="sxs-lookup"><span data-stu-id="510b3-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="510b3-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="510b3-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="510b3-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="510b3-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="510b3-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="510b3-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="510b3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="510b3-109">DESCRIPTION</span></span>
<span data-ttu-id="510b3-110">Cmdleten **New-AzureBatchTask** skapar en Azure Batch-uppgift under det jobb som anges med parametern *jobId* eller *jobb* parameter.</span><span class="sxs-lookup"><span data-stu-id="510b3-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="510b3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="510b3-111">EXAMPLES</span></span>

### <span data-ttu-id="510b3-112">Exempel 1: skapa en batchuppgiften</span><span class="sxs-lookup"><span data-stu-id="510b3-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="510b3-113">Det här kommandot skapar en uppgift med ID-Task23 under jobbet som har ID-jobbet-000001.</span><span class="sxs-lookup"><span data-stu-id="510b3-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="510b3-114">Aktiviteten kör det angivna kommandot.</span><span class="sxs-lookup"><span data-stu-id="510b3-114">The task runs the specified command.</span></span>
<span data-ttu-id="510b3-115">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="510b3-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="510b3-116">Exempel 2: skapa en batchuppgiften</span><span class="sxs-lookup"><span data-stu-id="510b3-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="510b3-117">Det här kommandot får batch-jobbet med ID-000001 genom att använda cmdleten **Get-AzureBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="510b3-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="510b3-118">Kommandot skickar jobbet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="510b3-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="510b3-119">Kommandot skapar en uppgift med ID-Task26 under det jobbet.</span><span class="sxs-lookup"><span data-stu-id="510b3-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="510b3-120">Aktiviteten kör det angivna kommandot med förhöjda behörigheter.</span><span class="sxs-lookup"><span data-stu-id="510b3-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="510b3-121">Exempel 3: lägga till en mängd uppgifter till det angivna jobbet genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="510b3-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="510b3-122">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="510b3-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="510b3-123">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="510b3-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="510b3-124">De två kommandona skapar **PSCloudTask** -objekt med hjälp av New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="510b3-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="510b3-125">I kommandona lagras aktiviteterna i $Task 01-och $Task 02-variabler.</span><span class="sxs-lookup"><span data-stu-id="510b3-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="510b3-126">Det sista kommandot får batch-jobbet med ID-000001 genom att använda **Get-AzureBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="510b3-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="510b3-127">Då överförs det jobbet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="510b3-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="510b3-128">Kommandot lägger till en mängd uppgifter under det jobbet.</span><span class="sxs-lookup"><span data-stu-id="510b3-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="510b3-129">Kommandot använder kontexten som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="510b3-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="510b3-130">Exempel 4: lägga till en mängd uppgifter i det angivna jobbet</span><span class="sxs-lookup"><span data-stu-id="510b3-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="510b3-131">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="510b3-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="510b3-132">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="510b3-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="510b3-133">De två kommandona skapar **PSCloudTask** -objekt med hjälp av New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="510b3-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="510b3-134">I kommandona lagras aktiviteterna i $Task 01-och $Task 02-variabler.</span><span class="sxs-lookup"><span data-stu-id="510b3-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="510b3-135">Med kommandot slut läggs aktiviteterna i $Task 01 och $Task 02 till det jobb som har ID-000001.</span><span class="sxs-lookup"><span data-stu-id="510b3-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="510b3-136">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="510b3-136">PARAMETERS</span></span>

### <span data-ttu-id="510b3-137">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="510b3-137">-AffinityInformation</span></span>
<span data-ttu-id="510b3-138">Anger ett lokal tips som används i kommando tjänsten för att välja en nod för att köra uppgiften.</span><span class="sxs-lookup"><span data-stu-id="510b3-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-139">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="510b3-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="510b3-140">-BatchContext</span></span>
<span data-ttu-id="510b3-141">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="510b3-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="510b3-142">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="510b3-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="510b3-143">-Kommandorad</span><span class="sxs-lookup"><span data-stu-id="510b3-143">-CommandLine</span></span>
<span data-ttu-id="510b3-144">Anger kommando raden för uppgiften.</span><span class="sxs-lookup"><span data-stu-id="510b3-144">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-145">-Begränsningar</span><span class="sxs-lookup"><span data-stu-id="510b3-145">-Constraints</span></span>
<span data-ttu-id="510b3-146">Anger de körnings begränsningar som gäller för den här uppgiften.</span><span class="sxs-lookup"><span data-stu-id="510b3-146">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-147">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="510b3-147">-DependsOn</span></span>
<span data-ttu-id="510b3-148">Anger att aktiviteten är beroende av andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="510b3-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="510b3-149">Aktiviteten schemaläggs inte förrän alla förväntade uppgifter har genomförts.</span><span class="sxs-lookup"><span data-stu-id="510b3-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="510b3-150">-DisplayName</span></span>
<span data-ttu-id="510b3-151">Anger uppgiftens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="510b3-151">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="510b3-152">-EnvironmentSettings</span></span>
<span data-ttu-id="510b3-153">Anger miljö inställningar, som nycklar/värde par, som denna cmdlet lägger till i uppgiften.</span><span class="sxs-lookup"><span data-stu-id="510b3-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="510b3-154">Det här är namnet på miljö inställningen.</span><span class="sxs-lookup"><span data-stu-id="510b3-154">The key is the environment setting name.</span></span>
<span data-ttu-id="510b3-155">Värdet är miljö inställningen.</span><span class="sxs-lookup"><span data-stu-id="510b3-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="510b3-156">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-157">-ID</span><span class="sxs-lookup"><span data-stu-id="510b3-157">-Id</span></span>
<span data-ttu-id="510b3-158">Anger aktivitetens ID.</span><span class="sxs-lookup"><span data-stu-id="510b3-158">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-159">-Jobb</span><span class="sxs-lookup"><span data-stu-id="510b3-159">-Job</span></span>
<span data-ttu-id="510b3-160">Anger det jobb under vilket denna cmdlet skapar uppgiften.</span><span class="sxs-lookup"><span data-stu-id="510b3-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="510b3-161">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="510b3-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="510b3-162">-JobId</span></span>
<span data-ttu-id="510b3-163">Anger ID för det jobb som den här cmdleten skapar för aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="510b3-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-164">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="510b3-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="510b3-165">Anger information om hur du kör en aktivitet med flera instanser.</span><span class="sxs-lookup"><span data-stu-id="510b3-165">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="510b3-166">-ResourceFiles</span></span>
<span data-ttu-id="510b3-167">Anger resursfiler, som nycklar/värde par, som aktiviteten kräver.</span><span class="sxs-lookup"><span data-stu-id="510b3-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="510b3-168">Nyckelns fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="510b3-168">The key is the resource file path.</span></span>
<span data-ttu-id="510b3-169">Värdet är resurs filens BLOB-källa.</span><span class="sxs-lookup"><span data-stu-id="510b3-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-170">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="510b3-170">-RunElevated</span></span>
<span data-ttu-id="510b3-171">Visar att aktivitets processen körs med administratörs behörigheter.</span><span class="sxs-lookup"><span data-stu-id="510b3-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-172">-Uppgifter</span><span class="sxs-lookup"><span data-stu-id="510b3-172">-Tasks</span></span>
<span data-ttu-id="510b3-173">Anger mängden med uppgifter som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="510b3-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="510b3-174">Varje uppgift måste ha ett unikt ID.</span><span class="sxs-lookup"><span data-stu-id="510b3-174">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="510b3-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510b3-175">-DefaultProfile</span></span>
<span data-ttu-id="510b3-176">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="510b3-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="510b3-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510b3-177">CommonParameters</span></span>
<span data-ttu-id="510b3-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="510b3-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510b3-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="510b3-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510b3-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="510b3-180">INPUTS</span></span>

### <span data-ttu-id="510b3-181">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="510b3-181">BatchAccountContext</span></span>
<span data-ttu-id="510b3-182">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="510b3-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="510b3-183">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="510b3-183">PSCloudJob</span></span>
<span data-ttu-id="510b3-184">Parametern ' Job ' godkänner värdet av typen ' PSCloudJob ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="510b3-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="510b3-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="510b3-185">OUTPUTS</span></span>

## <span data-ttu-id="510b3-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="510b3-186">NOTES</span></span>

## <span data-ttu-id="510b3-187">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="510b3-187">RELATED LINKS</span></span>

[<span data-ttu-id="510b3-188">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="510b3-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="510b3-189">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="510b3-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="510b3-190">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="510b3-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="510b3-191">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="510b3-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="510b3-192">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="510b3-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="510b3-193">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="510b3-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="510b3-194">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="510b3-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


