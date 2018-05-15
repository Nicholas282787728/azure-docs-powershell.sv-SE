---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Viktig information

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

---

## <a name="600---may-2018"></a>6.0.0 – Maj 2018

### <a name="general"></a>Allmänt
* Konfigurera minsta beroende för moduler till PowerShell 5.0

### <a name="azurestorage"></a>Azure.Storage
* Stöd som namn på blob-behållare för Storage
    - New-AzureStorageBlobContainer
    - Remove-AzureStorageBlobContainer
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* Åtgärda problemet med att vissa felmeddelanden om Storage-cmdletar inte innehåller information om felet

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Lägger till flera icke-bakåtkompatibla ändringar
    - Mer information finns i migreringsguiden

### <a name="azurermautomation"></a>AzureRM.Automation
* Ta bort inaktuella alias för ”taggar” från cmdletar
    - "Set-AzureRmAutomationRunbook"

### <a name="azurermbatch"></a>AzureRM.Batch
* Dokumentationen för New-AzureBatchPool för att ta bort inaktuella exempel har uppdaterats

### <a name="azurermcdn"></a>AzureRM.Cdn
* Lägger till flera icke-bakåtkompatibla ändringar
    - Mer information finns i migreringsguiden

### <a name="azurermcompute"></a>AzureRM.Compute
* ”New-AzureRmVm” och ”New-AzureRmVmss” stöder utförliga utdata för parametrar
* ”New-AzureRmVm” och ”New-AzureRmVmss” (enkelt parameteruppsättning) stöder tilldelning av användardefinierade och (eller) systemdefinierade identiteter till virtuella datorer.
* Funktionerna VMSS Redeploy and PerformMaintenance
    -  Lägg till de nya växelparametrarna -Redeploy och -PerformMaintenance till ”Set-AzureRmVmss” och ”Set-AzureRmVmssVM”
* Lägg till växelparametern DisableVMAgent till cmdleten ”Set-AzureRmVMOperatingSystem”
* ”New-AzureRmVm” och ”New-AzureRmVmss” (enkel parameteruppsättning) stöder en ”Win10”-avbildning.
* Cmdleten ”Repair-AzureRmVmssServiceFabricUpdateDomain” har lagts till.
* Lägger till flera icke-bakåtkompatibla ändringar
    - Mer information finns i guiden för migrering
* ”Set-AzureRmVmDiskEncryptionExtension” gör AAD-parametrar valfria

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Ta bort inaktuella alias för ”taggar” från cmdletar
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* SDK:n för ADF .Net har uppdaterats till version 0.7.0-preview som innehåller följande ändringar:
    - Körningsparametrar och egenskap för anslutningshantering har lagts till på ExecuteSSISPackage-aktivitet
    - PostgreSql, en MySql-länkad tjänst för att använda en fullständig anslutningssträng istället för server, databas, schema, användarnamn och lösenord har uppdaterats
    - Schemat från DB2-länkad tjänst har tagits bort
    - Schemaegenskap från Teradata-länkad tjänst har tagits bort
    - LinkedService, Dataset, CopySource för Responsys har lagts till

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Ta bort inaktuella alias för ”taggar” från cmdletar
    - ”New-AzureRmDataLakeAnalyticsAccount”
    - ”Set-AzureRmDataLakeAnalyticsAccount”

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Lägg till ny funktion för rekursiv Acl-förändring för Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry och Set-AzureRmDataLakeStoreItemAcl
* Lägg till ny cmdlet för att hämta en innehållssammanfattning under en katalog
* Lägg till ny cmdlet för att hämta dump angående diskanvändning och Acl
* Åtgärda returtypen för Set-AzureRmDataLakeStoreItemAcl-verktyget till IEnumerable<DataLakeStoreItemAce>
* Åtgärda returtypen för Set-AzureRmDataLakeStoreItemAclEntry-verktyget till IEnumerable<DataLakeStoreItemAce>
* Icke-bakåtkompatibla ändringar för Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem

### <a name="azurermdns"></a>AzureRM.Dns
* Lägger till flera icke-bakåtkompatibla ändringar
    - Mer information finns i migreringsguiden

### <a name="azurermeventhub"></a>AzureRM.EventHub
* Hjälp för cmdletar som saknar exempel har uppdaterats

### <a name="azurerminsights"></a>AzureRM.Insights
* Flera icke-bakåtkompatibla ändringar har introducerats
    - Mer information finns i migreringsguiden

### <a name="azurermiothub"></a>AzureRM.IotHub
* Aktivera taggar och grundläggande SKU för IotHub

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Icke-bakåtkompatibla ändringar för stöd för pipingscenarier
* Nya cmdletar har lagts till: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval och Undo-AzureKeyVaultManagedStorageAccountRemoval

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Ta bort inaktuella alias för ”taggar” från cmdletar
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* Ta bort inaktuella alias för ”taggar” från cmdletar
    - ”Set-AzureRmMediaService”

### <a name="azurermnetwork"></a>AzureRM.Network
* Lägg till stöd för planresurs för DDoS-skydd
* Flera icke-bakåtkompatibla ändringar har introducerats
    - Mer information finns i migreringsguiden

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Presentation av flera icke-bakåtkompatibla ändringar
    - Mer information finns i migreringsguiden

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Presentation av flera icke-bakåtkompatibla ändringar
    - Mer information finns i migreringsguiden

### <a name="azurermprofile"></a>AzureRM.Profile
* Aktivera automatiskt sparande av kontext som standard
* Lägg till egenskaperna USGovernmentOperationalInsightsEndpoint och USGovernmentOperationalInsightsEndpointResourceId i en Azure-miljö för US Gov.

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices
* Autentiseringsrubriken i SiteRecovery-scenarier har korrigerats

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Flera icke-bakåtkompatibla ändringar har introducerats
    - Mer information finns i migreringsguiden

### <a name="azurermresources"></a>AzureRM.Resources
* Ta bort den inaktuella parametern -AtScopeAndBelow från anropet Get-AzureRmRoledefinition
* Inkludera tilldelningar till borttagna användare/grupper/huvudnamn för tjänsten i resultat för Get-AzureRmRoleAssignment
* Lägg till tabbifyllning för Scope och ResourceType
* Lägg till bekväm cmdlet för att skapa huvudnamn för tjänst
* Sammanfoga funktioner för att hämta och hitta med Get-AzureRmResource
* Lägg till AD-cmdletar:
  - Remove-AzureRmADGroupMember
  - Get-AzureRmADGroup
  - New-AzureRmADGroup
  - Remove-AzureRmADGroup
  - Remove-AzureRmADUser
  - Update-AzureRmADApplication
  - Update-AzureRmADServicePrincipal
  - Update-AzureRmADUser

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Uppdatera SKU för version av Linux-avbildning som är standard
  - SKU-uppdatering för UbuntuServer1604 som är standard för NewAzureServiceFabricCluster.cs

### <a name="azurermstorage"></a>AzureRM.Storage
* Flera icke-bakåtkompatibla ändringar har introducerats
    - Mer information finns i migreringsguiden

### <a name="azurermwebsites"></a>AzureRM.Websites
* Uppgradera till den senaste versionen av Websites-SDK
* Egenskaperna -AssignIdentity och -Httpsonly har lagts till för Set-AzureRmWebApp och Set-AzureRmWebAppSlot
* Två nya cmdletar har lagts till: Get-AzureRmWebAppSnapshots och Restore-AzureRmWebAppSnapshot
