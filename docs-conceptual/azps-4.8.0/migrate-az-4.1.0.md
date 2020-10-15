---
title: Migreringsguide för Az 4.1.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 4.1.0 av Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c64541beb5eb0d3db38932fb3915de865919641b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002163"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="3ef91-103">Migreringsguide för Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="3ef91-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="3ef91-104">I det här dokumentet beskrivs ändringarna mellan Az-versionerna 3.0.0 och 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="3ef91-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="3ef91-105">Migreringsguide för Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="3ef91-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="3ef91-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef91-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="3ef91-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef91-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="3ef91-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="3ef91-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="3ef91-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="3ef91-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="3ef91-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="3ef91-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="3ef91-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef91-111">Az.Compute</span></span>](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [<span data-ttu-id="3ef91-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef91-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="3ef91-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef91-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="3ef91-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef91-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="3ef91-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef91-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [<span data-ttu-id="3ef91-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef91-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="3ef91-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef91-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="3ef91-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="3ef91-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="3ef91-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="3ef91-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="3ef91-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="3ef91-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="3ef91-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="3ef91-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="3ef91-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="3ef91-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="3ef91-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3ef91-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="3ef91-124">Typen för egenskapen `Type` av typen `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` har ändrats från `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` till `System.String`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="3ef91-125">Cmdleten `New-AzApiManagement` stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="3ef91-126">Parameteruppsättningen `__AllParameterSets` för cmdleten `New-AzApiManagement` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="3ef91-127">Cmdleten `Set-AzApiManagement` stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="3ef91-128">Parameteruppsättningen `__AllParameterSets` för cmdleten `Set-AzApiManagement` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="3ef91-129">Cmdleten `Get-AzApiManagementProperty` har ersatts av `Get-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="3ef91-130">Cmdleten `New-AzApiManagementProperty` har ersatts av `New-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="3ef91-131">Cmdleten `Remove-AzApiManagementProperty` har ersatts av `Remove-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="3ef91-132">Cmdleten `Set-AzApiManagementProperty` har ersatts av `Set-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="3ef91-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3ef91-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="3ef91-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="3ef91-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="3ef91-135">Egenskapen `ApplicationPackages` av typen `Microsoft.Azure.Commands.Batch.Models.PSApplication` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="3ef91-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="3ef91-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="3ef91-137">Egenskapen `PublicIPs` av typen `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="3ef91-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="3ef91-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="3ef91-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="3ef91-139">Typen för egenskapen `StorageUrlExpiry` av typen `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` har ändrats från `System.DateTime` till `System.DateTime?`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="3ef91-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3ef91-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="3ef91-141">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="3ef91-142">Cmdleten `Get-AzVMImage` stöder inte längre parametern `FilterExpression` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="3ef91-143">Parameteruppsättningen `ListVMImage` för cmdleten `Get-AzVMImage` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="3ef91-144">Cmdleten `New-AzVMConfig` stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="3ef91-145">Parameteruppsättningen `AssignIdentityParameterSet` för cmdleten `New-AzVMConfig` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="3ef91-146">Cmdleten `Update-AzVM` stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="3ef91-147">Parameteruppsättningen `AssignIdentityParameterSet` för cmdleten `Update-AzVM` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="3ef91-148">Den generiska typen för egenskapen `VirtualMachines`, `VirtualMachineScaleSets` och `AvailabilitySets` har ändrats från `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` till `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="3ef91-149">Egenskapen `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` och `AvailabilitySetsColocationStatus` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-150">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-150">Before</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="3ef91-151">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-151">After</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- <span data-ttu-id="3ef91-152">Den generiska typen för egenskapen `VirtualMachines`, `VirtualMachineScaleSets` och `AvailabilitySets` har ändrats från `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` till `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="3ef91-153">Egenskapen `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` och `AvailabilitySetsColocationStatus` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-154">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-154">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="3ef91-155">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-155">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- <span data-ttu-id="3ef91-156">Den generiska typen för egenskapen `VirtualMachines`, `VirtualMachineScaleSets` och `AvailabilitySets` har ändrats från `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` till `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="3ef91-157">Egenskapen `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` och `AvailabilitySetsColocationStatus` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-158">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-158">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="3ef91-159">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-159">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

<span data-ttu-id="3ef91-160">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="3ef91-161">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="3ef91-162">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="3ef91-163">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="3ef91-164">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="3ef91-165">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="3ef91-166">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="3ef91-167">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="3ef91-168">Stöder inte längre parametern `AutomaticRepairMaxInstanceRepairsPercent` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="3ef91-169">Stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="3ef91-170">Parameteruppsättningen `__AllParameterSets` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="3ef91-171">Parameteruppsättningen `ExplicitIdentityParameterSet` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="3ef91-172">Parameteruppsättningen `AssignIdentityParameterSet` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="3ef91-173">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="3ef91-174">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="3ef91-175">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="3ef91-176">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="3ef91-177">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="3ef91-178">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="3ef91-179">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="3ef91-180">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="3ef91-181">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="3ef91-182">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="3ef91-183">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="3ef91-184">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="3ef91-185">Stöder inte längre parametern `AutomaticRepairMaxInstanceRepairsPercent` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="3ef91-186">Parameteruppsättningen `__AllParameterSets` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="3ef91-187">Parameteruppsättningen `ExplicitIdentityParameterSet` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="3ef91-188">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="3ef91-189">Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="3ef91-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3ef91-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="3ef91-191">Aliaset `New-AzKeyVaultCertificateOrganizationDetails` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="3ef91-192">Använd `New-AzKeyVaultCertificateOrganizationDetail`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-193">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="3ef91-194">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="3ef91-195">Aliaset `New-AzKeyVaultCertificateAdministratorDetails` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="3ef91-196">Använd `New-AzKeyVaultCertificateAdministratorDetail`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-197">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="3ef91-198">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="3ef91-199">`-EnableSoftDelete` tas bort eftersom mjuk borttagning är aktiverat som standard.</span><span class="sxs-lookup"><span data-stu-id="3ef91-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="3ef91-200">Använd `-DisableSoftDelete` om du inte vill använda det här beteendet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-201">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="3ef91-202">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="3ef91-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3ef91-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="3ef91-204">Typen för egenskapen `RetentionPolicy` av typen `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` har ändrats från `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` till `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="3ef91-205">Typen för egenskapen `RetentionPolicy` av typen `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` har ändrats från `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` till `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="3ef91-206">Parameteruppsättningen `__AllParameterSets` för cmdleten `New-AzMetricAlertRuleV2Criteria` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="3ef91-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3ef91-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="3ef91-208">Den generiska typen för egenskapen `RoundTripTimeMs` har ändrats från `System.Nullable1[System.Int32]` till `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="3ef91-209">Den generiska typen för parametern `SuccessThresholdRoundTripTimeMs` har ändrats från `System.Nullable1[System.Int32]` till `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="3ef91-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3ef91-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="3ef91-211">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="3ef91-212">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="3ef91-213">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="3ef91-214">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="3ef91-215">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="3ef91-216">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="3ef91-217">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="3ef91-218">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="3ef91-219">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="3ef91-220">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="3ef91-221">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="3ef91-222">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="3ef91-223">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="3ef91-224">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="3ef91-225">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="3ef91-226">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="3ef91-227">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="3ef91-228">Egenskapen `Metadata` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="3ef91-229">Cmdleten `Get-AzOperationalInsightsSavedSearchResult` stöds inte längre av SDK och har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="3ef91-230">Cmdleten `Get-AzOperationalInsightsSearchResult` stöds inte längre av SDK och har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="3ef91-231">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="3ef91-232">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="3ef91-233">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="3ef91-234">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="3ef91-235">Cmdleten `Get-AzOperationalInsightsLinkTarget` stöds inte längre av SDK och har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="3ef91-236">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="3ef91-237">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="3ef91-238">Cmdleten `New-AzOperationalInsightsWorkspace` stöder inte längre parametern `CustomerId` och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="3ef91-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="3ef91-239">Parameteruppsättningen `__AllParameterSets` för cmdleten `New-AzOperationalInsightsWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="3ef91-240">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="3ef91-241">Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3ef91-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="3ef91-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3ef91-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="3ef91-243">Typen för egenskapen `Status` för typen `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` har ändrats från `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` till `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="3ef91-244">Typen för egenskapen `Status` av typen `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` har ändrats från `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` till `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="3ef91-245">Typen för egenskapen `Status` för typen `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` har ändrats från `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` till `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="3ef91-246">Parametern `TenantLevel` har tagits bort</span><span class="sxs-lookup"><span data-stu-id="3ef91-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="3ef91-247">Den generiska typen för egenskapen `Aliases` har ändrats från `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` till `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="3ef91-248">Cmdleten `New-AzPolicyAssignment` stöder inte längre typen `System.Management.Automation.PSObject` för parametern `PolicyDefinition`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="3ef91-249">Cmdleten `New-AzPolicyAssignment` stöder inte längre typen `System.Management.Automation.PSObject` för parametern `PolicySetDefinition`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="3ef91-250">Typen för egenskapen `Status` av typen `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` har ändrats från `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` till `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="3ef91-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="3ef91-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3ef91-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="3ef91-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="3ef91-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="3ef91-253">NetWorkRule DefaultAction-värdet har ändrats från: Tillåt = 1, Neka = 0, till: Tillåt = 0, Neka = 1.</span><span class="sxs-lookup"><span data-stu-id="3ef91-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="3ef91-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="3ef91-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="3ef91-255">Två egenskaper har tagits bort för utdataobjektet AzureStorageTable.CloudTable.ServiceClient: ConnectionPolicy, ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="3ef91-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="3ef91-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="3ef91-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="3ef91-257">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir den underordnade egenskapen ”CloudFile” i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="3ef91-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-258">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="3ef91-259">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="3ef91-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="3ef91-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="3ef91-261">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir den underordnade egenskapen ”CloudFileDirectory” i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="3ef91-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-262">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="3ef91-263">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="3ef91-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="3ef91-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="3ef91-265">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir den underordnade egenskapen ”CloudFileShare” i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="3ef91-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-266">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="3ef91-267">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="3ef91-268">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir den underordnade egenskapen ”CloudFileShare.Properties” i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="3ef91-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-269">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="3ef91-270">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-270">After</span></span>

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

<span data-ttu-id="3ef91-271">Du kan inte längre mata in -Path från pipelinen med typmatchning (sträng) när du tar bort underordnade filkataloger med det överordnade katalogobjektet och -Path.</span><span class="sxs-lookup"><span data-stu-id="3ef91-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="3ef91-272">Före</span><span class="sxs-lookup"><span data-stu-id="3ef91-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="3ef91-273">Efter</span><span class="sxs-lookup"><span data-stu-id="3ef91-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
