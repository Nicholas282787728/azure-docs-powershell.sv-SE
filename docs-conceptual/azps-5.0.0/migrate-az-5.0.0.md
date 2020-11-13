---
title: Migreringsguide för Az 5.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 5.0.0 av Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410068"
---
# <a name="migration-guide-for-az-500"></a>Migreringsguide för Az 5.0.0

I det här dokumentet beskrivs ändringarna mellan Az-versionerna 4.0.0 och 5.0.0.

- [Migreringsguide för Az 5.0.0](#migration-guide-for-az-500)
  - [Az.Aks](#azaks)
    - [New-AzAksCluster](#new-azakscluster)
    - [Set-AzAksCluster](#set-azakscluster)
  - [Az.ContainerRegistry](#azcontainerregistry)
    - [New-AzContainerRegistry](#new-azcontainerregistry)
  - [Az.Functions](#azfunctions)
    - [Get-AzFunctionApp](#get-azfunctionapp)
    - [New-AzFunctionApp](#new-azfunctionapp)
  - [Az.KeyVault](#azkeyvault)
    - [New-AzKeyVault](#new-azkeyvault)
    - [Update-AzKeyVault](#update-azkeyvault)
    - [Get-AzKeyVaultSecret](#get-azkeyvaultsecret)
  - [Az.ManagedServices](#azmanagedservices)
    - [Get-AzManagedServicesDefinition](#get-azmanagedservicesdefinition)
    - [New-AzManagedServicesAssignment](#new-azmanagedservicesassignment)
    - [Remove-AzManagedServicesAssignment](#remove-azmanagedservicesassignment)
    - [Remove-AzManagedServicesDefinition](#remove-azmanagedservicesdefinition)
  - [Az.ResourceManager](#azresourcemanager)
    - [Get-AzManagementGroupDeployment](#get-azmanagementgroupdeployment)
    - [Get-AzManagementGroupDeploymentOperation](#get-azmanagementgroupdeploymentoperation)
    - [Get-AzDeployment](#get-azdeployment)
    - [Get-AzDeploymentOperation](#get-azdeploymentoperation)
    - [Get-AzDeploymentWhatIfResult](#get-azdeploymentwhatifresult)
    - [Get-AzTenantDeployment](#get-aztenantdeployment)
    - [Get-AzTenantDeploymentOperation](#get-aztenantdeploymentoperation)
    - [New-AzManagementGroupDeployment](#new-azmanagementgroupdeployment)
    - [New-AzDeployment](#new-azdeployment)
    - [New-AzTenantDeployment](#new-aztenantdeployment)
    - [Remove-AzManagementGroupDeployment](#remove-azmanagementgroupdeployment)
    - [Remove-AzDeployment](#remove-azdeployment)
    - [Remove-AzTenantDeployment](#remove-aztenantdeployment)
    - [Save-AzManagementGroupDeploymentTemplate](#save-azmanagementgroupdeploymenttemplate)
    - [Save-AzDeploymentTemplate](#save-azdeploymenttemplate)
    - [Save-AzTenantDeploymentTemplate](#save-aztenantdeploymenttemplate)
    - [Stop-AzManagementGroupDeployment](#stop-azmanagementgroupdeployment)
    - [Stop-AzDeployment](#stop-azdeployment)
    - [Stop-AzTenantDeployment](#stop-aztenantdeployment)
    - [Test-AzManagementGroupDeployment](#test-azmanagementgroupdeployment)
    - [Test-AzDeployment](#test-azdeployment)
    - [Test-AzTenantDeployment](#test-aztenantdeployment)
    - [Get-AzResourceGroupDeployment](#get-azresourcegroupdeployment)
    - [Get-AzResourceGroupDeploymentOperation](#get-azresourcegroupdeploymentoperation)
    - [Get-AzResourceGroupDeploymentWhatIfResult](#get-azresourcegroupdeploymentwhatifresult)
    - [New-AzResourceGroupDeployment](#new-azresourcegroupdeployment)
    - [Remove-AzResourceGroupDeployment](#remove-azresourcegroupdeployment)
    - [Save-AzResourceGroupDeploymentTemplate](#save-azresourcegroupdeploymenttemplate)
    - [Stop-AzResourceGroupDeployment](#stop-azresourcegroupdeployment)
    - [Test-AzResourceGroupDeployment](#test-azresourcegroupdeployment)
    - [Get-AzManagementGroupDeploymentWhatIfResult](#get-azmanagementgroupdeploymentwhatifresult)
    - [Get-AzTenantDeploymentWhatIfResult](#get-aztenantdeploymentwhatifresult)
  - [Az.Sql](#azsql)
    - [Set-AzSqlServerActiveDirectoryAdministrator](#set-azsqlserveractivedirectoryadministrator)
  - [Az.Synapse](#azsynapse)
    - [New-AzSynapseSqlPool](#new-azsynapsesqlpool)
    - [Update-AzSynapseSqlPool](#update-azsynapsesqlpool)
  - [Az.Network](#aznetwork)
    - [Approve-AzPrivateEndpointConnection](#approve-azprivateendpointconnection)
    - [Deny-AzPrivateEndpointConnection](#deny-azprivateendpointconnection)
    - [Get-AzPrivateEndpointConnection](#get-azprivateendpointconnection)
    - [Remove-AzPrivateEndpointConnection](#remove-azprivateendpointconnection)
    - [Set-AzPrivateEndpointConnection](#set-azprivateendpointconnection)
    - [New-AzNetworkWatcherConnectionMonitorEndpointObject](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a>Az.Aks

### <a name="new-azakscluster"></a>New-AzAksCluster

- Stöder inte längre parametern `NodeOsType` och inget alias hittades för det ursprungliga parameternamnet, som alltid kommer att vara `Linux`.
- Stöder inte längre aliaset `ClientIdAndSecret` för parametern `ServicePrincipalIdAndSecret`.
- Standardvärdet för `NodeVmSetType` har ändrats från `AvailabilitySet` till `VirtualMachineScaleSets`.
- Standardvärdet för `NetworkPlugin` har ändrats från `none` till `azure`.

#### <a name="before"></a>Före

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a>Efter

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a>Set-AzAksCluster

Stöder inte längre aliaset `ClientIdAndSecret` för parametern `ServicePrincipalIdAndSecret`.

#### <a name="before"></a>Före

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a>Efter

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a>Az.ContainerRegistry

### <a name="new-azcontainerregistry"></a>New-AzContainerRegistry

Stöder inte längre parametern `StorageAccountName` och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a>Efter

`Classic` är inaktuell och `StorageAccountName` har tagits bort eftersom den endast fungerar med klassiska Container Registry.

## <a name="azfunctions"></a>Az.Functions

### <a name="get-azfunctionapp"></a>Get-AzFunctionApp

Tog bort växelparametern `IncludeSlot` från alla förutom en parameteruppsättning av `Get-AzFunctionApp`. Cmdleten stöder nu hämtning av distributionsfack i resultaten när `-IncludeSlot` anges.
Den här funktionen fungerade inte i den tidigare cmdlet-versionen. Detta är dock åtgärdat nu.

### <a name="new-azfunctionapp"></a>New-AzFunctionApp

- Korrigerade `-DisableApplicationInsights` i `New-AzFunctionApp` så att inga Application Insights-projekt skapas när det här alternativet har angetts.
- Tog bort stöd för att skapa PowerShell 6.2-funktionsappar eftersom PowerShell 6.2 är EOL. Vi rekommenderar för närvarande att kunder skapar PowerShell 7.0-funktionsappar i stället.
- Ändrade körningsversionen som är standard i Functions version 3 i Windows för PowerShell-funktionsppar från 6.2 till 7.0 när parametern `RuntimeVersion` inte har angetts.
- Ändrade körningsversionen som är standard i Functions version 3 i Windows och Linux för Node-funktionsppar från 10 till 12 när parametern `RuntimeVersion` inte har angetts. Användare kan dock fortfarande skapa Node 10-funktionsappar genom att ange `-Runtime Node` och `-RuntimeVersion 10`. Ändrade körningsversionen som är standard i Functions version 3 i Linux för Python-funktionsppar från 3.7 till 3.8 när parametern `RuntimeVersion` inte har angetts. Användare kan dock fortfarande skapa Python 3.7-funktionsappar genom att ange `-Runtime Python` och `-RuntimeVersion 3.7`.

#### <a name="before"></a>Före

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a>Efter

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a>Az.KeyVault

### <a name="new-azkeyvault"></a>New-AzKeyVault

Stöder inte längre parametern `DisableSoftDelete` och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a>Efter

Möjligheten att uppdatera inställningen för mjuk borttagning är inaktuell i Az.KeyVault 3.0.0. Läs mer: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="update-azkeyvault"></a>Update-AzKeyVault

Stöder inte längre parametrarna `EnableSoftDelete`, `SoftDeleteRetentionInDays`, och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a>Efter

Möjligheten att uppdatera inställningen för mjuk borttagning är inaktuell i Az.KeyVault 3.0.0. Läs mer: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="get-azkeyvaultsecret"></a>Get-AzKeyVaultSecret

Egenskapen `SecretValueText` av typen `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` har tagits bort. Egenskapen `SecretValueText` har ersatts av `SecretValue`.

#### <a name="before"></a>Före

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a>Efter

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a>Az.ManagedServices

### <a name="get-azmanagedservicesdefinition"></a>Get-AzManagedServicesDefinition

Stöder inte längre parametern `ResourceId` och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Efter

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a>New-AzManagedServicesAssignment

Stöder inte längre parametrarna `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a>Efter

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a>Remove-AzManagedServicesAssignment

Stöder inte längre parametrarna `Id`, `ResourceId`, och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a>Efter

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a>Remove-AzManagedServicesDefinition

Stöder inte längre parametrarna `Id`, `ResourceId`, och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Efter

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a>Az.ResourceManager

### <a name="get-azmanagementgroupdeployment"></a>Get-AzManagementGroupDeployment

Stöder inte längre parametern `ApiVersion` och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a>Efter

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a>Get-AzManagementGroupDeploymentOperation

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-azdeployment"></a>Get-AzDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-azdeploymentoperation"></a>Get-AzDeploymentOperation

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-azdeploymentwhatifresult"></a>Get-AzDeploymentWhatIfResult

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeployment"></a>Get-AzTenantDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeploymentoperation"></a>Get-AzTenantDeploymentOperation

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="new-azmanagementgroupdeployment"></a>New-AzManagementGroupDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="new-azdeployment"></a>New-AzDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="new-aztenantdeployment"></a>New-AzTenantDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="remove-azmanagementgroupdeployment"></a>Remove-AzManagementGroupDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="remove-azdeployment"></a>Remove-AzDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="remove-aztenantdeployment"></a>Remove-AzTenantDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="save-azmanagementgroupdeploymenttemplate"></a>Save-AzManagementGroupDeploymentTemplate

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="save-azdeploymenttemplate"></a>Save-AzDeploymentTemplate

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="save-aztenantdeploymenttemplate"></a>Save-AzTenantDeploymentTemplate

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="stop-azmanagementgroupdeployment"></a>Stop-AzManagementGroupDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="stop-azdeployment"></a>Stop-AzDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="stop-aztenantdeployment"></a>Stop-AzTenantDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="test-azmanagementgroupdeployment"></a>Test-AzManagementGroupDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="test-azdeployment"></a>Test-AzDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="test-aztenantdeployment"></a>Test-AzTenantDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeployment"></a>Get-AzResourceGroupDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeploymentoperation"></a>Get-AzResourceGroupDeploymentOperation

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeploymentwhatifresult"></a>Get-AzResourceGroupDeploymentWhatIfResult

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="new-azresourcegroupdeployment"></a>New-AzResourceGroupDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="remove-azresourcegroupdeployment"></a>Remove-AzResourceGroupDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="save-azresourcegroupdeploymenttemplate"></a>Save-AzResourceGroupDeploymentTemplate

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="stop-azresourcegroupdeployment"></a>Stop-AzResourceGroupDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="test-azresourcegroupdeployment"></a>Test-AzResourceGroupDeployment

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a>Get-AzManagementGroupDeploymentWhatIfResult

Detsamma gäller för `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeploymentwhatifresult"></a>Get-AzTenantDeploymentWhatIfResult

Detsamma gäller för `Get-AzManagementGroupDeployment`.

## <a name="azsql"></a>Az.Sql

### <a name="set-azsqlserveractivedirectoryadministrator"></a>Set-AzSqlServerActiveDirectoryAdministrator

Stöder inte längre parametern `IsAzureADOnlyAuthentication` och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a>Efter

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a>Az.Synapse

### <a name="new-azsynapsesqlpool"></a>New-AzSynapseSqlPool

Stöder inte längre parametrarna `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a>Efter

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a>Update-AzSynapseSqlPool

Stöder inte längre parametrarna `Suspend`, `Resume`, och inget alias hittades för det ursprungliga parameternamnet.

## <a name="aznetwork"></a>Az.Network

### <a name="approve-azprivateendpointconnection"></a>Approve-AzPrivateEndpointConnection

Stöder inte längre parametern `PrivateLinkResourceType` och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a>Efter

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a>Deny-AzPrivateEndpointConnection

Detsamma gäller för `Approve-AzPrivateEndpointConnection`.

### <a name="get-azprivateendpointconnection"></a>Get-AzPrivateEndpointConnection

Detsamma gäller för `Approve-AzPrivateEndpointConnection`.

### <a name="remove-azprivateendpointconnection"></a>Remove-AzPrivateEndpointConnection

Detsamma gäller för `Approve-AzPrivateEndpointConnection`.

### <a name="set-azprivateendpointconnection"></a>Set-AzPrivateEndpointConnection

Detsamma gäller för `Approve-AzPrivateEndpointConnection`.

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a>New-AzNetworkWatcherConnectionMonitorEndpointObject

Stöder inte längre parametrarna `FilterType`, `FilterItem`, och inget alias hittades för det ursprungliga parameternamnet.

#### <a name="before"></a>Före

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a>Efter

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
