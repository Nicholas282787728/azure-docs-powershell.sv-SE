---
title: Större ändringar för Microsoft Azure PowerShell 5.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i version 5 av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: f8dc413a91876e53e62d25cc38ac3b3ef6afda8e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534595"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="25fe1-103">Större ändringar för Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="25fe1-103">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="25fe1-104">Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="25fe1-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="25fe1-105">I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet.</span><span class="sxs-lookup"><span data-stu-id="25fe1-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="25fe1-106">Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.</span><span class="sxs-lookup"><span data-stu-id="25fe1-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="25fe1-107">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="25fe1-107">Table of Contents</span></span>

- [<span data-ttu-id="25fe1-108">Större ändringar i ApiManagement-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-108">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="25fe1-109">Större ändringar i Batch-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-109">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="25fe1-110">Större ändringar i Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-110">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="25fe1-111">Större ändringar i EventHub-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-111">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="25fe1-112">Större ändringar i Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-112">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="25fe1-113">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-113">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="25fe1-114">Större ändringar i Resources-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-114">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="25fe1-115">Större ändringar i ServiceBus-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-115">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="25fe1-116">Större ändringar i ApiManagement-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-116">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="25fe1-117">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="25fe1-117">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="25fe1-118">Parametrarna ”UserName” och ”Password” ersätts av PSCredential</span><span class="sxs-lookup"><span data-stu-id="25fe1-118">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="25fe1-119">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="25fe1-119">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="25fe1-120">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="25fe1-121">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="25fe1-121">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="25fe1-122">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-122">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="25fe1-123">Större ändringar i Batch-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-123">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="25fe1-124">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="25fe1-124">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="25fe1-125">Parametern `Password` ersätts av en säker sträng</span><span class="sxs-lookup"><span data-stu-id="25fe1-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="25fe1-126">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="25fe1-126">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="25fe1-127">Parametern `Password` ersätts av en säker sträng</span><span class="sxs-lookup"><span data-stu-id="25fe1-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="25fe1-128">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="25fe1-128">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="25fe1-129">Parametern `Password` ersätts av en säker sträng</span><span class="sxs-lookup"><span data-stu-id="25fe1-129">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="25fe1-130">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="25fe1-130">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="25fe1-131">Växeln `RunElevated` har tagits bort och ersatts med `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-131">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="25fe1-132">Detta påverkar även egenskapen `RunElevated` på `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` och `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-132">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="25fe1-133">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="25fe1-133">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="25fe1-134">`PSMultiInstanceSettings`-konstruktorn tar inte längre en obligatorisk `numberOfInstances`-parameter. Den tar i stället en nödvändig `coordinationCommandLine`-parameter.</span><span class="sxs-lookup"><span data-stu-id="25fe1-134">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="25fe1-135">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="25fe1-135">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="25fe1-136">Egenskapen `RunElevated` har tagits bort på `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-136">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="25fe1-137">Egenskapen `UserIdentity` har lagts till för att ersätta `RunElevated`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-137">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="25fe1-138">Detta påverkar även egenskapen `RunElevated` på `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` och `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-138">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="25fe1-139">**Flera typer**</span><span class="sxs-lookup"><span data-stu-id="25fe1-139">**Multiple types**</span></span>

- <span data-ttu-id="25fe1-140">Egenskapen `SchedulingError` på `PSExitConditions` har bytt namn till `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-140">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="25fe1-141">**Flera typer**</span><span class="sxs-lookup"><span data-stu-id="25fe1-141">**Multiple types**</span></span>

- <span data-ttu-id="25fe1-142">Egenskapen `SchedulingError` på `PSJobPreparationTaskExecutionInformation` har bytt namn till `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` och `PSTaskExecutionInformation` till `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-142">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="25fe1-143">`FailureInformation` returneras när ett fel uppstår i uppgiften.</span><span class="sxs-lookup"><span data-stu-id="25fe1-143">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="25fe1-144">Det här omfattar alla tidigare fall av schemaläggningsfel, slutkoder för aktiviteter utan nollor och fel vid uppladdning av filer från den nya funktionen för utdatafiler.</span><span class="sxs-lookup"><span data-stu-id="25fe1-144">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="25fe1-145">Det här är strukturerat på samma sätt som tidigare, så du behöver inte göra några ändringar i koden när du använder den här typen.</span><span class="sxs-lookup"><span data-stu-id="25fe1-145">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="25fe1-146">Det här påverkar även: Get-AzureBatchPool, Get-AzureBatchSubtask och Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="25fe1-146">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="25fe1-147">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="25fe1-147">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="25fe1-148">`TargetDedicated` har tagits bort och ersatts med `TargetDedicatedComputeNodes` och `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-148">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="25fe1-149">`TargetDedicatedComputeNodes` har ett alias `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-149">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="25fe1-150">Det här påverkar dessutom: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="25fe1-150">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="25fe1-151">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="25fe1-151">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="25fe1-152">Egenskaperna `TargetDedicated` och `CurrentDedicated` på `PSCloudPool` har bytt namn till `TargetDedicatedComputeNodes` och `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-152">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="25fe1-153">**PSCloudPool-typ**</span><span class="sxs-lookup"><span data-stu-id="25fe1-153">**Type PSCloudPool**</span></span>

- <span data-ttu-id="25fe1-154">`ResizeError` har bytt namn till `ResizeErrors` på `PSCloudPool` och det är nu en samling.</span><span class="sxs-lookup"><span data-stu-id="25fe1-154">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="25fe1-155">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="25fe1-155">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="25fe1-156">Egenskapen `TargetDedicated` på `PSPoolSpecification` har bytt namn till `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-156">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell-interactive
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

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="25fe1-157">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="25fe1-157">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="25fe1-158">`Name` har tagits bort och ersatts med `Path`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-158">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="25fe1-159">`Path` har ett alias `Name`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-159">`Path` has an alias `Name`.</span></span>

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="25fe1-160">Det här påverkar dessutom: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="25fe1-160">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="25fe1-161">Typen **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="25fe1-161">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="25fe1-162">Egenskapen `Name` på `PSNodeFile` har bytt namn till `Path`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-162">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="25fe1-163">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="25fe1-163">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="25fe1-164">Egenskaperna `PreviousState` och `State` för `PSSubtaskInformation` är inte längre är av typen `TaskState`.De är istället av typen `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-164">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="25fe1-165">Till skillnad från `TaskState` har inte `SubtaskState` något `Active`-värde eftersom det inte är möjligt för underuppgifter att vara i tillståndet `Active`.</span><span class="sxs-lookup"><span data-stu-id="25fe1-165">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="25fe1-166">Större ändringar i Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-166">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="25fe1-167">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="25fe1-167">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="25fe1-168">Parametrarna ”UserName” och ”Password” ersätts av PSCredential</span><span class="sxs-lookup"><span data-stu-id="25fe1-168">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="25fe1-169">Större ändringar i EventHub-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-169">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="25fe1-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-171">Cmdleten ”New-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-171">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-172">Använd cmdleten ”New-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="25fe1-172">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="25fe1-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-174">Cmdleten ”Get-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-174">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-175">Använd cmdleten ”Get-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="25fe1-175">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="25fe1-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-177">Cmdleten ”Set-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-177">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-178">Använd cmdleten ”Set-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="25fe1-178">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="25fe1-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-180">Cmdleten ”Remove-AzureRmEventHubNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-180">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-181">Använd cmdleten ”Remove-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="25fe1-181">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="25fe1-182">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="25fe1-182">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="25fe1-183">Cmdleten ”New-AzureRmEventHubNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-183">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-184">Använd cmdleten ”New-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="25fe1-184">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="25fe1-185">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="25fe1-185">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="25fe1-186">Cmdleten ”Get-AzureRmEventHubNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-186">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-187">Använd cmdleten ”Get-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="25fe1-187">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="25fe1-188">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="25fe1-188">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="25fe1-189">Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="25fe1-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="25fe1-190">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="25fe1-190">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="25fe1-191">Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="25fe1-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="25fe1-192">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="25fe1-192">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="25fe1-193">Egenskaperna ”Status” och ”Enabled” kommer att tas bort från NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="25fe1-193">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="25fe1-194">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="25fe1-194">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="25fe1-195">Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="25fe1-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="25fe1-196">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="25fe1-196">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="25fe1-197">Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="25fe1-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="25fe1-198">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="25fe1-198">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="25fe1-199">Egenskapen ”EventHubPath” kommer att tas bort från ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="25fe1-199">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="25fe1-200">Större ändringar i Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-200">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="25fe1-201">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-201">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="25fe1-202">Cmdleten **Add-AzureRMLogAlertRule** har gjorts inaktuell</span><span class="sxs-lookup"><span data-stu-id="25fe1-202">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="25fe1-203">Efter den 1 oktober kommer den här cmdleten inte längre att ha någon effekt eftersom den här funktionen kommer att övergå till aktivitetsloggaviseringar.</span><span class="sxs-lookup"><span data-stu-id="25fe1-203">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="25fe1-204">Mer information finns i https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="25fe1-204">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="25fe1-205">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="25fe1-205">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="25fe1-206">Cmdleten **Get-AzureRMUsage** har gjorts inaktuell</span><span class="sxs-lookup"><span data-stu-id="25fe1-206">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="25fe1-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="25fe1-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="25fe1-208">Ändring i utdata: Fältet EventChannels från EventData-objektet (som returneras av de här cmdletarna) kommer att bli inaktuellt eftersom det nu returnerar ett konstant värde (Admin, Åtgärd.)</span><span class="sxs-lookup"><span data-stu-id="25fe1-208">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="25fe1-209">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-209">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="25fe1-210">Ändring i utdata: Utdata från den här cmdleten jämnas ut. Det innebär att egenskapsfältet kommer att tas bort för att förbättra användarupplevelsen.</span><span class="sxs-lookup"><span data-stu-id="25fe1-210">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell-interactive
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

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="25fe1-211">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="25fe1-211">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="25fe1-212">Ändring i utdata: Fältet AutoscaleSettingResourceName kommer att bli inaktuellt eftersom det alltid är samma som fältet Name.</span><span class="sxs-lookup"><span data-stu-id="25fe1-212">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell-interactive
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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="25fe1-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="25fe1-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="25fe1-214">Ändring i utdata: Typen av utdata kommer att ändras så att ett enda objekt som innehåller ID för begäran och statuskod returneras.</span><span class="sxs-lookup"><span data-stu-id="25fe1-214">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell-interactive
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

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="25fe1-215">Större ändringar i Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-215">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="25fe1-216">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="25fe1-216">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="25fe1-217">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="25fe1-218">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="25fe1-218">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="25fe1-219">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="25fe1-220">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="25fe1-220">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="25fe1-221">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-221">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="25fe1-222">Större ändringar i Resources-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-222">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="25fe1-223">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="25fe1-223">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="25fe1-224">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="25fe1-225">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="25fe1-225">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="25fe1-226">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="25fe1-227">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="25fe1-227">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="25fe1-228">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="25fe1-229">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="25fe1-229">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="25fe1-230">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="25fe1-231">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="25fe1-231">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="25fe1-232">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="25fe1-233">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="25fe1-233">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="25fe1-234">Parametern ”Password” ersätts av SecureString</span><span class="sxs-lookup"><span data-stu-id="25fe1-234">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="25fe1-235">Större ändringar i ServiceBus-cmdletar</span><span class="sxs-lookup"><span data-stu-id="25fe1-235">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="25fe1-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-237">Cmdleten ”Get-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-237">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-238">Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-238">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="25fe1-239">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="25fe1-239">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="25fe1-240">Cmdleten ”Get-AzureRmServiceBusTopicKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-240">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-241">Använd cmdleten ”Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-241">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="25fe1-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-243">Cmdleten ”New-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-243">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-244">Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-244">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="25fe1-245">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="25fe1-245">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="25fe1-246">Cmdleten ”New-AzureRmServiceBusTopicKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-246">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-247">Använd cmdleten ”New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-247">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="25fe1-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-249">Cmdleten ”Remove-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-249">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-250">Använd cmdleten ”Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-250">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="25fe1-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-252">Cmdleten ”Set-AzureRmServiceBusTopicAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-252">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-253">Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-253">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="25fe1-254">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="25fe1-254">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="25fe1-255">Cmdleten ”New-AzureRmServiceBusNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-255">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-256">Använd cmdleten ”New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-256">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="25fe1-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-258">Cmdleten ”Get-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-258">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-259">Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-259">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="25fe1-260">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="25fe1-260">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="25fe1-261">Cmdleten ”Get-AzureRmServiceBusQueueKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-261">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-262">Använd cmdleten ”Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-262">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="25fe1-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-264">Cmdleten ”New-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-264">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-265">Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-265">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="25fe1-266">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="25fe1-266">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="25fe1-267">Cmdleten ”New-AzureRmServiceBusQueueKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-267">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-268">Använd cmdleten ”New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-268">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="25fe1-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-270">Cmdleten ”Remove-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-270">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-271">Använd cmdleten ”GRemove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-271">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="25fe1-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-273">Cmdleten ”Set-AzureRmServiceBusQueueAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-273">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-274">Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-274">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="25fe1-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-276">Cmdleten ”Get-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-276">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-277">Använd cmdleten ”Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-277">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="25fe1-278">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="25fe1-278">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="25fe1-279">Cmdleten ”Get-AzureRmServiceBusNamespaceKey” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-279">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-280">Använd cmdleten ”Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-280">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="25fe1-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-282">Cmdleten ”New-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-282">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-283">Använd cmdleten ”New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-283">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="25fe1-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-285">Cmdleten ”Remove-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-285">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-286">Använd cmdleten ”Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-286">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="25fe1-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="25fe1-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="25fe1-288">Cmdleten ”Set-AzureRmServiceBusNamespaceAuthorizationRule” har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="25fe1-288">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="25fe1-289">Använd cmdleten ”Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="25fe1-289">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="25fe1-290">**Typen NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="25fe1-290">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="25fe1-291">Följande egenskaper har tagits bort</span><span class="sxs-lookup"><span data-stu-id="25fe1-291">The following properties have been removed</span></span>
    - <span data-ttu-id="25fe1-292">Enabled</span><span class="sxs-lookup"><span data-stu-id="25fe1-292">Enabled</span></span>
    - <span data-ttu-id="25fe1-293">Status</span><span class="sxs-lookup"><span data-stu-id="25fe1-293">Status</span></span>
   
```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="25fe1-294">**Typen QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="25fe1-294">**Type QueueAttribute**</span></span>
- <span data-ttu-id="25fe1-295">Följande egenskaper har angetts som föråldrade:</span><span class="sxs-lookup"><span data-stu-id="25fe1-295">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="25fe1-296">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="25fe1-296">EnableBatchedOperations</span></span>
    - <span data-ttu-id="25fe1-297">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="25fe1-297">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="25fe1-298">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="25fe1-298">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="25fe1-299">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="25fe1-299">SupportOrdering</span></span>

```powershell-interactive
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
   
### <a name="type-topicattribute"></a><span data-ttu-id="25fe1-300">**Typen TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="25fe1-300">**Type TopicAttribute**</span></span>
- <span data-ttu-id="25fe1-301">Följande egenskaper har angetts som föråldrade:</span><span class="sxs-lookup"><span data-stu-id="25fe1-301">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="25fe1-302">Location</span><span class="sxs-lookup"><span data-stu-id="25fe1-302">Location</span></span>
    - <span data-ttu-id="25fe1-303">IsExpress</span><span class="sxs-lookup"><span data-stu-id="25fe1-303">IsExpress</span></span>
    - <span data-ttu-id="25fe1-304">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="25fe1-304">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="25fe1-305">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="25fe1-305">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="25fe1-306">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="25fe1-306">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="25fe1-307">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="25fe1-307">EntityAvailabilityStatus</span></span>

```powershell-interactive
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
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="25fe1-308">**Typen SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="25fe1-308">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="25fe1-309">Följande egenskaper har angetts som föråldrade</span><span class="sxs-lookup"><span data-stu-id="25fe1-309">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="25fe1-310">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="25fe1-310">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="25fe1-311">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="25fe1-311">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="25fe1-312">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="25fe1-312">IsReadOnly</span></span>
    - <span data-ttu-id="25fe1-313">Location</span><span class="sxs-lookup"><span data-stu-id="25fe1-313">Location</span></span>
   
```powershell-interactive
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