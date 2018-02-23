# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="7f586-101">Större ändringar för Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="7f586-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="7f586-102">Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7f586-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="7f586-103">I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet.</span><span class="sxs-lookup"><span data-stu-id="7f586-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="7f586-104">Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.</span><span class="sxs-lookup"><span data-stu-id="7f586-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="7f586-105">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="7f586-105">Table of Contents</span></span>

- [<span data-ttu-id="7f586-106">Större ändringar i ApiManagement-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="7f586-107">Större ändringar i Batch-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="7f586-108">Större ändringar i Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="7f586-109">Större ändringar i EventHub-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="7f586-110">Större ändringar i Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="7f586-111">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="7f586-112">Större ändringar i Resources-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="7f586-113">Större ändringar i ServiceBus-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="7f586-114">Större ändringar i ApiManagement-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="7f586-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="7f586-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="7f586-116">Parametrarna ”UserName” och ”Password” ersätts av PSCredential</span><span class="sxs-lookup"><span data-stu-id="7f586-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="7f586-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="7f586-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="7f586-118">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="7f586-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="7f586-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="7f586-120">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="7f586-121">Större ändringar i Batch-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="7f586-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="7f586-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="7f586-123">Parametern `Password` ersätts av en säker sträng</span><span class="sxs-lookup"><span data-stu-id="7f586-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="7f586-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="7f586-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="7f586-125">Parametern `Password` ersätts av en säker sträng</span><span class="sxs-lookup"><span data-stu-id="7f586-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="7f586-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="7f586-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="7f586-127">Parametern `Password` ersätts av en säker sträng</span><span class="sxs-lookup"><span data-stu-id="7f586-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="7f586-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="7f586-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="7f586-129">Växeln `RunElevated` har tagits bort och ersatts med `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="7f586-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="7f586-130">Detta påverkar även egenskapen `RunElevated` på `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` och `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="7f586-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="7f586-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="7f586-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="7f586-132">`PSMultiInstanceSettings`-konstruktorn tar inte längre en obligatorisk `numberOfInstances`-parameter. Den tar i stället en nödvändig `coordinationCommandLine`-parameter.</span><span class="sxs-lookup"><span data-stu-id="7f586-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="7f586-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="7f586-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="7f586-134">Egenskapen `RunElevated` har tagits bort på `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="7f586-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="7f586-135">Egenskapen `UserIdentity` har lagts till för att ersätta `RunElevated`.</span><span class="sxs-lookup"><span data-stu-id="7f586-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="7f586-136">Detta påverkar även egenskapen `RunElevated` på `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` och `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="7f586-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="7f586-137">**Flera typer**</span><span class="sxs-lookup"><span data-stu-id="7f586-137">**Multiple types**</span></span>

- <span data-ttu-id="7f586-138">Egenskapen `SchedulingError` på `PSExitConditions` har bytt namn till `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="7f586-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="7f586-139">**Flera typer**</span><span class="sxs-lookup"><span data-stu-id="7f586-139">**Multiple types**</span></span>

- <span data-ttu-id="7f586-140">Egenskapen `SchedulingError` på `PSJobPreparationTaskExecutionInformation` har bytt namn till `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` och `PSTaskExecutionInformation` till `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="7f586-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="7f586-141">`FailureInformation` returneras när ett fel uppstår i uppgiften.</span><span class="sxs-lookup"><span data-stu-id="7f586-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="7f586-142">Det här omfattar alla tidigare fall av schemaläggningsfel, slutkoder för aktiviteter utan nollor och fel vid uppladdning av filer från den nya funktionen för utdatafiler.</span><span class="sxs-lookup"><span data-stu-id="7f586-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="7f586-143">Det här är strukturerat på samma sätt som tidigare, så du behöver inte göra några ändringar i koden när du använder den här typen.</span><span class="sxs-lookup"><span data-stu-id="7f586-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="7f586-144">Det här påverkar dessutom: Get-AzureBatchPool, Get-AzureBatchSubtask och Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="7f586-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="7f586-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="7f586-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="7f586-146">`TargetDedicated` har tagits bort och ersatts med `TargetDedicatedComputeNodes` och `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="7f586-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="7f586-147">`TargetDedicatedComputeNodes` har ett alias `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="7f586-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="7f586-148">Det här påverkar dessutom: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="7f586-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="7f586-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="7f586-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="7f586-150">Egenskaperna `TargetDedicated` och `CurrentDedicated` på `PSCloudPool` har bytt namn till `TargetDedicatedComputeNodes` och `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="7f586-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

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

### <a name="type-pscloudpool"></a><span data-ttu-id="7f586-151">**PSCloudPool-typ**</span><span class="sxs-lookup"><span data-stu-id="7f586-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="7f586-152">`ResizeError` har bytt namn till `ResizeErrors` på `PSCloudPool` och det är nu en samling.</span><span class="sxs-lookup"><span data-stu-id="7f586-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="7f586-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="7f586-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="7f586-154">Egenskapen `TargetDedicated` på `PSPoolSpecification` har bytt namn till `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="7f586-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

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

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="7f586-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="7f586-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="7f586-156">`Name` har tagits bort och ersatts med `Path`.</span><span class="sxs-lookup"><span data-stu-id="7f586-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="7f586-157">`Path` har ett alias `Name`.</span><span class="sxs-lookup"><span data-stu-id="7f586-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="7f586-158">Det här påverkar dessutom: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="7f586-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="7f586-159">Typen **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="7f586-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="7f586-160">Egenskapen `Name` på `PSNodeFile` har bytt namn till `Path`.</span><span class="sxs-lookup"><span data-stu-id="7f586-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="7f586-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="7f586-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="7f586-162">Egenskaperna `PreviousState` och `State` för `PSSubtaskInformation` är inte längre är av typen `TaskState`.De är istället av typen `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="7f586-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="7f586-163">Till skillnad från `TaskState` har inte `SubtaskState` något `Active`-värde eftersom det inte är möjligt för underuppgifter att vara i tillståndet `Active`.</span><span class="sxs-lookup"><span data-stu-id="7f586-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="7f586-164">Större ändringar i Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="7f586-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="7f586-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="7f586-166">Parametrarna ”UserName” och ”Password” ersätts av PSCredential</span><span class="sxs-lookup"><span data-stu-id="7f586-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="7f586-167">Större ändringar i EventHub-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="7f586-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-169">Cmdleten ”New-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-170">Använd cmdleten ”New-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="7f586-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="7f586-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-172">Cmdleten ”Get-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-173">Använd cmdleten ”Get-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="7f586-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="7f586-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-175">Cmdleten ”Set-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-176">Använd cmdleten ”Set-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="7f586-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="7f586-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-178">Cmdleten ”Remove-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-179">Använd cmdleten ”Remove-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="7f586-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="7f586-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="7f586-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="7f586-181">Cmdleten ”New-AzureRmEventHubNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-182">Använd cmdleten ”New-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="7f586-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="7f586-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="7f586-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="7f586-184">Cmdleten ”Get-AzureRmEventHubNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-185">Använd cmdleten ”Get-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="7f586-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="7f586-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="7f586-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="7f586-187">Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="7f586-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

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
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="7f586-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="7f586-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="7f586-189">Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="7f586-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

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
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="7f586-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="7f586-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="7f586-191">Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="7f586-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

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
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="7f586-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="7f586-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="7f586-193">Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="7f586-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="7f586-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="7f586-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="7f586-195">Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="7f586-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="7f586-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="7f586-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="7f586-197">Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="7f586-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="7f586-198">Större ändringar i Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="7f586-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="7f586-200">Cmdleten **Add-AzureRMLogAlertRule** har gjorts inaktuell</span><span class="sxs-lookup"><span data-stu-id="7f586-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="7f586-201">Efter den 1 oktober kommer den här cmdleten inte längre att ha någon effekt eftersom den här funktionen kommer att övergå till aktivitetsloggaviseringar.</span><span class="sxs-lookup"><span data-stu-id="7f586-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="7f586-202">Mer information finns på https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="7f586-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="7f586-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="7f586-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="7f586-204">Cmdleten **Get-AzureRMUsage** har gjorts inaktuell</span><span class="sxs-lookup"><span data-stu-id="7f586-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="7f586-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="7f586-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="7f586-206">Ändring i utdata: Fältet EventChannels från EventData-objektet (som returneras av de här cmdletarna) kommer att bli inaktuellt eftersom det nu returnerar ett konstant värde (Admin, Åtgärd.)</span><span class="sxs-lookup"><span data-stu-id="7f586-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="7f586-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="7f586-208">Ändring i utdata: Utdata från den här cmdleten jämnas ut. Det innebär att egenskapsfältet kommer att tas bort för att förbättra användarupplevelsen.</span><span class="sxs-lookup"><span data-stu-id="7f586-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

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

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="7f586-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="7f586-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="7f586-210">Ändring i utdata: Fältet AutoscaleSettingResourceName kommer att bli inaktuellt eftersom det alltid är samma som fältet Name.</span><span class="sxs-lookup"><span data-stu-id="7f586-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="7f586-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="7f586-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="7f586-212">Ändring i utdata: Typen av utdata kommer att ändras så att ett enda objekt som innehåller ID för begäran och statuskod returneras.</span><span class="sxs-lookup"><span data-stu-id="7f586-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

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

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="7f586-213">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="7f586-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="7f586-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="7f586-215">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="7f586-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="7f586-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="7f586-217">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="7f586-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="7f586-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="7f586-219">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="7f586-220">Större ändringar i Resources-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="7f586-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="7f586-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="7f586-222">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="7f586-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="7f586-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="7f586-224">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="7f586-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="7f586-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="7f586-226">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="7f586-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="7f586-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="7f586-228">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="7f586-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="7f586-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="7f586-230">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="7f586-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="7f586-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="7f586-232">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="7f586-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="7f586-233">Större ändringar i ServiceBus-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7f586-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="7f586-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-235">Cmdleten ”Get-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-236">Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="7f586-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="7f586-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="7f586-238">Cmdleten ”Get-AzureRmServiceBusTopicKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-239">Använd cmdleten ”Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="7f586-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="7f586-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-241">Cmdleten ”New-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-242">Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="7f586-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="7f586-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="7f586-244">Cmdleten ”New-AzureRmServiceBusTopicKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-245">Använd cmdleten ”New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="7f586-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="7f586-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-247">Cmdleten ”Remove-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-248">Använd cmdleten ”Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="7f586-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-250">Cmdleten ”Set-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-251">Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="7f586-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="7f586-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="7f586-253">Cmdleten ”New-AzureRmServiceBusNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-254">Använd cmdleten ”New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="7f586-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="7f586-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-256">Cmdleten ”Get-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-257">Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="7f586-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="7f586-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="7f586-259">Cmdleten ”Get-AzureRmServiceBusQueueKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-260">Använd cmdleten ”Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="7f586-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="7f586-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-262">Cmdleten ”New-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-263">Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="7f586-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="7f586-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="7f586-265">Cmdleten ”New-AzureRmServiceBusQueueKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-266">Använd cmdleten ”New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="7f586-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="7f586-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-268">Cmdleten ”Remove-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-269">Använd cmdleten ”GRemove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="7f586-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-271">Cmdleten ”Set-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-272">Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="7f586-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-274">Cmdleten ”Get-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-275">Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="7f586-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="7f586-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="7f586-277">Cmdleten ”Get-AzureRmServiceBusNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-278">Använd cmdleten ”Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="7f586-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="7f586-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-280">Cmdleten ”New-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-281">Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="7f586-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-283">Cmdleten ”Remove-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-284">Använd cmdleten ”Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="7f586-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="7f586-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="7f586-286">Cmdleten ”Set-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7f586-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="7f586-287">Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="7f586-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="7f586-288">**Typen NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="7f586-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="7f586-289">Följande egenskaper har tagits bort</span><span class="sxs-lookup"><span data-stu-id="7f586-289">The following properties have been removed</span></span>
    - <span data-ttu-id="7f586-290">Enabled</span><span class="sxs-lookup"><span data-stu-id="7f586-290">Enabled</span></span>
    - <span data-ttu-id="7f586-291">Status</span><span class="sxs-lookup"><span data-stu-id="7f586-291">Status</span></span>
   
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

### <a name="type-queueattribute"></a><span data-ttu-id="7f586-292">**Typen QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="7f586-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="7f586-293">Följande egenskaper har angetts som föråldrade:</span><span class="sxs-lookup"><span data-stu-id="7f586-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="7f586-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="7f586-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="7f586-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="7f586-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="7f586-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="7f586-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="7f586-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="7f586-297">SupportOrdering</span></span>

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
   
### <a name="type-topicattribute"></a><span data-ttu-id="7f586-298">**Typen TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="7f586-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="7f586-299">Följande egenskaper har angetts som föråldrade:</span><span class="sxs-lookup"><span data-stu-id="7f586-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="7f586-300">Plats</span><span class="sxs-lookup"><span data-stu-id="7f586-300">Location</span></span>
    - <span data-ttu-id="7f586-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="7f586-301">IsExpress</span></span>
    - <span data-ttu-id="7f586-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="7f586-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="7f586-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="7f586-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="7f586-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="7f586-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="7f586-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="7f586-305">EntityAvailabilityStatus</span></span>

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
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="7f586-306">**Typen SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="7f586-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="7f586-307">Följande egenskaper har angetts som föråldrade</span><span class="sxs-lookup"><span data-stu-id="7f586-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="7f586-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="7f586-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="7f586-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="7f586-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="7f586-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="7f586-310">IsReadOnly</span></span>
    - <span data-ttu-id="7f586-311">Plats</span><span class="sxs-lookup"><span data-stu-id="7f586-311">Location</span></span>
   
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