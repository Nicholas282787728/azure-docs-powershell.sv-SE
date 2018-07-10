---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406672"
---
# <a name="release-notes"></a>Viktig information

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

---
## <a name="640---july-2018"></a>6.4.0 – juli 2018
#### <a name="general"></a>Allmänt
* Formatering av OutputType i hjälpfiler har korrigerats för de flesta moduler

#### <a name="azurermprofile"></a>AzureRM.Profile
* Ps1Xml-attribut har lagts till för grundläggande utdatatyper

#### <a name="azurermcompute"></a>AzureRM.Compute
* IP-tagg-funktioner för VMSS
    - "New-AzureRmVmssIpTagConfig"-cmdlet har lagts till
    - IpTag-parameter har lagts till för New-AzureRmVmssIpConfig
* Automatisk återställningsfunktion för operativsystem för VMSS
    - DisableAutoRollback-parametrar har lagts till för New-AzureRmVmssConfig och Update-AzureRmVmss
* Funktion för uppgraderingshistorik för operativsystem för Vmss
    - OSUpgradeHistory-växlingsparametern har lagts till för Get-AzureRmVmss

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Lägg till stöd för katalog-ACL:er med hjälp av följande kommandon:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Lägg till stöd för annullering och förloppsspårning för Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Lägg till stöd för annullering för Export-AzureRmDataLakeStoreChildItemProperties
* Åtgärda tömning av felsökningsmeddelanden för cmdletar som gör rekursiva åtgärder
* Åtgärda platsen för testning av DataLake-cmdletar

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Parametrar för optimalt maxantal har lagts till i liståtgärds-cmdletarna Get-AzureRmEventHub och Get-AzureRmEventHubConsumerGroup
* Ett problem i New-AzureRmEventHub-cmdleten har åtgärdats där minst en parameter behövdes när du skapade en ny EventHub. Angiven standardparameter har ställts in.
* Valfri parameter för KeyValue har lagts till för New-AzureRmEventHubKey-cmdleten, vilket gör det möjligt att ange KeyValue.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Åtgärda problem där alla resurser returnerades av Get-AzureRmKeyVault-taggen

#### <a name="azurermnetwork"></a>AzureRM.Network
* Gör nya SKU:er tillgängliga för zonredundanta VirtualNetworkGateways
* Nya kommandon har lagts till för funktionen: ExpressRoute Partner APIs via ARM
    - Get-AzureRmExpressRouteCrossConnection har lagts till
    - Set-AzureRmExpressRouteCrossConnection har lagts till
    - Add-AzureRmExpressRouteCrossConnectionPeering har lagts till
    - Get-AzureRmExpressRouteCrossConnectionPeering har lagts till
    - Remove-AzureRmExpressRouteCrossConnectionPeering har lagts till
    - Get-AzureRMExpressRouteCrossConnectionArpTable har lagts till
    - Get-AzureRMExpressRouteCrossConnectionRouteTable har lagts till
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary har lagts till

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices
* Get-AzureRmRecoveryServicesBackupStatus-cmdlet har lagts till. Denna cmdlet tar ett ID för virtuell dator och kontrollerar om den virtuella datorn skyddas av ett valv i prenumerationen. Om ett sådant valv finns returnerar cmdleten valvinformationen.

#### <a name="azurermresources"></a>AzureRM.Resources
* Uppdatera Get-AzureRmPolicyAssignment-cmdletar:
    - Lägg till stöd för att lista -Scope-värden på hanteringsgruppsnivå
    - Lägg till stöd för hämtning av enskilda tilldelningar med -Scope-värden på hanteringsgruppsnivå.
    - Lägg till växlar för -Effective och -All till kontrollparametrar
* Uppdatera Get/New/Remove/Set-AzureRmPolicyDefinition-cmdletar
    - Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp
    - Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration
* Uppdatera Get/New/Remove/Set-AzureRmPolicySetDefinition-cmdletar
    - Lägg till parameter för -ManagementGroupName om du vill tillämpa åtgärder för en viss hanteringsgrupp
    - Lägg till parameter för -SubscriptionId om du vill tillämpa åtgärder för en viss prenumeration
* Lägg till stöd för hemliga KeyVault-referenser i parametrar när du använder "TemplateParameterObject" i "New-AzureRmResourceGroupDeployment"
* Åtgärda problem med att "-EndDate"-parametern ignorerades på grund av "New-AzureRmADAppCredential"
    - https://github.com/Azure/azure-powershell/issues/6505
* Åtgärda problem med att felaktig URL användes i "New-AzureRmADAppCredential" vid begäran
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Valfri parameter för -KeyValue har lagts till för New-AzureRmServiceBusKey-cmdleten, vilket gör det möjligt att ange KeyValue.

#### <a name="azurermsql"></a>AzureRM.Sql
* Användardefinierade återställningspunkter har klargjorts för SQLDW i New-AzureRmSqlDatabaseRestorePoint-hjälpen
* Dokumentationen om parametern -ComputeGeneration har uppdaterats i fler cmdletar

## <a name="630---june-2018"></a>6.3.0 – juni 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Uppdaterade felmeddelanden för Enable-AzureRmContextAutoSave
* Skapa en kontext för varje prenumeration när du kör ”Connect-AzureRmAccount” utan tidigare kontext

#### <a name="azurestorage"></a>Azure.Storage
* Ytterligare information om parametern -Permissions har lagts till i hjälpfilerna.

#### <a name="azurermcompute"></a>AzureRM.Compute
* ”Get-AzureRmVmDiskEncryptionStatus” korrigerar ett problem för virtuella datorer utan datadiskar 
* Uppdatera version av klientbibliotek för Compute för att korrigera följande cmdletar
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* Följande cmdletar har åtgärdats för att visa ”Åtgärds-ID” och ”Åtgärdsstatus” på ett korrekt sätt:
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Ta bort verifieringsvillkoren ValidateNotNullOrEmpty för SubjectBeginsWith/SubjectEndsWith i cmdleten Update-AzureRmEventGridSubscription för att ändra de här parametrarna till en tom sträng om det behövs.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Åtgärda problem där inga taggar returneras när Get-AzureRmKeyVault -Tag körs

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Offentlig lansering av cmdletar för Policy Insights
    - Använd API-version 2018-04-04
    - Lägg till PolicyDefinitionReferenceId i resultaten för Get-AzureRmPolicyStateSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices
* Parametern -Vault har lagts till i cmdletarna för RecoveryServices.Backup. När den godkänns åsidosätts cmdleten Set-AzureRmRecoveryServicesContext.

#### <a name="azurermsql"></a>AzureRM.Sql
* Exemplet i hjälpfilen för Get-AzureRmSqlDatabaseExpanded har uppdaterats

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Hjälpfilen för Add-AzureRmTrafficManagerEndpointConfig har uppdaterats

#### <a name="azurermwebsites"></a>AzureRM.Websites
* ”Set-AzureRmWebApp” har uppdaterats så att den inte skriver över appinställningarna när du använder -AssignIdentity
* ”New-AzureRMWebAppSlot” har uppdaterats för att visa att AppServicePlan är en valfri parameter

## <a name="621---june-2018"></a>6.2.1 – juni 2018
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* PSWorkspace-modellen har uppdaterats för att tillåta att nätverket använder typ som en parameter

## <a name="620---june-2018"></a>6.2.0 – juni 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS VM-uppdateringsfunktion
    - Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till
    - Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:
    - Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till
    - QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret
    - Flera modelltyper från SecretBase till Object har uppdaterats
    - Utlösaren Blob Events har lagts till

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Uppdatera dokumentation med exempel på utdata

### <a name="azurermnetwork"></a>AzureRM.Network
* Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar

#### <a name="azurermresources"></a>AzureRM.Resources
* Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob

### <a name="azurermsql"></a>AzureRM.Sql
* Följande cmdletar har uppdaterats med valfri LicenseType-parameter
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.

## <a name="610---may-2018"></a>6.1.0 – maj 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Aktivera Gateway associerings- och avassocieringsåtgärder på AS.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till
* Stöd för serverdelen på ServiceFabric har lagts till
* Stöd för Application Insights-loggare har lagts till
* Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till
* Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till
* Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till
* Stöd för MSI-identitet har lagts till
* Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Släpp nya cmdleten Get-AzureBatchPoolNodeCounts
* Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties
* Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry 
* Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry 

#### <a name="azurermnetwork"></a>AzureRM.Network
* Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0
* Cmdlet har lagts till för att skapa protokollinformation
    - New-AzureRmNetworkWatcherProtocolConfiguration
* Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* Cmdlet har lagts till för att hämta en kretsanslutning
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats

#### <a name="azurermsql"></a>AzureRM.Sql
* Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats
* Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds, och att en begäran med den nya flexibla bevarandeprincipen ska skickas.
* Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.
* Cmdletar har uppdaterats, inklusive: 
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.