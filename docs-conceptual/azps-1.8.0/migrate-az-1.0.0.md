---
title: Alla ändringar från AzureRM till Azure PowerShell Az 1.0.0
description: Den här migreringsguiden innehåller en lista över icke-bakåtkompatibla ändringar som gjorts i Az version 1 av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: 04c520a3171d0b06ceaaa96f1c77bda6b03952ae
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365736"
---
# <a name="breaking-changes-for-az-100"></a>Icke-bakåtkompatibla ändringar för Az 1.0.0

I det här dokumentet finns detaljerad information om ändringar mellan AzureRM 6.x och den nya Az-modulen, version 1.x och senare. Innehållsförteckningen leder dig genom en fullständig migrering, inklusive modulspecifika ändringar som kan påverka skripten.

Allmänna råd om hur du kommer igång med en migrering från AzureRM till Az finns i [Starta migrering från AzureRM till Az](migrate-from-azurerm-to-az.md).

## <a name="table-of-contents"></a>Innehållsförteckning

- [Allmänna icke-bakåtkompatibla ändringar](#general-breaking-changes)
  - [Ändringar av substantivprefix i cmdlet](#cmdlet-noun-prefix-changes)
  - [Ändringar av modulnamn](#module-name-changes)
  - [Borttagna moduler](#removed-modules)
  - [Windows PowerShell 5.1 och .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Tillfällig borttagning av användarinloggning med PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Inloggning med standardenhetskod i stället för med webbläsarfråga](#default-device-code-login-instead-of-web-browser-prompt)
- [Icke-bakåtkompatibla ändringar](#module-breaking-changes)
  - [Az.ApiManagement (tidigare AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (tidigare AzureRM.Billing, AzureRM.Consumption och AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (tidigare AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (tidigare AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (tidigare AzureRM.DataFactories och AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (tidigare AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (tidigare AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (tidigare AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (tidigare AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (tidigare AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (tidigare AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (tidigare AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (tidigare AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup och AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (tidigare AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (tidigare AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (tidigare AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (tidigare Azure.Storage och AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (tidigare AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>Allmänna icke-bakåtkompatibla ändringar

I det här avsnittet beskriver vi de allmänna icke-bakåtkompatibla ändringarna i den nya utformningen av Az-modulen.

### <a name="cmdlet-noun-prefix-changes"></a>Ändringar av substantivprefix i cmdlet

I AzureRM-modulen är de cmdletar som används antingen `AzureRM` eller `Azure` som ett substantivprefix.  Az förenklar och normaliserar cmdlet-namn så att Az används som cmdlet-substantivprefix för alla cmdletar. Exempel:

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

Har ändrats till:

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

För att göra övergången till de nya cmdlet-namnen enklare introduceras två nya cmdletar, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) och [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).  `Enable-AzureRmAlias` skapar alias för de äldre cmdlet-namnen i AzureRM till de nyare cmdlet-namnen i Az. Med argumentet `-Scope` med `Enable-AzureRmAlias` kan du välja var alias ska aktiveras.

Till exempel kan följande skript i AzureRM:

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Kan köras med minimala ändringar med `Enable-AzureRmAlias`:

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

När `Enable-AzureRmAlias -Scope CurrentUser` körs kan alias aktiveras för alla PowerShell-sessioner som du öppnar, så när denna cmdlet har körts behöver ett skript som detta inte ändras alls:

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

All information om användningen av alias-cmdletar finns i [referensmaterialet för Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

När du är redo att inaktivera alias tar `Disable-AzureRmAlias` bort skapade alias. All information finns i [referensmaterialet till Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> När du inaktiverar alias ska du se till att de är inaktiverade för _alla_ omfång som har aktiverade alias.

### <a name="module-name-changes"></a>Ändringar av modulnamn

Modulnamnen har ändrats från `AzureRM.*` till `Az.*`, förutom följande moduler:

| AzureRM-modul | Az-modul |
|----------------|-----------|
| Azure.Storage | Az.Storage |
| Azure.AnalysisServices | Az.AnalysisServices |
| AzureRM.Profile | Az.Accounts |
| AzureRM.Insights | Az.Monitor |
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices | Az.RecoveryServices |
| AzureRM.RecoveryServices | Az.RecoveryServices |
| AzureRM.Tags | Az.Resources |
| AzureRM.MachineLearningCompute | Az.MachineLearning |
| AzureRM.UsageAggregates | Az.Billing |
| AzureRM.Consumption | Az.Billing |

Ändringarna i modulnamnen innebär att alla skript som använder `#Requires` eller `Import-Module` för att läsa in specifika moduler måste ändras så att de använder den nya modulen i stället. För moduler där cmdletsuffixet inte har ändrats innebär det att även om modulnamnet har ändrats har suffixet som anger åtgärdsutrymmet _inte_ det.

#### <a name="migrating-requires-and-import-module-statements"></a>Migrera instruktioner av typen #Requires och Import-Module

Skript som använder `#Requires` eller `Import-Module` för att deklarera beroende av AzureRM-moduler måste uppdateras så att de nya modulnamnen används. Exempel:

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

Ska ändras till:

```azurepowershell-interactive
#Requires -Module Az.Compute
```

För `Import-Module`:

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

Ska ändras till:

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Migrera fullständigt kvalificerade cmdlet-anrop

Skript som använder modulkvalificerade cmdlet-anrop som:

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

Måste ändras så att de nya modul- och cmdlet-namnen används

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Migrera modulmanifestberoenden

För moduler som uttrycker beroenden av AzureRM-moduler via en modulmanifestfil (.psd1) behöver modulnamnen uppdateras i avsnittet `RequiredModules`:

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Måste ändras till:

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Borttagna moduler

Följande moduler har tagits bort:

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Verktygen för de här tjänsterna stöds inte längre aktivt.  Kunderna rekommenderas att övergå till alternativa tjänster så snart som möjligt.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 och .NET 4.7.2

Om Az ska användas med PowerShell 5.1 för Windows måste .NET Framework 4.7.2 vara installerat. För PowerShell Core 6.x och senare krävs inte .NET Framework.

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Tillfällig borttagning av användarinloggning med PSCredential

På grund av ändringar i autentiseringsflödet för .NET Standard tar vi tillfälligt bort användarinloggning med PSCredential. Funktionen återintroduceras i version 1/15/2019/ av Windows PowerShell 5.1 för Windows. Det här diskuteras mer ingående i [det här GitHub-ärendet.](https://github.com/Azure/azure-powershell/issues/7430)

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Inloggning med standardenhetskod i stället för med webbläsarfråga

På grund av ändringar i autentiseringsflödet för .NET Standard använder vi enhetsinloggning som standardinloggningsflöde under interaktiv inloggning. Webbläsarbaserad webbinloggning återintroduceras som standardfunktion i version 1/15/2019 av PowerShell 5.1 för Windows. Då kan användarna välja enhetsinloggning med hjälp av en växlingsparameter.

## <a name="module-breaking-changes"></a>Icke-bakåtkompatibla ändringar

I det här avsnittet beskriver vi icke-bakåtkompatibla ändringar för enskilda moduler och cmdletar.

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (tidigare AzureRM.ApiManagement)

- Följande cmdletar togs bort:
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Använd istället cmdleten **Set-AzApiManagement** för att ställa dessa egenskaper
- Följande egenskaper togs bort:
  - Egenskapen `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` och `ScmHostnameConfiguration` av typen `PsApiManagementHostnameConfiguration` har tagits bort från `PsApiManagementContext`. Använd i stället `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` och `ScmCustomHostnameConfiguration` av typen `PsApiManagementCustomHostNameConfiguration`.
  - Egenskapen `StaticIPs` har tagits bort från PsApiManagementContext. Egenskapen har delats upp i `PublicIPAddresses` och `PrivateIPAddresses`.
  - Den nödvändiga egenskapen `Location` har tagits bort från cmdleten New-AzureApiManagementVirtualNetwork.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (tidigare AzureRM.Billing, AzureRM.Consumption och AzureRM.UsageAggregates)

- Parametern `InvoiceName` har tagits bort från cmdleten `Get-AzConsumptionUsageDetail`.  Skripten behöver nu använda andra identitetsparametrar för fakturan.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (tidigare AzureRM.CognitiveServices)

- Parameteruppsättningen `GetSkusWithAccountParamSetName` har tagits bort från cmdleten `Get-AzCognitiveServicesAccountSkus`.  Du måste hämta SKU:er efter typ och plats i stället för att använda ResourceGroupName och Account Name.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (tidigare AzureRM.Compute)

- `IdentityIds` tas bort från egenskapen `Identity` i objekten `PSVirtualMachine` och `PSVirtualMachineScaleSet` Skripten bör nu inte längre använda värdet för det här fältet för att fatta bearbetningsbeslut.
- Typ av `InstanceView`-egenskap för `PSVirtualMachineScaleSetVM`-objekt ändras från `VirtualMachineInstanceView` till `VirtualMachineScaleSetVMInstanceView`
- Egenskaperna `AutoOSUpgradePolicy` och `AutomaticOSUpgrade` tas bort från egenskapen `UpgradePolicy`
- Typ av `Sku`-egenskap i `PSSnapshotUpdate`-objekt ändras från `DiskSku` till `SnapshotSku`
- `VmScaleSetVMParameterSet` tas bort från cmdleten `Add-AzVMDataDisk`, och du kan inte längre lägga till en datadisk individuellt till en virtuell ScaleSet-dator.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (tidigare AzureRM.DataFactories och AzureRM.DataFactoryV2)

- Parametern `GatewayName` har blivit obligatorisk i cmdleten `New-AzDataFactoryEncryptValue`
- Cmdleten `New-AzDataFactoryGatewayKey` har tagits bort
- Parametern `LinkedServiceName` har tagits bort från cmdleten `Get-AzDataFactoryV2ActivityRun` Skripten ska inte längre använda värdet för det här fältet för att fatta bearbetningsbeslut.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (tidigare AzureRM.DataLakeAnalytics)

- Följande inaktuella cmdletar har tagits bort: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` och `Set-AzDataLakeAnalyticsCatalogSecret`

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (tidigare AzureRM.DataLakeStore)

- I följande cmdletar har parametern `Encoding` ändrats från typen `FileSystemCmdletProviderEncoding` till `System.Text.Encoding`. Den här ändringen tar bort kodningsvärdena `String` och `Oem`. Övriga tidigare kodningsvärden kvarstår.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- Det inaktuella egenskapsaliaset `Tags` har tagits bort från cmdletarna `New-AzDataLakeStoreAccount` och `Set-AzDataLakeStoreAccount`

  Skript som använder
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  Ska ändras till
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- De inaktuella egenskaperna `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` har tagits bort från `PSDataLakeStoreAccountBasic`-objekt.  Alla skript som använder den `PSDatalakeStoreAccount` som returnerades från `Get-AzDataLakeStoreAccount` ska inte längre referera till dessa egenskaper.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (tidigare AzureRM.KeyVault)

- Egenskapen `PurgeDisabled` har tagits bort från `PSKeyVaultKeyAttributes`-, `PSKeyVaultKeyIdentityItem`- och `PSKeyVaultSecretAttributes`-objekt Skript ska inte längre referera till egenskapen ```PurgeDisabled``` för att fatta bearbetningsbeslut.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (tidigare AzureRM.Media)

- Tog bort inaktuellt egenskapsalias `Tags` från skript för cmdleten `New-AzMediaService` med hjälp av
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  Ska ändras till
  ```azurepowershell-interactive
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (tidigare AzureRM.Insights)

- Tog bort pluralnamnet `Categories` och parametern `Timegrains` och ersatte med singularparameternamn från cmdlet-skript för `Set-AzDiagnosticSetting` med hjälp av
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  Ska ändras till
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (tidigare AzureRM.Network)

- Tog bort den inaktuella parametern `ResourceId` från cmdleten `Get-AzServiceEndpointPolicyDefinition`
- Tog bort den inaktuella egenskapen `EnableVmProtection` från objektet `PSVirtualNetwork`
- Tog bort den inaktuella cmdleten `Set-AzVirtualNetworkGatewayVpnClientConfig`
  
Skript bör inte längre fatta bearbetningsbeslut baserat på värdena för dessa fält.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (tidigare AzureRM.OperationalInsights)

- Standardparameteruppsättningen för `Get-AzOperationalInsightsDataSource` har tagits bort och `ByWorkspaceNameByKind` är nu standardparameteruppsättning

  Skript som listar datakällor med hjälp av
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  ska ändras så att de anger en typ
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (tidigare AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup och AzureRM.RecoveryServices.SiteRecovery)

- Parametern `Encryption` har tagits bort från cmdleten `New/Set-AzRecoveryServicesAsrPolicy`
- Parametern `TargetStorageAccountName` är nu obligatorisk för hanterade diskåterställningar i cmdleten `Restore-AzRecoveryServicesBackupItem`
- Tog bort parametrarna `StorageAccountName` och `StorageAccountResourceGroupName` i cmdleten `Restore-AzRecoveryServicesBackupItem`
- Tog bort parametern `Name` i cmdleten `Get-AzRecoveryServicesBackupContainer`

### <a name="azresources-previously-azurermresources"></a>Az.Resources (tidigare AzureRM.Resources)

- Parametern `Sku` har tagits bort från cmdleten `New/Set-AzPolicyAssignment`
- Parametern `Password` har tagits bort från cmdleten `New-AzADServicePrincipal` och `New-AzADSpCredential` Lösenord genereras automatiskt och skript som tillhandahöll lösenordet:

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Bör ändras så att de hämtar lösenordet från utdata:

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (tidigare AzureRM.ServiceFabric)

- Följande cmdlet-returtyper har ändrats:
  - Egenskapen `ServiceTypeHealthPolicies` av typen `ApplicationHealthPolicy` har tagits bort.
  - Egenskapen `ApplicationHealthPolicies` av typen `ClusterUpgradeDeltaHealthPolicy` har tagits bort.
  - Egenskapen `OverrideUserUpgradePolicy` av typen `ClusterUpgradePolicy` har tagits bort.
  - Ändringarna påverkar följande cmdletar:
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql (tidigare AzureRM.Sql)

- Tog bort parametrarna `State` och `ResourceId` från cmdleten `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`
- Följande inaktuella cmdletar har tagits bort: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`
- Tog bort den inaktuella parametern `Current` från cmdleten `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`
- Tog bort den inaktuella parametern `DatabaseName` från cmdleten `Get-AzSqlServerServiceObjective`
- Tog bort den inaktuella parametern `PrivilegedLogin` från cmdleten `Set-AzSqlDatabaseDataMaskingPolicy`

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (tidigare Azure.Storage och AzureRM.Storage)

- Standardparameteruppsättningen har ändrats till `OAuthParameterSet` för att det ska gå att skapa en Oauth-lagringskontext endast med namnet på lagringskontot
  - Exempel: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- Parametern `Location` har blivit obligatorisk i cmdleten `Get-AzStorageUsage`
- Storage-API-metoderna använder nu TAP (uppgiftsbaserat asynkront mönster) i stället för synkrona API-anrop. Följande exempel visar de nya asynkrona kommandona:

#### <a name="blob-snapshot"></a>Blobögonblicksbild

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

Az:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a>Dela ögonblicksbild

AzureRM:

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

Az:

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a>Ångra borttagning av mjukborttagen blob

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

Az:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a>Ange blobnivå

AzureRM:

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

Az:

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (tidigare AzureRM.Websites)

- Inaktuella egenskaper har tagits bort från `PSAppServicePlan`-, `PSCertificate`-, `PSCloningInfo`- och `PSSite`-objekten
