---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: adb3a44a5d913d636d216750358ebd96c8fc5a29
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928382"
---
# <span data-ttu-id="7e360-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7e360-101">New-AzBatchTask</span></span>

## <span data-ttu-id="7e360-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e360-102">SYNOPSIS</span></span>
<span data-ttu-id="7e360-103">Skapar en batchuppgiften under ett jobb.</span><span class="sxs-lookup"><span data-stu-id="7e360-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="7e360-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e360-104">SYNTAX</span></span>

### <span data-ttu-id="7e360-105">JobId_Single (standard)</span><span class="sxs-lookup"><span data-stu-id="7e360-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e360-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="7e360-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e360-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="7e360-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e360-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="7e360-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e360-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e360-109">DESCRIPTION</span></span>
<span data-ttu-id="7e360-110">Cmdleten **New-AzBatchTask** skapar en Azure Batch-uppgift under det jobb som anges med parametern *jobId* eller *jobb* parameter.</span><span class="sxs-lookup"><span data-stu-id="7e360-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="7e360-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e360-111">EXAMPLES</span></span>

### <span data-ttu-id="7e360-112">Exempel 1: skapa en batchuppgiften</span><span class="sxs-lookup"><span data-stu-id="7e360-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="7e360-113">Det här kommandot skapar en uppgift med ID-Task23 under jobbet som har ID-jobbet-000001.</span><span class="sxs-lookup"><span data-stu-id="7e360-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="7e360-114">Aktiviteten kör det angivna kommandot.</span><span class="sxs-lookup"><span data-stu-id="7e360-114">The task runs the specified command.</span></span>
<span data-ttu-id="7e360-115">Använd cmdleten **Get-AzBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="7e360-115">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7e360-116">Exempel 2: skapa en batchuppgiften</span><span class="sxs-lookup"><span data-stu-id="7e360-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="7e360-117">Det här kommandot får batch-jobbet med ID-000001 genom att använda cmdleten **Get-AzBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="7e360-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="7e360-118">Kommandot skickar jobbet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="7e360-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e360-119">Kommandot skapar en uppgift med ID-Task26 under det jobbet.</span><span class="sxs-lookup"><span data-stu-id="7e360-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="7e360-120">Aktiviteten kör det angivna kommandot med förhöjda behörigheter.</span><span class="sxs-lookup"><span data-stu-id="7e360-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="7e360-121">Exempel 3: lägga till en mängd uppgifter till det angivna jobbet genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="7e360-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="7e360-122">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="7e360-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="7e360-123">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="7e360-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="7e360-124">De två kommandona skapar **PSCloudTask** -objekt med hjälp av New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e360-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="7e360-125">I kommandona lagras aktiviteterna i $Task 01-och $Task 02-variabler.</span><span class="sxs-lookup"><span data-stu-id="7e360-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="7e360-126">Det sista kommandot får batch-jobbet med ID-000001 genom att använda **Get-AzBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="7e360-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="7e360-127">Då överförs det jobbet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="7e360-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e360-128">Kommandot lägger till en mängd uppgifter under det jobbet.</span><span class="sxs-lookup"><span data-stu-id="7e360-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="7e360-129">Kommandot använder kontexten som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="7e360-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="7e360-130">Exempel 4: lägga till en mängd uppgifter i det angivna jobbet</span><span class="sxs-lookup"><span data-stu-id="7e360-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="7e360-131">Det första kommandot skapar en objekt referens till konto nycklarna för batch-kontot som heter ContosoBatchAccount genom att använda **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="7e360-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="7e360-132">Kommandot lagrar objekt referensen i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="7e360-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="7e360-133">De två kommandona skapar **PSCloudTask** -objekt med hjälp av New-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e360-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="7e360-134">I kommandona lagras aktiviteterna i $Task 01-och $Task 02-variabler.</span><span class="sxs-lookup"><span data-stu-id="7e360-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="7e360-135">Med kommandot slut läggs aktiviteterna i $Task 01 och $Task 02 till det jobb som har ID-000001.</span><span class="sxs-lookup"><span data-stu-id="7e360-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="7e360-136">Exempel 5: lägga till en aktivitet med utdatafiler</span><span class="sxs-lookup"><span data-stu-id="7e360-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="7e360-137">Exempel 6: lägga till en aktivitet med inställningar för autentiseringstoken</span><span class="sxs-lookup"><span data-stu-id="7e360-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="7e360-138">Exempel 7: lägga till en aktivitet som körs i en behållare</span><span class="sxs-lookup"><span data-stu-id="7e360-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="7e360-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e360-139">PARAMETERS</span></span>

### <span data-ttu-id="7e360-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="7e360-140">-AffinityInformation</span></span>
<span data-ttu-id="7e360-141">Anger ett lokal tips som används i kommando tjänsten för att välja en nod för att köra uppgiften.</span><span class="sxs-lookup"><span data-stu-id="7e360-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="7e360-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="7e360-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e360-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="7e360-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="7e360-144">Inställningarna för en autentiseringstoken som aktiviteten kan använda för att utföra kommando tjänst åtgärder.</span><span class="sxs-lookup"><span data-stu-id="7e360-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="7e360-145">Om det här alternativet anges tillhandahåller kommando tjänsten aktiviteten med en autentiseringstoken som kan användas för att autentisera kommando tjänst åtgärder utan att behöva en konto åtkomst nyckel.</span><span class="sxs-lookup"><span data-stu-id="7e360-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="7e360-146">Token tillhandahålls via AZ_BATCH_AUTHENTICATION_TOKEN-miljövariabeln.</span><span class="sxs-lookup"><span data-stu-id="7e360-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="7e360-147">Vilka åtgärder som aktiviteten kan utföra med hjälp av token beror på inställningarna.</span><span class="sxs-lookup"><span data-stu-id="7e360-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="7e360-148">En aktivitet kan till exempel begära jobb behörigheter för att lägga till andra uppgifter i jobbet eller kontrol lera status för jobbet eller andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="7e360-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e360-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7e360-149">-BatchContext</span></span>
<span data-ttu-id="7e360-150">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7e360-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7e360-151">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7e360-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7e360-152">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="7e360-152">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7e360-153">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="7e360-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7e360-154">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7e360-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7e360-155">-Kommandorad</span><span class="sxs-lookup"><span data-stu-id="7e360-155">-CommandLine</span></span>
<span data-ttu-id="7e360-156">Anger kommando raden för uppgiften.</span><span class="sxs-lookup"><span data-stu-id="7e360-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="7e360-157">-Begränsningar</span><span class="sxs-lookup"><span data-stu-id="7e360-157">-Constraints</span></span>
<span data-ttu-id="7e360-158">Anger de körnings begränsningar som gäller för den här uppgiften.</span><span class="sxs-lookup"><span data-stu-id="7e360-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="7e360-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="7e360-159">-ContainerSettings</span></span>
<span data-ttu-id="7e360-160">Inställningarna för den behållare under vilken aktiviteten körs.</span><span class="sxs-lookup"><span data-stu-id="7e360-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="7e360-161">Om den pool som kör den här uppgiften har containerConfiguration inställd, måste även detta ställas in.</span><span class="sxs-lookup"><span data-stu-id="7e360-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="7e360-162">Om den pool som kör den här uppgiften inte har containerConfiguration inställd, får den inte vara angiven.</span><span class="sxs-lookup"><span data-stu-id="7e360-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="7e360-163">När detta anges mappas alla kataloger rekursivt under AZ_BATCH_NODE_ROOT_DIR (roten av Azure-gruppkatalogerna på noden) till behållaren, alla aktiviteter för aktivitets miljön mappas till behållaren och kommando raden för uppgiften utförs i behållaren.</span><span class="sxs-lookup"><span data-stu-id="7e360-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e360-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e360-164">-DefaultProfile</span></span>
<span data-ttu-id="7e360-165">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e360-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e360-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="7e360-166">-DependsOn</span></span>
<span data-ttu-id="7e360-167">Anger att aktiviteten är beroende av andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="7e360-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="7e360-168">Aktiviteten schemaläggs inte förrän alla förväntade uppgifter har genomförts.</span><span class="sxs-lookup"><span data-stu-id="7e360-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="7e360-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7e360-169">-DisplayName</span></span>
<span data-ttu-id="7e360-170">Anger uppgiftens visnings namn.</span><span class="sxs-lookup"><span data-stu-id="7e360-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="7e360-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="7e360-171">-EnvironmentSettings</span></span>
<span data-ttu-id="7e360-172">Anger miljö inställningar, som nycklar/värde par, som denna cmdlet lägger till i uppgiften.</span><span class="sxs-lookup"><span data-stu-id="7e360-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="7e360-173">Det här är namnet på miljö inställningen.</span><span class="sxs-lookup"><span data-stu-id="7e360-173">The key is the environment setting name.</span></span>
<span data-ttu-id="7e360-174">Värdet är miljö inställningen.</span><span class="sxs-lookup"><span data-stu-id="7e360-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e360-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="7e360-175">-ExitConditions</span></span>
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

### <span data-ttu-id="7e360-176">-ID</span><span class="sxs-lookup"><span data-stu-id="7e360-176">-Id</span></span>
<span data-ttu-id="7e360-177">Anger aktivitetens ID.</span><span class="sxs-lookup"><span data-stu-id="7e360-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="7e360-178">-Jobb</span><span class="sxs-lookup"><span data-stu-id="7e360-178">-Job</span></span>
<span data-ttu-id="7e360-179">Anger det jobb under vilket denna cmdlet skapar uppgiften.</span><span class="sxs-lookup"><span data-stu-id="7e360-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="7e360-180">För att hämta ett **PSCloudJob** -objekt, Använd cmdleten Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="7e360-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="7e360-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="7e360-181">-JobId</span></span>
<span data-ttu-id="7e360-182">Anger ID för det jobb som den här cmdleten skapar för aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="7e360-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="7e360-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="7e360-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="7e360-184">Anger information om hur du kör en aktivitet med flera instanser.</span><span class="sxs-lookup"><span data-stu-id="7e360-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="7e360-185">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="7e360-185">-OutputFile</span></span>
<span data-ttu-id="7e360-186">Hämtar eller anger en lista med filer som kommando tjänsten laddar upp från noden Compute när kommando raden körs.</span><span class="sxs-lookup"><span data-stu-id="7e360-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="7e360-187">För aktiviteter med flera instanser kommer filerna bara att laddas upp från den datornod som den primära aktiviteten körs på.</span><span class="sxs-lookup"><span data-stu-id="7e360-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e360-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="7e360-188">-ResourceFiles</span></span>
<span data-ttu-id="7e360-189">Anger resursfiler, som nycklar/värde par, som aktiviteten kräver.</span><span class="sxs-lookup"><span data-stu-id="7e360-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="7e360-190">Nyckelns fil Sök väg.</span><span class="sxs-lookup"><span data-stu-id="7e360-190">The key is the resource file path.</span></span>
<span data-ttu-id="7e360-191">Värdet är resurs filens BLOB-källa.</span><span class="sxs-lookup"><span data-stu-id="7e360-191">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e360-192">-Uppgifter</span><span class="sxs-lookup"><span data-stu-id="7e360-192">-Tasks</span></span>
<span data-ttu-id="7e360-193">Anger mängden med uppgifter som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="7e360-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="7e360-194">Varje uppgift måste ha ett unikt ID.</span><span class="sxs-lookup"><span data-stu-id="7e360-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="7e360-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="7e360-195">-UserIdentity</span></span>
<span data-ttu-id="7e360-196">Den användar identitet under vilken aktiviteten körs.</span><span class="sxs-lookup"><span data-stu-id="7e360-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e360-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e360-197">CommonParameters</span></span>
<span data-ttu-id="7e360-198">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e360-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e360-199">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e360-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e360-200">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e360-200">INPUTS</span></span>

### <span data-ttu-id="7e360-201">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="7e360-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="7e360-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7e360-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7e360-203">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e360-203">OUTPUTS</span></span>

### <span data-ttu-id="7e360-204">System. Void</span><span class="sxs-lookup"><span data-stu-id="7e360-204">System.Void</span></span>

## <span data-ttu-id="7e360-205">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e360-205">NOTES</span></span>

## <span data-ttu-id="7e360-206">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e360-206">RELATED LINKS</span></span>

[<span data-ttu-id="7e360-207">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7e360-207">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7e360-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="7e360-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="7e360-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7e360-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="7e360-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7e360-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="7e360-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7e360-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="7e360-212">Stopp-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="7e360-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="7e360-213">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7e360-213">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

