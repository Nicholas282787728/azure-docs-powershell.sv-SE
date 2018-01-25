# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="5abed-101">Större ändringar för Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="5abed-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="5abed-102">Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="5abed-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5abed-103">I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet.</span><span class="sxs-lookup"><span data-stu-id="5abed-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="5abed-104">Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.</span><span class="sxs-lookup"><span data-stu-id="5abed-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="5abed-105">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="5abed-105">Table of Contents</span></span>

- [<span data-ttu-id="5abed-106">Större ändringar i ApiManagement-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="5abed-107">Större ändringar i Batch-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="5abed-108">Större ändringar i Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="5abed-109">Större ändringar i EventHub-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="5abed-110">Större ändringar i Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="5abed-111">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="5abed-112">Större ändringar i Resources-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="5abed-113">Större ändringar i ServiceBus-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="5abed-114">Större ändringar i ApiManagement-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="5abed-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="5abed-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="5abed-116">Parametrarna ”UserName” och ”Password” ersätts av PSCredential</span><span class="sxs-lookup"><span data-stu-id="5abed-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="5abed-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="5abed-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="5abed-118">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="5abed-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="5abed-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="5abed-120">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="5abed-121">Större ändringar i Batch-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="5abed-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="5abed-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="5abed-123">Parametern `Password` ersätts av en säker sträng</span><span class="sxs-lookup"><span data-stu-id="5abed-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="5abed-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="5abed-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="5abed-125">Parametern `Password` ersätts av en säker sträng</span><span class="sxs-lookup"><span data-stu-id="5abed-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="5abed-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="5abed-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="5abed-127">Parametern `Password` ersätts av en säker sträng</span><span class="sxs-lookup"><span data-stu-id="5abed-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="5abed-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="5abed-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="5abed-129">Växeln `RunElevated` har tagits bort och ersatts med `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="5abed-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="5abed-130">Detta påverkar även egenskapen `RunElevated` på `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` och `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="5abed-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="5abed-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="5abed-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="5abed-132">`PSMultiInstanceSettings`-konstruktorn tar inte längre en obligatorisk `numberOfInstances`-parameter. Den tar i stället en nödvändig `coordinationCommandLine`-parameter.</span><span class="sxs-lookup"><span data-stu-id="5abed-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="5abed-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="5abed-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="5abed-134">Egenskapen `RunElevated` har tagits bort på `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="5abed-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="5abed-135">Egenskapen `UserIdentity` har lagts till för att ersätta `RunElevated`.</span><span class="sxs-lookup"><span data-stu-id="5abed-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="5abed-136">Detta påverkar även egenskapen `RunElevated` på `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` och `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="5abed-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="5abed-137">**Flera typer**</span><span class="sxs-lookup"><span data-stu-id="5abed-137">**Multiple types**</span></span>

- <span data-ttu-id="5abed-138">Egenskapen `SchedulingError` på `PSExitConditions` har bytt namn till `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="5abed-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="5abed-139">**Flera typer**</span><span class="sxs-lookup"><span data-stu-id="5abed-139">**Multiple types**</span></span>

- <span data-ttu-id="5abed-140">Egenskapen `SchedulingError` på `PSJobPreparationTaskExecutionInformation` har bytt namn till `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` och `PSTaskExecutionInformation` till `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="5abed-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="5abed-141">`FailureInformation` returneras när ett fel uppstår i uppgiften.</span><span class="sxs-lookup"><span data-stu-id="5abed-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="5abed-142">Det här omfattar alla tidigare fall av schemaläggningsfel, slutkoder för aktiviteter utan nollor och fel vid uppladdning av filer från den nya funktionen för utdatafiler.</span><span class="sxs-lookup"><span data-stu-id="5abed-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="5abed-143">Det här är strukturerat på samma sätt som tidigare, så du behöver inte göra några ändringar i koden när du använder den här typen.</span><span class="sxs-lookup"><span data-stu-id="5abed-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="5abed-144">Det här påverkar dessutom: Get-AzureBatchPool, Get-AzureBatchSubtask och Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="5abed-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="5abed-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="5abed-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="5abed-146">`TargetDedicated` har tagits bort och ersatts med `TargetDedicatedComputeNodes` och `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="5abed-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="5abed-147">`TargetDedicatedComputeNodes` har ett alias `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="5abed-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="5abed-148">Det här påverkar dessutom: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="5abed-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="5abed-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="5abed-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="5abed-150">Egenskaperna `TargetDedicated` och `CurrentDedicated` på `PSCloudPool` har bytt namn till `TargetDedicatedComputeNodes` och `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="5abed-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="5abed-151">**PSCloudPool-typ**</span><span class="sxs-lookup"><span data-stu-id="5abed-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="5abed-152">`ResizeError` har bytt namn till `ResizeErrors` på `PSCloudPool` och det är nu en samling.</span><span class="sxs-lookup"><span data-stu-id="5abed-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="5abed-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="5abed-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="5abed-154">Egenskapen `TargetDedicated` på `PSPoolSpecification` har bytt namn till `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="5abed-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="5abed-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="5abed-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="5abed-156">`Name` har tagits bort och ersatts med `Path`.</span><span class="sxs-lookup"><span data-stu-id="5abed-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="5abed-157">`Path` har ett alias `Name`.</span><span class="sxs-lookup"><span data-stu-id="5abed-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="5abed-158">Det här påverkar dessutom: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="5abed-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="5abed-159">Typen **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="5abed-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="5abed-160">Egenskapen `Name` på `PSNodeFile` har bytt namn till `Path`.</span><span class="sxs-lookup"><span data-stu-id="5abed-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="5abed-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="5abed-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="5abed-162">Egenskaperna `PreviousState` och `State` för `PSSubtaskInformation` är inte längre är av typen `TaskState`.De är istället av typen `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="5abed-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="5abed-163">Till skillnad från `TaskState` har inte `SubtaskState` något `Active`-värde eftersom det inte är möjligt för underuppgifter att vara i tillståndet `Active`.</span><span class="sxs-lookup"><span data-stu-id="5abed-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="5abed-164">Större ändringar i Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="5abed-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="5abed-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="5abed-166">Parametrarna ”UserName” och ”Password” ersätts av PSCredential</span><span class="sxs-lookup"><span data-stu-id="5abed-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="5abed-167">Större ändringar i EventHub-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="5abed-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-169">Cmdleten ”New-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-170">Använd cmdleten ”New-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="5abed-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="5abed-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-172">Cmdleten ”Get-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-173">Använd cmdleten ”Get-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="5abed-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="5abed-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-175">Cmdleten ”Set-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-176">Använd cmdleten ”Set-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="5abed-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="5abed-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-178">Cmdleten ”Remove-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-179">Använd cmdleten ”Remove-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="5abed-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="5abed-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="5abed-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="5abed-181">Cmdleten ”New-AzureRmEventHubNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-182">Använd cmdleten ”New-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="5abed-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="5abed-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="5abed-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="5abed-184">Cmdleten ”Get-AzureRmEventHubNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-185">Använd cmdleten ”Get-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="5abed-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="5abed-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="5abed-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="5abed-187">Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="5abed-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="5abed-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="5abed-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="5abed-189">Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="5abed-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="5abed-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="5abed-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="5abed-191">Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="5abed-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="5abed-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="5abed-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="5abed-193">Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="5abed-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="5abed-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="5abed-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="5abed-195">Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="5abed-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="5abed-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="5abed-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="5abed-197">Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="5abed-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="5abed-198">Större ändringar i Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="5abed-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="5abed-200">Cmdleten **Add-AzureRMLogAlertRule** har gjorts inaktuell</span><span class="sxs-lookup"><span data-stu-id="5abed-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="5abed-201">Efter den 1 oktober kommer den här cmdleten inte längre att ha någon effekt eftersom den här funktionen kommer att övergå till aktivitetsloggaviseringar.</span><span class="sxs-lookup"><span data-stu-id="5abed-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="5abed-202">Mer information finns på https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="5abed-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="5abed-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="5abed-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="5abed-204">Cmdleten **Get-AzureRMUsage** har gjorts inaktuell</span><span class="sxs-lookup"><span data-stu-id="5abed-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="5abed-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="5abed-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="5abed-206">Ändring i utdata: Fältet EventChannels från EventData-objektet (som returneras av de här cmdletarna) kommer att bli inaktuellt eftersom det nu returnerar ett konstant värde (Admin, Åtgärd.)</span><span class="sxs-lookup"><span data-stu-id="5abed-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="5abed-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="5abed-208">Ändring i utdata: Utdata från den här cmdleten jämnas ut. Det innebär att egenskapsfältet kommer att tas bort för att förbättra användarupplevelsen.</span><span class="sxs-lookup"><span data-stu-id="5abed-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="5abed-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="5abed-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="5abed-210">Ändring i utdata: Fältet AutoscaleSettingResourceName kommer att bli inaktuellt eftersom det alltid är samma som fältet Name.</span><span class="sxs-lookup"><span data-stu-id="5abed-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="5abed-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="5abed-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="5abed-212">Ändring i utdata: Typen av utdata kommer att ändras så att ett enda objekt som innehåller ID för begäran och statuskod returneras.</span><span class="sxs-lookup"><span data-stu-id="5abed-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="5abed-213">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="5abed-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="5abed-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="5abed-215">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="5abed-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="5abed-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="5abed-217">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="5abed-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="5abed-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="5abed-219">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="5abed-220">Större ändringar i Resources-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="5abed-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="5abed-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="5abed-222">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="5abed-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="5abed-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="5abed-224">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="5abed-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="5abed-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="5abed-226">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="5abed-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="5abed-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="5abed-228">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="5abed-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="5abed-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="5abed-230">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="5abed-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="5abed-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="5abed-232">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="5abed-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="5abed-233">Större ändringar i ServiceBus-cmdletar</span><span class="sxs-lookup"><span data-stu-id="5abed-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="5abed-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-235">Cmdleten ”Get-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-236">Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="5abed-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="5abed-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="5abed-238">Cmdleten ”Get-AzureRmServiceBusTopicKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-239">Använd cmdleten ”Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5abed-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="5abed-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-241">Cmdleten ”New-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-242">Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="5abed-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="5abed-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="5abed-244">Cmdleten ”New-AzureRmServiceBusTopicKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-245">Använd cmdleten ”New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5abed-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="5abed-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-247">Cmdleten ”Remove-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-248">Använd cmdleten ”Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="5abed-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-250">Cmdleten ”Set-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-251">Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="5abed-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="5abed-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="5abed-253">Cmdleten ”New-AzureRmServiceBusNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-254">Använd cmdleten ”New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5abed-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="5abed-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-256">Cmdleten ”Get-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-257">Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="5abed-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="5abed-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="5abed-259">Cmdleten ”Get-AzureRmServiceBusQueueKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-260">Använd cmdleten ”Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5abed-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="5abed-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-262">Cmdleten ”New-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-263">Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="5abed-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="5abed-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="5abed-265">Cmdleten ”New-AzureRmServiceBusQueueKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-266">Använd cmdleten ”New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5abed-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="5abed-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-268">Cmdleten ”Remove-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-269">Använd cmdleten ”GRemove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="5abed-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-271">Cmdleten ”Set-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-272">Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="5abed-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-274">Cmdleten ”Get-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-275">Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="5abed-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="5abed-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="5abed-277">Cmdleten ”Get-AzureRmServiceBusNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-278">Använd cmdleten ”Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="5abed-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="5abed-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-280">Cmdleten ”New-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-281">Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="5abed-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-283">Cmdleten ”Remove-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-284">Använd cmdleten ”Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="5abed-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="5abed-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="5abed-286">Cmdleten ”Set-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="5abed-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="5abed-287">Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="5abed-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="5abed-288">**Typen NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="5abed-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="5abed-289">Följande egenskaper har tagits bort</span><span class="sxs-lookup"><span data-stu-id="5abed-289">The following properties have been removed</span></span>
    - <span data-ttu-id="5abed-290">Enabled</span><span class="sxs-lookup"><span data-stu-id="5abed-290">Enabled</span></span>
    - <span data-ttu-id="5abed-291">Status</span><span class="sxs-lookup"><span data-stu-id="5abed-291">Status</span></span>
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="5abed-292">**Typen QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="5abed-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="5abed-293">Följande egenskaper har angetts som föråldrade:</span><span class="sxs-lookup"><span data-stu-id="5abed-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="5abed-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="5abed-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="5abed-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="5abed-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="5abed-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="5abed-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="5abed-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="5abed-297">SupportOrdering</span></span>

```powershell
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="5abed-298">**Typen TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="5abed-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="5abed-299">Följande egenskaper har angetts som föråldrade:</span><span class="sxs-lookup"><span data-stu-id="5abed-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="5abed-300">Plats</span><span class="sxs-lookup"><span data-stu-id="5abed-300">Location</span></span>
    - <span data-ttu-id="5abed-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="5abed-301">IsExpress</span></span>
    - <span data-ttu-id="5abed-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="5abed-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="5abed-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="5abed-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="5abed-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="5abed-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="5abed-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="5abed-305">EntityAvailabilityStatus</span></span>

```powershell
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="5abed-306">**Typen SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="5abed-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="5abed-307">Följande egenskaper har angetts som föråldrade</span><span class="sxs-lookup"><span data-stu-id="5abed-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="5abed-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="5abed-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="5abed-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="5abed-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="5abed-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="5abed-310">IsReadOnly</span></span>
    - <span data-ttu-id="5abed-311">Plats</span><span class="sxs-lookup"><span data-stu-id="5abed-311">Location</span></span>
   
```powershell
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```