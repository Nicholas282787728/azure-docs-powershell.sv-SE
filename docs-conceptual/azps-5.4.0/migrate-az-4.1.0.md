---
title: Migreringsguide för Az 4.1.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 4.1.0 av Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: fe4a2a7c2f1b171b530eef41ac072b2029be1026
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2021
ms.locfileid: "98574168"
---
# <a name="migration-guide-for-az-410"></a>Migreringsguide för Az 4.1.0

I det här dokumentet beskrivs ändringarna mellan Az-versionerna 3.0.0 och 4.1.0.

- [Migreringsguide för Az 4.1.0](#migration-guide-for-az-410)
  - [Az.ApiManagement](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [Az.Batch](#azbatch)
    - [`Get-AzBatchApplication`, `New-AzBatchApplication`](#get-azbatchapplication-new-azbatchapplication)
    - [`Get-AzBatchComputeNode`, `New-AzBatchPool`](#get-azbatchcomputenode-new-azbatchpool)
    - [`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [Az.Compute](#azcompute)
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
  - [Az.KeyVault](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [Az.Monitor](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [Az.Network](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [Az.OperationalInsights](#azoperationalinsights)
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
  - [Az.Resources](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [Az.Storage](#azstorage)
    - [`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [`New-AzStorageTable`, `Get-AzStorageTable`](#new-azstoragetable-get-azstoragetable)
    - [`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a>Az.ApiManagement

### `Add-AzApiManagementRegion`

Typen för egenskapen `Type` av typen `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` har ändrats från `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` till `System.String`.

### `New-AzApiManagement`

- Cmdleten `New-AzApiManagement` stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.
- Parameteruppsättningen `__AllParameterSets` för cmdleten `New-AzApiManagement` har tagits bort.

### `Set-AzApiManagement`

- Cmdleten `Set-AzApiManagement` stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.
- Parameteruppsättningen `__AllParameterSets` för cmdleten `Set-AzApiManagement` har tagits bort.

### `Get-AzApiManagementProperty`

Cmdleten `Get-AzApiManagementProperty` har ersatts av `Get-AzApiManagementNamedValue`.

### `New-AzApiManagementProperty`

Cmdleten `New-AzApiManagementProperty` har ersatts av `New-AzApiManagementNamedValue`.

### `Remove-AzApiManagementProperty`

Cmdleten `Remove-AzApiManagementProperty` har ersatts av `Remove-AzApiManagementNamedValue`.

### `Set-AzApiManagementProperty`

Cmdleten `Set-AzApiManagementProperty` har ersatts av `Set-AzApiManagementNamedValue`.

## <a name="azbatch"></a>Az.Batch

### <a name="get-azbatchapplication-new-azbatchapplication"></a>`Get-AzBatchApplication`, `New-AzBatchApplication`

Egenskapen `ApplicationPackages` av typen `Microsoft.Azure.Commands.Batch.Models.PSApplication` har tagits bort.

### <a name="get-azbatchcomputenode-new-azbatchpool"></a>`Get-AzBatchComputeNode`, `New-AzBatchPool`

Egenskapen `PublicIPs` av typen `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` har tagits bort

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a>`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`

Typen för egenskapen `StorageUrlExpiry` av typen `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` har ändrats från `System.DateTime` till `System.DateTime?`.

## <a name="azcompute"></a>Az.Compute

### `Remove-AzVmssDiagnosticsExtension`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Get-AzVMImage`

- Cmdleten `Get-AzVMImage` stöder inte längre parametern `FilterExpression` och inget alias hittades för det ursprungliga parameternamnet.
- Parameteruppsättningen `ListVMImage` för cmdleten `Get-AzVMImage` har tagits bort.

### `New-AzVMConfig`

- Cmdleten `New-AzVMConfig` stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.
- Parameteruppsättningen `AssignIdentityParameterSet` för cmdleten `New-AzVMConfig` har tagits bort.

### `Update-AzVM`

- Cmdleten `Update-AzVM` stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.
- Parameteruppsättningen `AssignIdentityParameterSet` för cmdleten `Update-AzVM` har tagits bort.

### `New-AzProximityPlacementGroup`

- Den generiska typen för egenskapen `VirtualMachines`, `VirtualMachineScaleSets` och `AvailabilitySets` har ändrats från `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` till `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- Egenskapen `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` och `AvailabilitySetsColocationStatus` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` har tagits bort.

#### <a name="before"></a>Före

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

#### <a name="after"></a>Efter

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

- Den generiska typen för egenskapen `VirtualMachines`, `VirtualMachineScaleSets` och `AvailabilitySets` har ändrats från `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` till `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- Egenskapen `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` och `AvailabilitySetsColocationStatus` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` har tagits bort.

#### <a name="before"></a>Före

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

#### <a name="after"></a>Efter

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

- Den generiska typen för egenskapen `VirtualMachines`, `VirtualMachineScaleSets` och `AvailabilitySets` har ändrats från `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` till `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- Egenskapen `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` och `AvailabilitySetsColocationStatus` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` har tagits bort.

#### <a name="before"></a>Före

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

#### <a name="after"></a>Efter

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

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssDataDisk`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssExtension`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssNetworkInterfaceConfiguration`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssSecret`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssSshPublicKey`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssWinRMListener`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `New-AzVmssConfig`

- Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.
- Stöder inte längre parametern `AutomaticRepairMaxInstanceRepairsPercent` och inget alias hittades för det ursprungliga parameternamnet.
- Stöder inte längre parametern `AssignIdentity` och inget alias hittades för det ursprungliga parameternamnet.
- Parameteruppsättningen `__AllParameterSets` har tagits bort.
- Parameteruppsättningen `ExplicitIdentityParameterSet` har tagits bort.
- Parameteruppsättningen `AssignIdentityParameterSet` har tagits bort.

### `Remove-AzVmssDataDisk`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Remove-AzVmssExtension`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Remove-AzVmssNetworkInterfaceConfiguration`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssBootDiagnostic`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssOsProfile`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssRollingUpgradePolicy`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssStorageProfile`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `New-AzVmss`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Repair-AzVmssServiceFabricUpdateDomain`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Get-AzVmss`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssOrchestrationServiceState`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Update-AzVmss`

- Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.
- Stöder inte längre parametern `AutomaticRepairMaxInstanceRepairsPercent` och inget alias hittades för det ursprungliga parameternamnet.
- Parameteruppsättningen `__AllParameterSets` har tagits bort.
- Parameteruppsättningen `ExplicitIdentityParameterSet` har tagits bort.

### `Add-AzVmssDiagnosticsExtension`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Disable-AzVmssDiskEncryption`

Typen för egenskapen `AutomaticRepairsPolicy` av typen `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` har ändrats från `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` till `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

## <a name="azkeyvault"></a>Az.KeyVault

### `New-AzKeyVaultCertificateOrganizationDetail`

Aliaset `New-AzKeyVaultCertificateOrganizationDetails` har tagits bort. Använd `New-AzKeyVaultCertificateOrganizationDetail`.

#### <a name="before"></a>Före

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a>Efter

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

Aliaset `New-AzKeyVaultCertificateAdministratorDetails` har tagits bort. Använd `New-AzKeyVaultCertificateAdministratorDetail`.

#### <a name="before"></a>Före

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a>Efter

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

`-EnableSoftDelete` tas bort eftersom mjuk borttagning är aktiverat som standard. Använd `-DisableSoftDelete` om du inte vill använda det här beteendet.

#### <a name="before"></a>Före

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a>Efter

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a>Az.Monitor

### `Add-AzLogProfile`

Typen för egenskapen `RetentionPolicy` av typen `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` har ändrats från `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` till `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.

### `Get-AzLogProfile`

Typen för egenskapen `RetentionPolicy` av typen `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` har ändrats från `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` till `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.

### `New-AzMetricAlertRuleV2Criteria`

Parameteruppsättningen `__AllParameterSets` för cmdleten `New-AzMetricAlertRuleV2Criteria` har tagits bort.

## <a name="aznetwork"></a>Az.Network

### `Get-AzNetworkWatcherConnectionMonitor`

Den generiska typen för egenskapen `RoundTripTimeMs` har ändrats från `System.Nullable1[System.Int32]` till `System.Nullable1[System.Double]`.

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

Den generiska typen för parametern `SuccessThresholdRoundTripTimeMs` har ändrats från `System.Nullable1[System.Int32]` till `System.Nullable1[System.Double]`.

## <a name="azoperationalinsights"></a>Az.OperationalInsights

### `Get-AzOperationalInsightsDataSource`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `New-AzOperationalInsightsApplicationInsightsDataSource`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `New-AzOperationalInsightsAzureActivityLogDataSource`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `New-AzOperationalInsightsCustomLogDataSource`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `New-AzOperationalInsightsLinuxSyslogDataSource`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `New-AzOperationalInsightsWindowsEventDataSource`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Remove-AzOperationalInsightsDataSource`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Disable-AzOperationalInsightsIISLogCollection`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Enable-AzOperationalInsightsIISLogCollection`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Get-AzOperationalInsightsSavedSearch`

Egenskapen `Metadata` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` har tagits bort.

### `Get-AzOperationalInsightsSavedSearchResult`

Cmdleten `Get-AzOperationalInsightsSavedSearchResult` stöds inte längre av SDK och har tagits bort.

### `Get-AzOperationalInsightsSearchResult`

Cmdleten `Get-AzOperationalInsightsSearchResult` stöds inte längre av SDK och har tagits bort.

### `Get-AzOperationalInsightsStorageInsight`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `New-AzOperationalInsightsStorageInsight`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Remove-AzOperationalInsightsStorageInsight`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Set-AzOperationalInsightsStorageInsight`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Get-AzOperationalInsightsLinkTarget`

Cmdleten `Get-AzOperationalInsightsLinkTarget` stöds inte längre av SDK och har tagits bort.

### `Get-AzOperationalInsightsWorkspace`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `New-AzOperationalInsightsWorkspace`

- Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.
- Cmdleten `New-AzOperationalInsightsWorkspace` stöder inte längre parametern `CustomerId` och inget alias hittades för det ursprungliga parameternamnet.
- Parameteruppsättningen `__AllParameterSets` för cmdleten `New-AzOperationalInsightsWorkspace` har tagits bort.

### `Set-AzOperationalInsightsWorkspace`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

### `Invoke-AzOperationalInsightsQuery`

Egenskapen `PortalUrl` av typen `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` har tagits bort.

## <a name="azresources"></a>Az.Resources

### `Get-AzDeploymentScript`

Typen för egenskapen `Status` för typen `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` har ändrats från `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` till `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Get-AzDeploymentScriptLog`

Typen för egenskapen `Status` av typen `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` har ändrats från `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` till `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Save-AzDeploymentScriptLog`

Typen för egenskapen `Status` för typen `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` har ändrats från `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` till `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

Parametern `TenantLevel` har tagits bort

### `Get-AzPolicyAlias`

Den generiska typen för egenskapen `Aliases` har ändrats från `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` till `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.

### `New-AzPolicyAssignment`

- Cmdleten `New-AzPolicyAssignment` stöder inte längre typen `System.Management.Automation.PSObject` för parametern `PolicyDefinition`.
- Cmdleten `New-AzPolicyAssignment` stöder inte längre typen `System.Management.Automation.PSObject` för parametern `PolicySetDefinition`.

### `Remove-AzDeploymentScript`

Typen för egenskapen `Status` av typen `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` har ändrats från `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` till `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

## <a name="azstorage"></a>Az.Storage

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a>`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`

NetWorkRule DefaultAction-värdet har ändrats från: Tillåt = 1, Neka = 0, till: Tillåt = 0, Neka = 1.

### <a name="new-azstoragetable-get-azstoragetable"></a>`New-AzStorageTable`, `Get-AzStorageTable`

Två egenskaper har tagits bort för utdataobjektet AzureStorageTable.CloudTable.ServiceClient: ConnectionPolicy, ConsistencyLevel.

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a>`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`

Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir den underordnade egenskapen ”CloudFile” i den nya utmatningen

#### <a name="before"></a>Före

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a>Efter

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a>`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`

Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir den underordnade egenskapen ”CloudFileDirectory” i den nya utmatningen

#### <a name="before"></a>Före

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>Efter

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a>`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`

Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir den underordnade egenskapen ”CloudFileShare” i den nya utmatningen

#### <a name="before"></a>Före

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a>Efter

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir den underordnade egenskapen ”CloudFileShare.Properties” i den nya utmatningen

#### <a name="before"></a>Före

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a>Efter

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

Du kan inte längre mata in -Path från pipelinen med typmatchning (sträng) när du tar bort underordnade filkataloger med det överordnade katalogobjektet och -Path.

#### <a name="before"></a>Före

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>Efter

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
