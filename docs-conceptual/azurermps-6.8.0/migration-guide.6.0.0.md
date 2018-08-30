---
title: Icke-bakåtkompatibla ändringar för Microsoft Azure PowerShell 6.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i version 6 av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 5/1/2018
ms.openlocfilehash: 4f9c99152fd6ddc23aec005c8e8957e545e65246
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117627"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="ea086-103">Icke-bakåtkompatibla ändringar för Microsoft Azure PowerShell 6.0.0</span><span class="sxs-lookup"><span data-stu-id="ea086-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="ea086-104">Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ea086-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ea086-105">I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet.</span><span class="sxs-lookup"><span data-stu-id="ea086-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="ea086-106">Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.</span><span class="sxs-lookup"><span data-stu-id="ea086-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="ea086-107">Innehållsförteckning</span><span class="sxs-lookup"><span data-stu-id="ea086-107">Table of Contents</span></span>

- [<span data-ttu-id="ea086-108">Allmänna icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ea086-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="ea086-109">Lägsta version av PowerShell som krävs har höjts till 5.0</span><span class="sxs-lookup"><span data-stu-id="ea086-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="ea086-110">Funktionen för att automatiskt spara kontext har aktiverats som standard</span><span class="sxs-lookup"><span data-stu-id="ea086-110">Context autosaved enabled by default</span></span>](#context-autosaved-enabled-by-default)
    - [<span data-ttu-id="ea086-111">Borttagning av alias för taggar</span><span class="sxs-lookup"><span data-stu-id="ea086-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="ea086-112">Icke-bakåtkompatibla ändringar i AzureRM.Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="ea086-113">Icke-bakåtkompatibla ändringar i AzureRM.DataLakeStore-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="ea086-114">Icke-bakåtkompatibla ändringar i AzureRM.Dns-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="ea086-115">Icke-bakåtkompatibla ändringar i AzureRM.Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="ea086-116">Icke-bakåtkompatibla ändringar i AzureRM.KeyVault-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="ea086-117">Icke-bakåtkompatibla ändringar i AzureRM.Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="ea086-118">Icke-bakåtkompatibla ändringar i AzureRM.RedisCache-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="ea086-119">Icke-bakåtkompatibla ändringar i AzureRM.Resources-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="ea086-120">Icke-bakåtkompatibla ändringar i AzureRM.Storage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="ea086-121">Borttagna moduler</span><span class="sxs-lookup"><span data-stu-id="ea086-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="ea086-122">Allmänna icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="ea086-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="ea086-123">Lägsta version av PowerShell som krävs har höjts till 5.0</span><span class="sxs-lookup"><span data-stu-id="ea086-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="ea086-124">Tidigare krävde Azure PowerShell _minst_ version 3.0 av PowerShell för att köra en cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea086-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="ea086-125">Det här kravet kommer att höjas till version 5.0 av PowerShell framöver.</span><span class="sxs-lookup"><span data-stu-id="ea086-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="ea086-126">Information om hur du uppgraderar till PowerShell 5.0 finns i [den här tabellen](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="ea086-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="ea086-127">Funktionen för att automatiskt spara kontext har aktiverats som standard</span><span class="sxs-lookup"><span data-stu-id="ea086-127">Context autosave enabled by default</span></span>

<span data-ttu-id="ea086-128">Automatiskt sparande av kontext är lagring av inloggningsinformation för Azure som kan användas mellan nya och olika PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="ea086-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="ea086-129">Mer information om att spara kontext automatiskt finns i [det här dokumentet](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="ea086-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="ea086-130">Tidigare var funktionen för att automatiskt spara kontext inaktiverad som standard, vilket innebar att användarnas autentiseringsinformation inte lagrades mellan sessioner förrän de körde cmdleten `Enable-AzureRmContextAutosave` för att aktivera kontextpersistens.</span><span class="sxs-lookup"><span data-stu-id="ea086-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="ea086-131">Funktionen för att automatiskt spara kontext kommer att vara aktiverad som standard hädanefter, vilket innebär att kontexten kommer att sparas automatiskt för användare _som inte har sparat några inställningar för automatiskt sparande av kontext_ nästa gång de loggar in.</span><span class="sxs-lookup"><span data-stu-id="ea086-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="ea086-132">Användarna kan välja bort den här funktionen med hjälp av cmdleten `Disable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="ea086-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="ea086-133">_Obs_: användare som tidigare har inaktiverat automatiskt sparande av kontext och användare som har aktiverat funktionen och har befintliga kontexter påverkas inte av den här ändringen</span><span class="sxs-lookup"><span data-stu-id="ea086-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="ea086-134">Borttagning av alias för taggar</span><span class="sxs-lookup"><span data-stu-id="ea086-134">Removal of Tags alias</span></span>

<span data-ttu-id="ea086-135">Alias `Tags` för parametern `Tag` har tagits bort för flera cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ea086-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="ea086-136">Nedan visas en lista med moduler (och de motsvarande cmdletarna) som påverkas av det här:</span><span class="sxs-lookup"><span data-stu-id="ea086-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="ea086-137">Icke-bakåtkompatibla ändringar i AzureRM.Compute-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="ea086-138">**Övrigt**</span><span class="sxs-lookup"><span data-stu-id="ea086-138">**Miscellaneous**</span></span>
- <span data-ttu-id="ea086-139">SKU-namnegenskapen som är kapslad i typerna `PSDisk` och `PSSnapshot` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="ea086-140">Typegenskapen för lagringskonton som är kapslad i typerna `PSVirtualMachine`, `PSVirtualMachineScaleSet` och `PSImage` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="ea086-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="ea086-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="ea086-142">Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="ea086-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="ea086-144">Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="ea086-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="ea086-146">Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="ea086-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="ea086-148">Parametern `Managed` har tagits bort och ersatts av `Sku`</span><span class="sxs-lookup"><span data-stu-id="ea086-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="ea086-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="ea086-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="ea086-150">Godkända värden för parametern `SkuName` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="ea086-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="ea086-152">Godkända värden för parametern `SkuName` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="ea086-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="ea086-154">Godkända värden för parametern `SkuName` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="ea086-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="ea086-156">Godkända värden för parametern `SkuName` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="ea086-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="ea086-158">Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="ea086-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="ea086-160">Parametern `DisableWAD` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="ea086-161">Windows Azure Diagnostics är inaktiverat som standard</span><span class="sxs-lookup"><span data-stu-id="ea086-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="ea086-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="ea086-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="ea086-163">Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="ea086-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="ea086-165">Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="ea086-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="ea086-167">Godkända värden för parametern `ManagedDisk` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="ea086-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="ea086-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="ea086-169">Godkända värden för parametern `ManagedDiskStorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="ea086-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="ea086-170">Icke-bakåtkompatibla ändringar i AzureRM.DataLakeStore-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="ea086-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="ea086-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="ea086-172">Parametrarna `PerFileThreadCount` och `ConcurrentFileCount` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ea086-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="ea086-173">Använd parametern `Concurrency` hädanefter</span><span class="sxs-lookup"><span data-stu-id="ea086-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="ea086-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="ea086-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="ea086-175">Parametrarna `PerFileThreadCount` och `ConcurrentFileCount` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ea086-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="ea086-176">Använd parametern `Concurrency` hädanefter</span><span class="sxs-lookup"><span data-stu-id="ea086-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="ea086-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="ea086-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="ea086-178">Parametern `Clean` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-178">Parameter `Clean` was removed</span></span>

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="ea086-179">Icke-bakåtkompatibla ändringar i AzureRM.Dns-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="ea086-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="ea086-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="ea086-181">Parametern `Force` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="ea086-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="ea086-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="ea086-183">Parametern `Force` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="ea086-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="ea086-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="ea086-185">Parametern `Force` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="ea086-186">Icke-bakåtkompatibla ändringar i AzureRM.Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="ea086-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="ea086-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="ea086-188">Parameteralias `AutoscaleProfiles` och `Notifications` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="ea086-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="ea086-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="ea086-190">Parameteralias `Categories` och `Locations` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="ea086-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="ea086-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="ea086-192">Parameteralias `Actions` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="ea086-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="ea086-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="ea086-194">Parameteralias `Actions` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="ea086-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="ea086-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="ea086-196">Parameteralias `MaxRecords` och `MaxEvents` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="ea086-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="ea086-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="ea086-198">Parameteralias `MetricNames` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="ea086-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="ea086-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="ea086-200">Parameteralias `CustomEmails` och `SendToServiceOwners` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="ea086-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="ea086-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="ea086-202">Parameteralias `Properties` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="ea086-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="ea086-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="ea086-204">Parameteralias `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` och `Webhooks` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="ea086-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="ea086-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="ea086-206">Parameteralias `Rules`, `ScheduleDays`, `ScheduleHours` och `ScheduleMinutes` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="ea086-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="ea086-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="ea086-208">Parameteralias `Properties` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="ea086-209">Icke-bakåtkompatibla ändringar i AzureRM.KeyVault-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="ea086-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="ea086-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="ea086-211">Parametern `CertificatePolicy` har blivit obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ea086-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="ea086-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="ea086-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="ea086-213">Cmdleten accepterar inte längre enskilda parametrar som utgör åtkomst-token. I stället ersätter cmdleten explicita tokenparametrar, som t. ex. `Service` eller `Permissions` med en allmän `TemplateUri`-parameter som motsvarar en exempel-åtkomsttoken och som definierats någon annanstans (förmodligen med Storage PowerShell-cmdletar eller sammanställts manuellt enligt Storage-dokumentationen.) Cmdleten behåller parametern `ValidityPeriod`.</span><span class="sxs-lookup"><span data-stu-id="ea086-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="ea086-214">Mer information om att sammanställa token för delad åtkomst för Azure Storage hittar du på följande dokumentationssidor:</span><span class="sxs-lookup"><span data-stu-id="ea086-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- <span data-ttu-id="ea086-215">[Skapa en tjänst-SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)</span><span class="sxs-lookup"><span data-stu-id="ea086-215">[Constructing a Service SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)</span></span>
- <span data-ttu-id="ea086-216">[Skapa en konto-SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)</span><span class="sxs-lookup"><span data-stu-id="ea086-216">[Constructing an Account SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)</span></span>

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="ea086-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="ea086-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="ea086-218">Parametern `IssuerProvider` har blivit obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ea086-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="ea086-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="ea086-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="ea086-220">Resultatet av den här cmdleten har ändrats från `CertificateBundle` till `PSKeyVaultCertificate`.</span><span class="sxs-lookup"><span data-stu-id="ea086-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="ea086-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="ea086-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="ea086-222">`ResourceGroupName` har tagits bort från parameteruppsättningen `InputObject` och hämtas istället från `InputObject`-parameterns `ResourceId`-egenskap.</span><span class="sxs-lookup"><span data-stu-id="ea086-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="ea086-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="ea086-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="ea086-224">Behörigheten `all` har tagits bort från `PermissionsToKeys`, `PermissionsToSecrets` och `PermissionsToCertificates`.</span><span class="sxs-lookup"><span data-stu-id="ea086-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="ea086-225">**Allmänt**</span><span class="sxs-lookup"><span data-stu-id="ea086-225">**General**</span></span>
- <span data-ttu-id="ea086-226">Egenskapen `ValueFromPipelineByPropertyName` togs bort från alla cmdletar där överföring genom `InputObject` har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="ea086-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="ea086-227">Cmdletarna som påverkas är:</span><span class="sxs-lookup"><span data-stu-id="ea086-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="ea086-228">`ConfirmImpact`-nivåerna har tagits bort från alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ea086-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="ea086-229">Cmdletarna som påverkas är:</span><span class="sxs-lookup"><span data-stu-id="ea086-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="ea086-230">`IKeyVaultDataServiceClient` har uppdaterats så att alla certifikatåtgärder returnerar PSTypes istället för SDK-typer.</span><span class="sxs-lookup"><span data-stu-id="ea086-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="ea086-231">Det här omfattar:</span><span class="sxs-lookup"><span data-stu-id="ea086-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="ea086-232">Icke-bakåtkompatibla ändringar i AzureRM.Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="ea086-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="ea086-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="ea086-234">Parametern `ProbeEnabled` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="ea086-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="ea086-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="ea086-236">Parameteralias `AlloowGatewayTransit` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="ea086-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="ea086-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="ea086-238">Parametern `ProbeEnabled` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="ea086-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="ea086-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="ea086-240">Parametern `ProbeEnabled` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="ea086-241">Icke-bakåtkompatibla ändringar i AzureRM.RedisCache-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="ea086-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="ea086-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="ea086-243">Parametrarna `Subnet` och `VirtualNetwork` har tagits bort och ersatts av `SubnetId`</span><span class="sxs-lookup"><span data-stu-id="ea086-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="ea086-244">Parametern `RedisVersion` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="ea086-245">Parametern `MaxMemoryPolicy` har tagits bort och ersatts av `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="ea086-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="ea086-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="ea086-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="ea086-247">Parametern `MaxMemoryPolicy` har tagits bort och ersatts av `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="ea086-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="ea086-248">Icke-bakåtkompatibla ändringar i AzureRM.Resources-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="ea086-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="ea086-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="ea086-250">Den här cmdleten har tagits bort och funktionen har flyttats till `Get-AzureRmResource`</span><span class="sxs-lookup"><span data-stu-id="ea086-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="ea086-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="ea086-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="ea086-252">Den här cmdleten har tagits bort och funktionen har flyttats till `Get-AzureRmResourceGroup`</span><span class="sxs-lookup"><span data-stu-id="ea086-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="ea086-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="ea086-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="ea086-254">Parametern `AtScopeAndBelow` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ea086-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="ea086-255">Icke-bakåtkompatibla ändringar i AzureRM.Storage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="ea086-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="ea086-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="ea086-257">Parametern `EnableEncryptionService` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="ea086-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="ea086-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="ea086-259">Parametrarna `EnableEncryptionService` och `DisableEncryptionService` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="ea086-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="ea086-260">Borttagna moduler</span><span class="sxs-lookup"><span data-stu-id="ea086-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="ea086-261">Serverhanteringsverktyget [togs ur bruk förra året](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/) och därför togs den motsvarande modulen för SMT, `AzureRM.ServerManagement`, bort från `AzureRM` och kommer inte att levereras i framtiden.</span><span class="sxs-lookup"><span data-stu-id="ea086-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="ea086-262">Modulen `AzureRM.SiteRecovery` ersätts av `AzureRM.RecoveryServices.SiteRecovery`, som är en funktionell överordnad uppsättning av modulen `AzureRM.SiteRecovery` och som innehåller en ny uppsättning motsvarande cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ea086-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="ea086-263">En fullständig lista över mappningar från gamla till nya cmdletar finns nedan:</span><span class="sxs-lookup"><span data-stu-id="ea086-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="ea086-264">Inaktuella cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="ea086-265">Motsvarande cmdletar</span><span class="sxs-lookup"><span data-stu-id="ea086-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="ea086-266">Alias</span><span class="sxs-lookup"><span data-stu-id="ea086-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
