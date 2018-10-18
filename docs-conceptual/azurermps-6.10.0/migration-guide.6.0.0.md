---
title: Icke-bakåtkompatibla ändringar för Microsoft Azure PowerShell 6.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i version 6 av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 227bec0f7eb24b0941e9e21d37524b290c4b83a5
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/18/2018
ms.locfileid: "49398965"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Icke-bakåtkompatibla ändringar för Microsoft Azure PowerShell 6.0.0

Det här dokumentet fungerar både som ett meddelande om större ändringar och som en migreringsguide för användare av Microsoft Azure PowerShell-cmdletar. I varje avsnitt beskrivs både orsaken till den större ändringen och det enklaste migreringssättet. Se den pull-begäran som är kopplad till varje ändring för en mer djupgående kontext.

## <a name="table-of-contents"></a>Innehållsförteckning

- [Allmänna icke-bakåtkompatibla ändringar](#general-breaking-changes)
    - [Lägsta version av PowerShell som krävs har höjts till 5.0](#minimum-powershell-version-required-bumped-to-50)
    - [Funktionen för att automatiskt spara kontext har aktiverats som standard](#context-autosave-enabled-by-default)
    - [Borttagning av alias för taggar](#removal-of-tags-alias)
- [Icke-bakåtkompatibla ändringar i AzureRM.Compute-cmdletar](#breaking-changes-to-azurermcompute-cmdlets)
- [Icke-bakåtkompatibla ändringar i AzureRM.DataLakeStore-cmdletar](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [Icke-bakåtkompatibla ändringar i AzureRM.Dns-cmdletar](#breaking-changes-to-azurermdns-cmdlets)
- [Icke-bakåtkompatibla ändringar i AzureRM.Insights-cmdletar](#breaking-changes-to-azurerminsights-cmdlets)
- [Icke-bakåtkompatibla ändringar i AzureRM.KeyVault-cmdletar](#breaking-changes-to-azurermkeyvault-cmdlets)
- [Icke-bakåtkompatibla ändringar i AzureRM.Network-cmdletar](#breaking-changes-to-azurermnetwork-cmdlets)
- [Icke-bakåtkompatibla ändringar i AzureRM.RedisCache-cmdletar](#breaking-changes-to-azurermrediscache-cmdlets)
- [Icke-bakåtkompatibla ändringar i AzureRM.Resources-cmdletar](#breaking-changes-to-azurermresources-cmdlets)
- [Icke-bakåtkompatibla ändringar i AzureRM.Storage-cmdletar](#breaking-changes-to-azurermstorage-cmdlets)
- [Borttagna moduler](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>Allmänna icke-bakåtkompatibla ändringar

### <a name="minimum-powershell-version-required-bumped-to-50"></a>Lägsta version av PowerShell som krävs har höjts till 5.0

Tidigare krävde Azure PowerShell _minst_ version 3.0 av PowerShell för att köra en cmdlet. Det här kravet kommer att höjas till version 5.0 av PowerShell framöver. Information om hur du uppgraderar till PowerShell 5.0 finns i [den här tabellen](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

### <a name="context-autosave-enabled-by-default"></a>Funktionen för att automatiskt spara kontext har aktiverats som standard

Automatiskt sparande av kontext är lagring av inloggningsinformation för Azure som kan användas mellan nya och olika PowerShell-sessioner. Mer information om att spara kontext automatiskt finns i [det här dokumentet](https://docs.microsoft.com/powershell/azure/context-persistence).

Tidigare var funktionen för att automatiskt spara kontext inaktiverad som standard, vilket innebar att användarnas autentiseringsinformation inte lagrades mellan sessioner förrän de körde cmdleten `Enable-AzureRmContextAutosave` för att aktivera kontextpersistens. Funktionen för att automatiskt spara kontext kommer att vara aktiverad som standard hädanefter, vilket innebär att kontexten kommer att sparas automatiskt för användare _som inte har sparat några inställningar för automatiskt sparande av kontext_ nästa gång de loggar in. Användarna kan välja bort den här funktionen med hjälp av cmdleten `Disable-AzureRmContextAutosave`.

_Obs_: användare som tidigare har inaktiverat automatiskt sparande av kontext och användare som har aktiverat funktionen och har befintliga kontexter påverkas inte av den här ändringen

### <a name="removal-of-tags-alias"></a>Borttagning av alias för taggar

Alias `Tags` för parametern `Tag` har tagits bort för flera cmdletar. Nedan visas en lista med moduler (och de motsvarande cmdletarna) som påverkas av det här:

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

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>Icke-bakåtkompatibla ändringar i AzureRM.Compute-cmdletar

**Övrigt**
- SKU-namnegenskapen som är kapslad i typerna `PSDisk` och `PSSnapshot` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- Typegenskapen för lagringskonton som är kapslad i typerna `PSVirtualMachine`, `PSVirtualMachineScaleSet` och `PSImage` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**Add-AzureRmVMDataDisk**
- Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**Add-AzureRmVmssDataDisk**
- Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**New-AzureRmAvailabilitySet**
- Parametern `Managed` har tagits bort och ersatts av `Sku`

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- Godkända värden för parametern `SkuName` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**New-AzureRmDiskUpdateConfig**
- Godkända värden för parametern `SkuName` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**New-AzureRmSnapshotConfig**
- Godkända värden för parametern `SkuName` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**New-AzureRmSnapshotUpdateConfig**
- Godkända värden för parametern `SkuName` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**Set-AzureRmImageOsDisk**
- Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**Set-AzureRmVMAEMExtension**
- Parametern `DisableWAD` har tagits bort
    -  Windows Azure Diagnostics är inaktiverat som standard

**Set-AzureRmVMDataDisk**
- Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**Set-AzureRmVMOSDisk**
- Godkända värden för parametern `StorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**Set-AzureRmVmssStorageProfile**
- Godkända värden för parametern `ManagedDisk` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

**Update-AzureRmVmss**
- Godkända värden för parametern `ManagedDiskStorageAccountType` har ändrats från `StandardLRS` och `PremiumLRS` till `Standard_LRS` respektive `Premium_LRS`

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>Icke-bakåtkompatibla ändringar i AzureRM.DataLakeStore-cmdletar

**Export-AzureRmDataLakeStoreItem**
- Parametrarna `PerFileThreadCount` och `ConcurrentFileCount` har tagits bort. Använd parametern `Concurrency` hädanefter

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- Parametrarna `PerFileThreadCount` och `ConcurrentFileCount` har tagits bort. Använd parametern `Concurrency` hädanefter

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- Parametern `Clean` har tagits bort

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>Icke-bakåtkompatibla ändringar i AzureRM.Dns-cmdletar

**New-AzureRmDnsRecordSet**
- Parametern `Force` har tagits bort

**Remove-AzureRmDnsRecordSet**
- Parametern `Force` har tagits bort

**Remove-AzureRmDnsZone**
- Parametern `Force` har tagits bort

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>Icke-bakåtkompatibla ändringar i AzureRM.Insights-cmdletar

**Add-AzureRmAutoscaleSetting**
- Parameteralias `AutoscaleProfiles` och `Notifications` har tagits bort

**Add-AzureRmLogProfile**
- Parameteralias `Categories` och `Locations` har tagits bort

**Add-AzureRmMetricAlertRule**
- Parameteralias `Actions` har tagits bort

**Add-AzureRmWebtestAlertRule**
- Parameteralias `Actions` har tagits bort

**Get-AzureRmLog**
- Parameteralias `MaxRecords` och `MaxEvents` har tagits bort

**Get-AzureRmMetricDefinition**
- Parameteralias `MetricNames` har tagits bort

**New-AzureRmAlertRuleEmail**
- Parameteralias `CustomEmails` och `SendToServiceOwners` har tagits bort

**New-AzureRmAlertRuleWebhook**
- Parameteralias `Properties` har tagits bort

**New-AzureRmAutoscaleNotification**
- Parameteralias `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` och `Webhooks` har tagits bort

**New-AzureRmAutoscaleProfile**
- Parameteralias `Rules`, `ScheduleDays`, `ScheduleHours` och `ScheduleMinutes` har tagits bort

**New-AzureRmAutoscaleWebhook**
- Parameteralias `Properties` har tagits bort

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>Icke-bakåtkompatibla ändringar i AzureRM.KeyVault-cmdletar

**Add-AzureKeyVaultCertificate**
- Parametern `CertificatePolicy` har blivit obligatorisk.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- Cmdleten accepterar inte längre enskilda parametrar som utgör åtkomst-token. I stället ersätter cmdleten explicita tokenparametrar, som t. ex. `Service` eller `Permissions` med en allmän `TemplateUri`-parameter som motsvarar en exempel-åtkomsttoken och som definierats någon annanstans (förmodligen med Storage PowerShell-cmdletar eller sammanställts manuellt enligt Storage-dokumentationen.) Cmdleten behåller parametern `ValidityPeriod`.

Mer information om att sammanställa token för delad åtkomst för Azure Storage hittar du på följande dokumentationssidor:
- [Skapa en tjänst-SAS] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)
- [Skapa en konto-SAS] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)

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

**Set-AzureKeyVaultCertificateIssuer**
- Parametern `IssuerProvider` har blivit obligatorisk.

**Undo-AzureKeyVaultCertificateRemoval**
- Resultatet av den här cmdleten har ändrats från `CertificateBundle` till `PSKeyVaultCertificate`.

**Undo-AzureRmKeyVaultRemoval**
- `ResourceGroupName` har tagits bort från parameteruppsättningen `InputObject` och hämtas istället från `InputObject`-parameterns `ResourceId`-egenskap.

**Set-AzureRmKeyVaultAccessPolicy**
- Behörigheten `all` har tagits bort från `PermissionsToKeys`, `PermissionsToSecrets` och `PermissionsToCertificates`.

**Allmänt**
- Egenskapen `ValueFromPipelineByPropertyName` togs bort från alla cmdletar där överföring genom `InputObject` har aktiverats.  Cmdletarna som påverkas är:
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

- `ConfirmImpact`-nivåerna har tagits bort från alla cmdletar.  Cmdletarna som påverkas är:
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

- `IKeyVaultDataServiceClient` har uppdaterats så att alla certifikatåtgärder returnerar PSTypes istället för SDK-typer. Det här omfattar:
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

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>Icke-bakåtkompatibla ändringar i AzureRM.Network-cmdletar


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- Parametern `ProbeEnabled` har tagits bort

**Add-AzureRmVirtualNetworkPeering**
- Parameteralias `AlloowGatewayTransit` har tagits bort

**New-AzureRmApplicationGatewayBackendHttpSettings**
- Parametern `ProbeEnabled` har tagits bort

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- Parametern `ProbeEnabled` har tagits bort

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>Icke-bakåtkompatibla ändringar i AzureRM.RedisCache-cmdletar

**New-AzureRmRedisCache**
- Parametrarna `Subnet` och `VirtualNetwork` har tagits bort och ersatts av `SubnetId`
- Parametern `RedisVersion` har tagits bort
- Parametern `MaxMemoryPolicy` har tagits bort och ersatts av `RedisConfiguration`

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- Parametern `MaxMemoryPolicy` har tagits bort och ersatts av `RedisConfiguration`

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>Icke-bakåtkompatibla ändringar i AzureRM.Resources-cmdletar

**Find-AzureRmResource**
- Den här cmdleten har tagits bort och funktionen har flyttats till `Get-AzureRmResource`

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- Den här cmdleten har tagits bort och funktionen har flyttats till `Get-AzureRmResourceGroup`

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

**Get-AzureRmRoleDefinition**
- Parametern `AtScopeAndBelow` har tagits bort.

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>Icke-bakåtkompatibla ändringar i AzureRM.Storage-cmdletar

**New-AzureRmStorageAccount**
- Parametern `EnableEncryptionService` har tagits bort

**Set-AzureRmStorageAccount**
- Parametrarna `EnableEncryptionService` och `DisableEncryptionService` har tagits bort

## <a name="removed-modules"></a>Borttagna moduler

### `AzureRM.ServerManagement`

Serverhanteringsverktyget [togs ur bruk förra året](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/) och därför togs den motsvarande modulen för SMT, `AzureRM.ServerManagement`, bort från `AzureRM` och kommer inte att levereras i framtiden.

### `AzureRM.SiteRecovery`

Modulen `AzureRM.SiteRecovery` ersätts av `AzureRM.RecoveryServices.SiteRecovery`, som är en funktionell överordnad uppsättning av modulen `AzureRM.SiteRecovery` och som innehåller en ny uppsättning motsvarande cmdletar. En fullständig lista över mappningar från gamla till nya cmdletar finns nedan:

| Inaktuella cmdletar                                        | Motsvarande cmdletar                                                | Alias                                  |
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
