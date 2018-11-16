---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: 1a9d38cd60ba596c085e5ee9f8d815e238362b1f
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2018
ms.locfileid: "51576240"
---
# <a name="release-notes"></a>Viktig information

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

---

# <a name="azure-powershell-570"></a>Azure PowerShell 5.7.0

Azure PowerShell 5.7.0-installationsprogram: [länk](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)

Gallerimodul för ARM-cmdletar: [länk](https://www.powershellgallery.com/packages/AzureRM/5.7.0)

Om du vill installera `AzureRM` från PowerShell-galleriet kör du följande kommando:

```powershell-interactive
Install-Module -Name AzureRM -Repository PSGallery -Force
```

Om du vill uppdatera från en äldre version av `AzureRM` kör du följande kommando:

```powershell-interactive
Update-Module -Name AzureRM
```

## <a name="changes-since-last-release"></a>Ändringar sedan den senaste versionen

#### <a name="general"></a>Allmänt
* Har uppdaterats till den senaste versionen av Azure ClientRuntime

#### <a name="azurestorage"></a>Azure.Storage
* Åtgärda problemet med att det inte går att ladda upp blobar och cmdletar för filer på datorer där FIPS-principen är aktiverad
    - Set-AzureStorageBlobContent
    - Set-AzureStorageFileContent

#### <a name="azurermbilling"></a>AzureRM.Billing
* Ny Get-AzureRmEnrollmentAccount-cmdlet
  - cmdlet för att hämta registreringskonton

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Integrera med Cognitive Services Management SDK, version 4.0.0.
* Lägg till åtgärden Get-AzureRmCognitiveServicesAccountUsage.

#### <a name="azurermcompute"></a>AzureRM.Compute
* `Get-AzureRmVmssDiskEncryptionStatus` stöder krypteringsstatus på datadisknivå
* `Get-AzureRmVmssVmDiskEncryptionStatus` stöder krypteringsstatus på datadisknivå
* Uppdatera för zonelasticitet
* New-AzureRmVm och New-AzureRmVmss (enkel parameteruppsättning) stöder tillgänglighetszoner.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Koppla bort beroendet av SDK:erna Commands.Resources.Rest och ARM/Storage.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Lägg till funktioner för felsökning
* Uppdatera versionen av SDK:n för ADLS-dataplanen till 1.1.2
* Export-AzureRmDataLakeStoreItem – parametrarna PerFileThreadCount och ConcurrentFileCount har gjorts inaktuella och parametern Concurrency har introducerats
* Import-AzureRMDataLakeStoreItem – parametrarna PerFileThreadCount och ConcurrentFileCount har gjorts inaktuella och parametern Concurrency har introducerats
* Get-AzureRMDataLakeStoreItemContent – slutbeteendet för innehåll som är större än 4 MB har åtgärdats
* Set-AzureRMDataLakeStoreItemExpiry – en ny SetRelativeExpiry-parameteruppsättning för att ange relativ förfallotid har introducerats
* Remove-AzureRmDataLakeStoreItem – parametern Clean har gjorts inaktuell.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* AlternameName i New-AzureRmEventHubGeoDRConfiguration har åtgärdats

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Cmdletar för att ta med pipingscenarier har uppdaterats
* Lägg till utfasningsmeddelanden för kommande version med icke-kompatibla ändringar

#### <a name="azurermnetwork"></a>AzureRM.Network
* Åtgärda felmeddelande med Network-cmdletar

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* "Properties" har lagts till i CorrelationFilter för Rules för stöd för customproperties
* Hjälpen om New-AzureRmServiceBusGeoDRConfiguration har uppdaterats och Rules-cmdletutdata har åtgärdats
* Egenskaper för automatisk vidarekoppling i cmdleten New-AzureRmServiceBusQueue och New-AzureRmServiceBusSubscription har åtgärdats

#### <a name="azurermsql"></a>AzureRM.Sql
* Lägg till ny Stop-AzureRmSqlElasticPoolActivity-cmdlet som stöd för att avbryta asynkrona åtgärder på elastisk pool
* Uppdatera svaret för cmdletarna Get-AzureRmSqlDatabaseActivity och Get-AzureRmSqlElasticPoolActivity för att visa mer information i svaret

Ändringar sedan den senaste versionen: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018

## <a name="560---march-2018"></a>5.6.0 – mars 2018

#### <a name="general"></a>Allmänt
* Åtgärda problem med standardresursgrupp i CloudShell
* Åtgärda problem där felaktiga startskript kördes under modulimport

#### <a name="azurermprofile"></a>AzureRM.Profile
* Aktivera MSI-autentisering i scenarier som inte stöds
* Lägg till stöd för användardefinierad hanterad tjänstidentitet

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Problem med rensning av skript i versionen har åtgärdats

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Problem med rensning av skript i versionen har åtgärdats

#### <a name="azurermcompute"></a>AzureRM.Compute
* "New-AzureRmVM" och "New-AzureRmVMSS"har stöd för datadiskar.
* "New-AzureRmVM" och "New-AzureRmVMSS" har stöd för anpassad avbildning efter namn eller efter ID.
* Log Analytics-funktion
    - "Export-AzureRmLogAnalyticRequestRateByInterval"-cmdlet har lagts till
    - "Export-AzureRmLogAnalyticThrottledRequests"-cmdlet har lagts till

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Åtgärda parameteruppsättningsproblem för containerregister och Azure-filvolymmontering

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* SDK:n för ADF .Net har uppdaterats till version 0.6.0-preview som innehåller följande ändringar:
    - Ny AzureDatabricks LinkedService- och DatabricksNotebook-aktivitet har lagts till
    - Egenskaper för headNodeSize och dataNodeSize har lagts till i HDInsightOnDemand LinkedService
    - LinkedService, Dataset, CopySource för SalesforceMarketingCloud har lagts till
    - Stöd har lagts till för SecureOutput i alla aktiviteter
    - Ny BatchCount-egenskap har lagts till i ForEach-aktivitet som styr hur många samtidiga aktiviteter som ska köras
    - Ny filteraktivitet har lagts till
    - Stöd för länkade tjänstparametrar har lagts till

#### <a name="azurermdns"></a>AzureRM.Dns
* Stöd för privata DNS-zoner har lagts till (allmänt tillgänglig förhandsversion)
    - Lägger till möjligheten att skapa DNS-zoner som endast är synliga för de tillhörande virtuella nätverken

#### <a name="azurermnetwork"></a>AzureRM.Network
* Uppdaterar modelltyper för kompatibilitet med DNS-cmdletar.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices
* Ändringar för ASR Azure till Azure Site Recovery (cmdletar stöder för närvarande åtgärder för Enterprise till Enterprise, Enterprise till Azure, HyperV till Azure, VMware till Azure)
    - New-AzureRmRecoveryServicesAsrProtectionContainer
    - New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig
    - Remove-AzureRmRecoveryServicesAsrProtectionContainer
    - Update-AzureRmRecoveryServicesAsrProtectionDirection

#### <a name="azurermstorage"></a>AzureRM.Storage
* Följande parametrar i nya och angivna cmdletar för lagringskonton används inte längre: EnableEncryptionService och DisableEncryptionService, eftersom vilande kryptering är aktiverat som standard och inte kan inaktiveras.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Hjälpen för Remove-AzureRmWebAppSlot har åtgärdats

## <a name="550---march-2018"></a>5.5.0 – mars 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Problem med att importera alias har åtgärdats
* Läs in version 10.0.3 av Newtonsoft.Json sida-vid-sida med version 6.0.8

#### <a name="azurestorage"></a>Azure.Storage
* Supportfunktion för mjuk borttagning
    - Enable-AzureStorageDeleteRetentionPolicy
    - Disable-AzureStorageDeleteRetentionPolicy
    - Get-AzureStorageBlob

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Problem med att importera alias har åtgärdats
* Lägg till stöd för brandväggs- och frågeutskalningsfunktionen, samt stöd för API-versionen 2017-08-01.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Problem med att importera alias har åtgärdats

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Problem med att importera alias har åtgärdats

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Uppdatera notice.txt och aviseringsmeddelandet.

#### <a name="azurermcompute"></a>AzureRM.Compute
* "New-AzureRmVMSS" skriver ut anslutningssträngar i utförligt läge.
* "New-AzureRmVmsssupport"stöder offentliga IP-adresser, belastningsutjämningsregler, inkommande NAT-regler.
* WriteAccelerator-funktion
    - WriteAccelerator-växlingsparametern har lagts till i följande cmdletar: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk
    - OsDiskWriteAccelerator-växlingsparametern har lagts till i följande cmdlet:     Set-AzureRmVmssStorageProfile.
    - Den booleska OsDiskWriteAccelerator-parametern har lagts till i följande cmdletar:     Update-AzureRmVM     Update-AzureRmVmss

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Åtgärda autentiseringskrypteringsfel som orsakade icke-betydande fel för vissa krypteringsåtgärder
* Aktivera integreringskörning som ska delas i en datafabrik

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Lägg till parametern "SetupScriptContainerSasUri" och "Edition" för cmdleten "Set-AzureRmDataFactoryV2IntegrationRuntime" för att aktivera funktioner för anpassad konfiguration och versionsval
* Åtgärda autentiseringskrypteringsfel som orskade icke-betydande fel för vissa krypteringsåtgärder.
* Aktivera integreringskörning som ska delas i en datafabrik

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Problem med att importera alias har åtgärdats

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Exemplet för Set-AzureRmKeyVaultAccessPolicy har åtgärdats

#### <a name="azurermnetwork"></a>AzureRM.Network
* Problem med att importera alias har åtgärdats

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Problem med att importera alias har åtgärdats

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Problem med att importera alias har åtgärdats

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices
* Problem med att importera alias har åtgärdats

#### <a name="azurermresources"></a>AzureRM.Resources
* Problem med att importera alias har åtgärdats

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Egenskapen EnableBatchedOperations har lagts till i kön
* Egenskapen DeadLetteringOnFilterEvaluationExceptions har lagts till i prenumerationer

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Uppdatering av Service Fabric-cmdleten
  - Uppdaterade ARM-mallar
  - Misslyckade åtgärder återställs inte längre
  - Add-AzureRmServiceFabricNodeType
    - Virtuella datorer återgår till standardinställningen för hanterade diskar
    - Befintliga VMSS-undernät används
    - Alla åtgärder är idempotenta
  - Remove-AzureRmServiceFabricNodeType rensar delvis skapade skalningsuppsättningar för virtuella datorer och/eller klusternodtyper
  - Utdata för PSCluster-objekt har åtgärdats för komplexa egenskapstyper

#### <a name="azurermsql"></a>AzureRM.Sql
* Problem med att importera alias har åtgärdats
* Get-AzureRmSqlServer-, New-AzureRmSqlServer- och Remove-AzureRmSqlServer-svar omfattar nu egenskapen FullyQualifiedDomainName.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Problem med att importera alias har åtgärdats
* New-AzureRMWebApp – parameteruppsättning har lagts till för att förenkla processen att skapa WebApp, med stöd för lokal git-lagringsplats.

## <a name="540---february-2018"></a>5.4.0 – februari 2018
#### <a name="azurermautomation"></a>AzureRM.Automation
* Alias från New-AzureRmAutomationModule till Import-AzureRmAutomationModule har lagts till

#### <a name="azurermcompute"></a>AzureRM.Compute
* Åtgärda ErrorAction-problem för vissa Get-cmdletar.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Tillämpa SDK för Azure Container-instans, 2018-02-01
    - Stöd för DNS-namnetikett

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Alla GET-cmdletar som tidigare inte fungerade har åtgärdats.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Åtgärda bugg i Get-AzureRmEventHubGeoDRConfiguration-hjälpen

#### <a name="azurermnetwork"></a>AzureRM.Network
* Cmdlet för att skapa en ny anslutningsövervakare har lagts till
    - New-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet för att uppdatera en anslutningsövervakare har lagts till
    - Set-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet för att hämta anslutningsövervakaren eller listan för anslutningsövervakaren har lagts till
    - Get-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet för att fråga anslutningsövervakaren har lagts till
    - Get-AzureRmNetworkWatcherConnectionMonitorReport
* Cmdlet för att starta anslutningsövervakaren har lagts till
    - Start-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet för att stoppa anslutningsövervakaren har lagts till
    - Stop-AzureRmNetworkWatcherConnectionMonitor
* Cmdlet för att ta bort anslutningsövervakaren har lagts till
    - Remove-AzureRmNetworkWatcherConnectionMonitor
* Dokumentationen Set-AzureRmApplicationGatewayBackendAddressPool för att ta bort föråldrat exempel har uppdaterats
* EnableHttp2-flagga har lagts till i Application Gateway
    - New-AzureRmApplicationGateway har uppdaterats: den valfria parametern -EnableHttp2 har lagts till
* Lägg till IpTags i PublicIpAddress
    - New-AzureRmPublicIpAddress har uppdaterats: IpTags har lagts till
    - New-AzureRmPublicIpTag för att lägga till Iptag
* Lägg till DisableBgpRoutePropagation-egenskap i RouteTable och effectiveRoute.

#### <a name="azurermresources"></a>AzureRM.Resources
* Registrera-AzureRmProviderFeature: exempel som saknades i dokumenten har lagts till
* Register-AzureRmResourceProvider: exempel som saknades i dokumenten har lagts till

#### <a name="azurermstorage"></a>AzureRM.Storage
* Följande parametrar i nya och angivna cmdletar för lagringskonton används inte längre: EnableEncryptionService och DisableEncryptionService, eftersom vilande kryptering är aktiverat som standard och inte kan inaktiveras.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount


## <a name="530---february-2018"></a>5.3.0 – februari 2018
### <a name="azurermprofile"></a>AzureRM.Profile
* Varning om utfasning har lagts till för PowerShell 3 och 4
* `Add-AzureRmAccount` har bytt namn till `Connect-AzureRmAccount`; ett alias har lagts till för det gamla cmdlet-namnet och andra alias (`Login-AzAccount` och `Login-AzureRmAccount`) har dirigerats om till det nya cmdlet-namnet.
* `Remove-AzureRmAccount` har bytt namn till `Disconnect-AzureRmAccount`; ett alias har lagts till för det gamla cmdlet-namnet och andra alias (`Logout-AzAccount` och `Logout-AzureRmAccount`) har dirigerats om till det nya cmdlet-namnet.
* Resurssträngar har korrigerats så att `Connect-AzureRmAccount` används istället för `Login-AzureRmAccount`
* `Add-AzureRmEnvironment` och `Set-AzureRmEnvironment`
  - `-AzureOperationalInsightsEndpoint` och `-AzureOperationalInsightsEndpointResourceId` har lagts till som parametrar för att användas med OperationalInsights RP-dataplaner.

### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Användning av `Login-AzureRmAccount` har korrigerats för användning av `Connect-AzureRmAccount`

### <a name="azurermcompute"></a>AzureRM.Compute
* Parametern `-AvailabilitySetName` har lagts till i den förenklade parameteruppsättningen för `New-AzureRmVM`.
* Användning av `Login-AzureRmAccount` har korrigerats för användning av `Connect-AzureRmAccount`
* Stöd för användartilldelad identitet för virtuella datorer och VM-skalningsuppsättningar
    - Parametrarna `-IdentityType` och `-IdentityId` läggs till i `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` och `Update-AzureRmVmss`
* Parametern `-EnableIPForwarding` har lagts till i `Add-AzureRmVmssNetworkInterfaceConfig`
* Parametern `-Priority` har lagts till i `New-AzureRmVmssConfig`

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Användning av `Login-AzureRmAccount` har korrigerats för användning av `Connect-AzureRmAccount`

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Användning av `Login-AzureRmAccount` har korrigerats för användning av `Connect-AzureRmAccount`
* Felmeddelandet för `Test-AzureRmDataLakeStoreAccount` har korrigerats när denna cmdlet körs utan att inloggning skett med `Login-AzureRmAccount`

### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Har uppdaterats för att använda API-versionen 2018-01-01.

### <a name="azurermeventhub"></a>AzureRM.EventHub

* De nya kommandona nedan har lagts till för åtgärder för geo-haveriberedskap.
  - Skapar ett nytt alias (haveriberedskapskonfiguration):
    - `New-AzureRmEventHubGeoDRConfiguration`
  - Hämta alias (haveriberedskapskonfiguration):
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - Inaktiverar haveriberedskap och stoppar replikering av ändringar från primära till sekundära namnområden
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - Anropar haveriberedskapsredundans och omkonfigurerar aliaset till att peka på det sekundära namnområdet
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - Tar bort ett alias (haveriberedskapskonfiguration)
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* De nya kommandona nedan har lagts till för att kontrollera namnet på namnområdet och tillgängligheten för GeoDr-konfigurationsnamnet och aliaset.
  - Kontrollera tillgängligheten för namnet på namnområdet eller namnet på aliaset (konfiguration av haveriberedskap):
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a>AzureRM.Insights
* Användning av `Login-AzureRmAccount` har korrigerats för användning av `Connect-AzureRmAccount`

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Användning av `Login-AzureRmAccount` har korrigerats för användning av `Connect-AzureRmAccount`

### <a name="azurermnetwork"></a>AzureRM.Network
* Åtgärda problem med överskrivning av meddelande "Are you sure you want to overwriteresource" (Vill du skriva över resursen)

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Stöd har lagts till för V2 API-frågor via `Invoke-AzureRmOperationalInsightsQuery`. Mer information om det nya API:et finns i [https://dev.loganalytics.io/](https://dev.loganalytics.io/).

### <a name="azurermresources"></a>AzureRM.Resources
* `Get-AzureRmADServicePrincipal`: har tagits bort `-ServicePrincipalName` från standardparameteruppsättningen Empty eftersom den var redundant i SPN-parameteruppsättningen

### <a name="azurermservicebus"></a>AzureRM.ServiceBus

* En funktionsåtgärd har lagts till för `Remove-AzureRmServiceBusRule` och `Get-AzureRmServiceBusKey`
* De nya kommandona nedan har lagts till för åtgärder för geo-haveriberedskap.
  - Skapar ett nytt alias (haveriberedskapskonfiguration):
    - `New-AzureRmServiceBusDRConfigurations`
  - Hämta alias (haveriberedskapskonfiguration):
    - `Get-AzureRmServiceBusDRConfigurations`
  - Inaktiverar haveriberedskap och stoppar replikering av ändringar från primära till sekundära namnområden
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - Anropar haveriberedskapsredundans och omkonfigurerar aliaset till att peka på det sekundära namnområdet
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - Tar bort ett alias (haveriberedskapskonfiguration)
    - `Remove-AzureRmServiceBusDRConfigurations`
* Kommandona `Test-AzureRmServiceBusName` har uppdaterats för att ha stöd tillgänglighetsåtgärder för geo-haveriberedskap och kontroll av aliasnamn.
  - Kontrollera tillgängligheten för namnet på namnområdet eller namnet på aliaset (konfiguration av haveriberedskap):
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Användning av `Login-AzureRmAccount` har korrigerats för användning av `Connect-AzureRmAccount`

## <a name="520---january-2018"></a>5.2.0 – januari 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* Add-AzureRmAccount
  * MSI-inloggning för autentisering har lagts till med autentiseringsuppgifterna för den hanterade tjänstidentiteten för den aktuella virtuella datorn/tjänsten
  * KeyVault-autentisering har åtgärdats när du loggar in med åtkomsttoken från användare

#### <a name="azurestorage"></a>Azure.Storage
* Lägg till cmdletar för att hämta och konfigurera egenskaper för lagringstjänster
    - Get-AzureStorageServiceProperty
    - Update-AzureStorageServiceProperty

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty och New-AzureRmApiManagement

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermautomation"></a>AzureRM.Automation
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för Set-AzureRmAutomationRunbook

#### <a name="azurermbackup"></a>AzureRM.Backup
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermbatch"></a>AzureRM.Batch
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för New-AzureRmCdnEndpoint och New-AzureRmCdnProfile

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Integrera med Cognitive Services Management SDK, version 3.0.0.

#### <a name="azurermcompute"></a>AzureRM.Compute
* En förenklad parameteruppsättning har lagts till i New-AzureRmVmss som skapar en VM-skalningsuppsättning och alla nödvändiga resurser med hjälp av smarta standardinställningar
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för New-AzureRmVm och Update-AzureRmVm
* Cmdleten Get-AzureRmComputeResourceSku har åtgärdats när en zon ingår i begränsningen.
* Konfigurationsschemat har uppdaterats för diagnostikagenten för stöd för Azure Monitor-kanalmottagare.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Stöd för Azure Key Vault har aktiverats i alla tjänster som är länkade till datalager
* Licenstypegenskap för Azure SSIS Integration Runtime har lagts till
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för New-AzureRmDataFactory

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Stöd för Azure Key Vault har aktiverats i alla tjänster som är länkade till datalager
* Licenstypegenskap för Azure SSIS Integration Runtime har lagts till
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* Lägg till parametern ”LicenseType” för kommandot ”Set-AzureRmDataFactoryV2IntegrationRuntime” för att aktivera AHUB-funktioner

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för AzureRmDataLakeAnalyticsAccount och Set-AzureRmDataLakeAnalyticsAccount

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för New-AzureRmDataLakeStoreAccount och Set-AzureRmDataLakeStoreAccount

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermdns"></a>AzureRM.Dns
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Följande nya cmdlet har lagts till:
  - Update-AzureRmEventGridSubscription
    - Uppdatera egenskaperna i en händelseprenumeration i Event Grid.
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurerminsights"></a>AzureRM.Insights
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Lägg till certifikatstöd för IoTHub-cmdletar
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* Stöd för -AsJob för tidskrävande KeyVault-cmdletar har lagts till. Tillåter att valda cmdletar körs i bakgrunden och returnerar ett jobb för att spåra och kontrollera förloppet.
  * Den berörda cmdleten är: Remove-AzureRmKeyVault
* En bugg i Set-AzureRmKeyVaultAccessPolicy där AAD-filtret ställde in SPN till angivet UPN i stället för att ställa in UPN har åtgärdats
  - Se följande problem för mer information: https://github.com/Azure/azure-powershell/issues/5201

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för Update-AzureRmMlCommitmentPlan

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Lägg till parametern IncludeAllResources i cmdleten Remove-AzureRmMlOpCluster
  - Den här växelparametern tar bort alla resurser som ursprungligen skapades med klustret
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermmedia"></a>AzureRM.Media
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för Set-AzureRmMediaService och New-AzureRmMediaService

#### <a name="azurermnetwork"></a>AzureRM.Network
* Stöd har lagts till för -AsJob för tidskrävande Network-cmdletar. Tillåter att valda cmdletar körs i bakgrunden och returnerar ett jobb för att spåra och kontrollera förloppet.
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för New-AzureRmNotificationHubsNamespace och Set-AzureRmNotificationHubsNamespace

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace och Set-AzureRmOperationalInsightsWorkspace

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* Alternativet -UseOriginalStorageAccount har lagts till i cmdleten Restore-AzureRmRecoveryServicesBackupItem.
  - När du aktiverar den här flaggan återställs diskar till sina ursprungliga lagringskonton. Då får användarna återställda virtuella datorer vars konfigurationer är så lika de ursprungliga virtuella datorerna som möjligt.
  - Det bidrar även till att förbättra prestandan för återställningsåtgärden.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* Tre nya cmdletar har lagts till för brandväggsregler
* Tre nya cmdletar har lagts till för geo-replikering
* Stöd för zoner och taggar har lagts till
* Ange ResourceGroup som valfri när det är möjligt.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermresources"></a>AzureRM.Resources
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* Stöd har lagts till för -AsJob för tidskrävande Resources-cmdletar. Tillåter att valda cmdletar körs i bakgrunden och returnerar ett jobb för att spåra och kontrollera förloppet.
* Alias har lagts till för från Get-AzureRmProviderOperation till Get-AzureRmResourceProviderAction för att dessa ska överensstämma med namngivningskonventionerna

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermservermanagement"></a>AzureRM.ServerManagement
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* -Tags har gjorts inaktuell och ersatts med -Tag för New-AzureRmServerManagementNode och New-AzureRmServerManagementGateway

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermsiterecovery"></a>AzureRM.SiteRecovery
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermsql"></a>AzureRM.Sql
* Uppdatera parameterbeskrivningen för granskningskommandon
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* Parametern -AsJob har lagts till för tidskrävande cmdletar
* Parametern -DatabaseName från Get-AzureRmSqlServiceObjective har gjorts inaktuell

#### <a name="azurermstorage"></a>AzureRM.Storage
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* Åtgärda ett problem med null-referenser i körningscmdleten New-AzureRMStorageAccount med parametern -EnableEncryptionService None
* Stöd för -AsJob för tidskrävande Storage-cmdletar har lagts till. Tillåter att valda cmdletar körs i bakgrunden och returnerar ett jobb för att spåra och kontrollera förloppet.
    - Berörda cmdletar är New-, Remove-, Add- och Update- för lagringskonton och nätverksregler för lagringskonton.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Platsifyllning har lagts till i -Location-parametrar vilket möjliggör tabbifyllning via giltiga platser
* ResourceGroup-ifyllning har lagts till i -ResourceGroup-parametrar vilket möjliggör tabbifyllning via resursgrupper i den aktuella prenumerationen
* Stöd för -AsJob har lagts till för tidskrävande Websites-cmdletar. Tillåter att valda cmdletar körs i bakgrunden och returnerar ett jobb för att spåra och kontrollera förloppet.
     - Berörda cmdletar är New-, Remove-, Add- och Set- för WebApps, AppServicePlan och Slots

## <a name="2017128-version-511"></a>2017.12.8, version 5.1.1
* AnalysisServices
  - Ändra verifieringsuppsättningen för platsen till dynamisk sökning så att alla moln stöds.
* Automation
  - Uppdatera till Import-AzureRMAutomationRunbook
    - Nu finns det stöd för Python2-runbookflöden
* Batch
  - Ett fel där kontoåtgärder utan en resursgrupp misslyckades att automatiskt identifiera resursgruppen har åtgärdats
* Compute
  - Get-AzureRmComputeResourceSku visar zoninformation.
  - Uppdatera Disable-AzureRmVmssDiskEncryption för att åtgärda problemet https://github.com/Azure/azure-powershell/issues/5038
  - Stöd för -AsJob för tidskrävande cmdletar för beräkning har lagts till. Tillåter att valda cmdletar körs i bakgrunden och returnerar ett jobb för att spåra och kontrollera förloppet.
    - Berörda cmdletar omfattar: New-, Update-, Set-, Remove-, Start-, Restart- och Stop-cmdletar för Virtual Machines och Virtual Machine Scale Sets
    - En förenklad parameteruppsättning till New-AzureRmVM, som skapar en virtuell dator och alla nödvändiga resurser med hjälp av smarta standardinställningar, har lagts till
* ContainerInstance
  - Tillämpa SDK för Azure Container-instans, 2017-10-01
    - Stöd för att slutföra körning av container
    - Stöd för Azure File-volymmontering
    - Stöd för att öppna flera portar för offentlig IP-adress
* ContainerRegistry
  - Nya cmdletar för geo-replikering och webhooks
    - Get/New/Remove-AzureRmContainerRegistryReplication
    - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* DataFactories
    - Funktioner för kryptering av autentiseringsuppgifter fungerar nu med både ”fjärråtkomst” aktiverat (över nätverket) och ”fjärråtkomst” inaktiverat (lokal dator).
* DataFactoryV2
  - Två nya cmdletar har lagts till: Update-AzureRmDataFactoryV2 och Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
  - En parameter med namnet ScriptParameter för Submit-AzureRmDataLakeAnalyticsJob har lagts till
    - Du kan hitta detaljerad information om ScriptParameter med hjälp av Get-Help på Submit-AzureRmDataLakeAnalyticsJob
  - Parametern MaxDegreeOfParallelism till MaxAnalyticsUnits för New-AzureRmDataLakeAnalyticsAccount har ändrats
    - Ett alias för parametern MaxAnalyticsUnits: MaxDegreeOfParallelism har lagts till
  - Parametern MaxDegreeOfParallelismPerJob till MaxAnalyticsUnitsPerJob för New-AzureRmDataLakeAnalyticsComputePolicy har ändrats
    - Ett alias för parametern MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob har lagts till
  - Parametern MaxDegreeOfParallelism till MaxAnalyticsUnits för Set-AzureRmDataLakeAnalyticsAccount har ändrats
    - Ett alias för parametern MaxAnalyticsUnits: MaxDegreeOfParallelism har lagts till
  - Parametern DegreeOfParallelism till AnalyticsUnits för Submit-AzureRmDataLakeAnalyticsJob har ändrats
    - Ett alias för parametern AnalyticsUnits: DegreeOfParallelism har lagts till
  - Parametern MaxDegreeOfParallelismPerJob till MaxAnalyticsUnitsPerJob för Update-AzureRmDataLakeAnalyticsComputePolicy har ändrats
    - Ett alias för parametern MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob har lagts till
* MachineLearningCompute
  - Lägg till Set-AzureRmMlOpCluster
    - Uppdatera ett klusters agentantal eller SSL-konfiguration
  - Orchestrator-egenskaperna är valfria
    - Tjänsten skapar ett huvudnamn för tjänsten om det inte redan angivits, så orchestrator-egenskaperna är nu valfria
* PowerBIEmbedded
  - Lägg till stöd för cmdletar för Power BI Embedded-kapacitet
  - Ny cmdlet: Get-AzureRmPowerBIEmbeddedCapacity – Hämtar information om PowerBI Embedded-kapaciteten.
  - Ny cmdlet: New-AzureRmPowerBIEmbeddedCapacity – Skapar ny PowerBI Embedded-kapacitet
  - Ny cmdlet: Remove-AzureRmPowerBIEmbeddedCapacity – Tar bort en instans av PowerBI Embedded-kapaciteten
  - Ny cmdlet: Resume-AzureRmPowerBIEmbeddedCapacity – Återupptar en instans av PowerBI Embedded-kapaciteten
  - Ny cmdlet: Suspend-AzureRmPowerBIEmbeddedCapacity – Inaktiverar en instans av PowerBI Embedded-kapaciteten
  - Ny cmdlet: Test-AzureRmPowerBIEmbeddedCapacity – Testar om en instans av PowerBI Embedded-kapaciteten finns eller inte
  - Ny cmdlet: Update-AzureRmPowerBIEmbeddedCapacity – Ändrar en instans av PowerBI Embedded-kapaciteten
* Profil
  - USGovernmentActiveDirectoryEndpoint har uppdaterats till https://login.microsoftonline.us/
    - Mer information om Azure Government-slutpunktsmappningar finns här: https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - Stöd har lagts till för -AsJob för cmdletar, vilket gör det möjligt att köra valda cmdletar i bakgrunden och returnera ett jobb som spårar och kontrollerar förloppet
    - Parametern -AsJob har lagts till för cmdleten Get-AzureRmSubscription
* RecoveryServices.Backup
  - Åtgärdat fel – Get-AzureRmRecoveryServicesBackupItem bör göra skiftlägesokänsliga jämförelser för filtret för containernamnet.
  - Åtgärdat fel – AzureVmItem har nu en egenskap som visar det senaste tillfället då en säkerhetskopiering genomförts – LastBackupTime.
* Resurser
  - Ett problem har åtgärdats med att Get-AzureRMRoleAssignment skapade en tilldelning utan rolldefinitionsnamn för anpassade roller
    - Användarna kan nu använda Get-AzureRMRoleAssignment med tilldelningar som har rolldefinitionsnamn oavsett typ av roll
  - Ett problem har åtgärdats med att Set-AzureRMRoleRoleDefinition visade ett felmeddelande om att fjärrskrivbordet inte hittades när ett nytt omfång fanns i assignablescopes
    - Användarna kan nu använda Set-AzureRMRoleRoleDefinition med tilldelningsbara omfång, inklusive nya omfång oavsett omfångets position
  - Tillåt att omfång slutar med ”/”
    - Användare kan nu använda cmdletarna RoleDefinition och RoleAssignment med omfång som slutar med ”/”, vilket är enhetligt med API och CLI
  - Tillåt att användare skapar RoleAssignment med flaggan för delegering
    - Användarna kan nu använda New-AzureRMRoleAssignment med ett alternativ för att lägga till flaggan för delegering
  - Åtgärda så att RoleAssignment respekterar omfångets parameter
  - Lägg till ett alias för ServicePrincipalName i cmdleten New-AzureRmRoleAssignment
    - Användarna kan nu utnyttja ApplicationId istället för ServicePrincipalName när de använder cmdleten New-AzureRmRoleAssignment
* SiteRecovery
  - Lägg till varningar om utfasning för alla cmdletar i den här modulen som förberedelse för nästa version med stora ändringar.
    - Guiden om kommande stora ändringar innehåller mer information om hur du migrerar dina cmdletar från AzureRM.
* SQL
  - Möjlighet att byta namn på databaser med hjälp av Set-AzureRmSqlDatabase har lagts till
  - Åtgärdat problem https://github.com/Azure/azure-powershell/issues/4974
    - Det genererar inte längre ett fel att ange ett ogiltigt värde för AUDIT_CHANGED_GROUP för cmdletar för granskning och detta kommer att tas bort i en kommande version.
  - Åtgärdat problem https://github.com/Azure/azure-powershell/issues/5046
    - Parametern AuditAction i cmdletar för granskning ignoreras inte längre
  - Ett problem i cmdletar för granskning när ”sekundär” StorageKeyType har angetts har åtgärdats
    - När blobgranskning konfigurerades användes det primära lagringskontots åtkomstnyckel i stället för den sekundära nyckeln när ett "sekundärt" värde för parametern StorageKeyType angavs.
  - Ändrar texten för bekräftelsemeddelandet från Set-AzureRmSqlServerTransparentDataEncryptionProtector
* Azure (RDFE)
    - Alla RemoteApp-cmdletar har tagits bort
* Azure.Storage
    - Uppgradera till Azure Storage-klientbiblioteket 8.6.0 och Azure Storage DataMovement-biblioteket 0.6.5

## <a name="20171110-version-501"></a>2017-11-10 Version 5.0.1
* Problem med sammansättningsinläsning som orsakade att vissa cmdletar misslyckades med att köras i följande moduler har åtgärdats:
  - AzureRM.ApiManagement
  - AzureRM.Backup
  - AzureRM.Batch
  - AzureRM.Compute
  - AzureRM.DataFactories
  - AzureRM.HDInsight
  - AzureRM.KeyVault
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices
  - AzureRM.RedisCache
  - AzureRM.SiteRecovery
  - AzureRM.Sql
  - AzureRM.Storage
  - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>2017-11-08 – version 5.0.0
* Obs! Detta är en viktig ändring. I migreringsguiden (https://aka.ms/azps-migration-guide) finns en fullständig lista över viktiga ändringar som har introducerats.
* Alla cmdletar i AzureRM stöder nu onlinehjälp
  - Kör Get-Help med parametern -Online för att öppna onlinehjälpen i din standardwebbläsare
* AnalysisServices
  * Kommandot Synchronize-AzureAsInstance har åtgärdats så att det fungerar med ny AsAzure REST API för synkronisering
* ApiManagement
  * I migreringsguiden finns information om viktiga ändringar av ApiManagement i den här versionen
  * Cmdleten Get-AzureRmApiManagementUser har uppdaterats för att åtgärda problemet https://github.com/Azure/azure-powershell/issues/4510
  * Cmdleten New-AzureRmApiManagementApi har uppdaterats för att skapa API med en tom sökväg https://github.com/Azure/azure-powershell/issues/4069
* ApplicationInsights
  * Lägg till kommandon för att hämta/skapa/ta bort Application Insights-resurs
    - Get-AzureRmApplicationInsights
    - New-AzureRmApplicationInsights
    - Remove-AzureRmApplicationInsights
  * Lägg till kommandon för att hämta/uppdatera prissättning/dagligt tak för Application Insights-resurs
    - Get-AzureRmApplicationInsights -IncludeDailyCap
    - Set-AzureRmApplicationInsightsPricingPlan
    - Set-AzureRmApplicationInsightsDailyCap
  * Lägg till kommandon för att hämta/skapa/uppdatera/ta bort löpande export av Application Insights-resurs
    - Get-AzureRmApplicationInsightsContinuousExport
    - Set-AzureRmApplicationInsightsContinuousExport
    - New-AzureRmApplicationInsightsContinuousExport
    - Remove-AzureRmApplicationInsightsContinuousExport
  * Lägg till kommandon för att hämta/skapa/ta bort API-nycklar för Application Insights-resurs
    - Get-AzureRmApplicationInsightsApiKey
    - New-AzureRmApplicationInsightsApiKey
    - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
  * Nya parametrar har lagts till för `New-AzureRmBatchAccount`.
    - `PoolAllocationMode`: Allokeringsläget som ska användas för att skapa pooler i Batch-kontot. Om du vill skapa ett Batch-konto som allokerar poolnoder i användarens prenumeration ställer du in detta på `UserSubscription`.
    - `KeyVaultId`: Resurs-ID:t till det Azure-nyckelvalv som är associerat till Batch-kontot.
    - `KeyVaultUrl`: Webbadressen till det Azure-nyckelvalv som är associerat till Batch-kontot.
  * Uppdaterade parametrar till `New-AzureBatchTask`.
    - Switchen `RunElevated` har tagits bort. Parametern `UserIdentity` har lagts till för att ersätta `RunElevated`, och motsvarande beteende kan uppnås om en `PSUserIdentity` byggs enligt nedan:
      - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
      - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
    - Parametern `AuthenticationTokenSettings` har lagts till. Med den här parametern kan du begära att Batch-tjänsten tillhandahåller ett autentiseringstoken till uppgiften när den körs för att undvika behovet av att skicka Batch-kontonycklar till uppgiften för att utfärda begäran för Batch-tjänsten.
    - Parametern `ContainerSettings` har lagts till.
      - Med den här parametern kan du begära att Batch-tjänsten kör uppgiften i en container.
    - Parametern `OutputFiles` har lagts till.
      - Med den här parametern kan du konfigurera uppgiften för att ladda upp filer till Azure Storage när den har avslutats.
  * Parametrar för `New-AzureBatchPool` har uppdaterats.
    - Parametern `UserAccounts` har lagts till.
      - Den här parametern definierar användarkonton som skapats på varje nod i poolen.
    - `TargetLowPriorityComputeNodes` har lagts till, och `TargetDedicated` har bytt namn till `TargetDedicatedComputeNodes`.
      - Ett `TargetDedicated` alias skapades för parametern `TargetDedicatedComputeNodes`.
    - Parametern `NetworkConfiguration` har lagts till.
      - Med den här parametern kan du konfigurera nätverksinställningarna för pooler.
  * Parametrar för `New-AzureBatchCertificate` har uppdaterats.
    - Parametern `Password` är nu en `SecureString`.
  * Parametrar för `New-AzureBatchComputeNodeUser` har uppdaterats.
    - Parametern `Password` är nu en `SecureString`.
  * Parametrar för `Set-AzureBatchComputeNodeUser` har uppdaterats.
    - Parametern `Password` är nu en `SecureString`.
  * Bytte namn på parametern `Name` till `Path` på `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent` och `Remove-AzureBatchNodeFile`.
    - Ett `Name` alias skapades för parametern `Path`.
  * Ändringar av objekt
    - I Batch-ändringsloggen finns en fullständig lista
  * Stöd har lagts till för Azure Active Directory-baserad autentisering.
    - För att använda Azure Active Directory-autentisering hämtar du ett `BatchAccountContext` objekt som använder cmdleten `Get-AzureRmBatchAccount`, och tillhandahåller det `BatchAccountContext` till parametern `-BatchContext` i en cmdlet i Batch-tjänsten. Azure Active Directory-autentisering är obligatoriskt för konton med `PoolAllocationMode = UserSubscription`.
    - För befintliga konton eller för nya konton som skapats med `PoolAllocationMode = BatchService` kan du fortsätta att använda autentisering för delade nycklar genom att hämta ett `BatchAccountContext`-objekt med cmdleten `Get-AzureRmBatchAccoutKeys`.
* Compute
  * Kommandon för Azure Disk Encryption-tillägg
    - Ny parameter för ”Set-AzureRmVmDiskEncryptionExtension”: ”-EncryptFormatAll” som gör det möjligt att kryptera och formatera datadiskar
    - Nya parametrar för ”Set-AzureRmVmDiskEncryptionExtension”: ”-ExtensionPublisherName” och ”-ExtensionType” som gör det möjligt att växla till andra versioner av tillägget
    - Nya parametrar för ”Disable-AzureRmVmDiskEncryption”: ”-ExtensionPublisherName”: ”-ExtensionPublisherName” och ”-ExtensionType” som gör det möjligt att växla till andra versioner av tillägget
    - Nya parametrar för ”Get-AzureRmVmDiskEncryptionStatus”: ”-ExtensionPublisherName” and ”-ExtensionType” som gör det möjligt att växla till andra versioner av tillägget
* DataLakeAnalytics
  * I migreringsguiden finns information om viktiga ändringar av DataLakeAnalytics i den här versionen
  * En av två OutputTypes i Get-AzureRmDataLakeAnalyticsAccount har ändrats
    - List\<DataLakeAnalyticsAccount> till List\<PSDataLakeAnalyticsAccountBasic>
    - Egenskaperna för PSDataLakeAnalyticsAccountBasic är en strikt delmängd av egenskaperna i DataLakeAnalyticsAccount
    - Ytterligare egenskaper som finns i DataLakeAnalyticsAccount returneras inte av tjänsten.  Den här ändringen är därför till för att återspegla detta korrekt. Dessa ytterligare egenskaper är fortfarande i PSDataLakeAnalyticsAccountBasic, men de är märkta som föråldrade.
  * En av två OutputTypes i Get-AzureRmDataLakeAnalyticsJob har ändrats
    - List\<JobInformation> till List\<PSJobInformationBasic>
    - Egenskaperna i PSJobInformationBasic är en strikt delmängd av egenskaperna i JobInformation
    - Ytterligare egenskaper som finns i JobInformation returneras inte av tjänsten.  Den här ändringen är därför till för att återspegla detta korrekt. Dessa ytterligare egenskaper är fortfarande i PSJobInformationBasic, men de är märkta som föråldrade.
* DataLakeStore
  * I migreringsguiden finns information om viktiga ändringar av DataLakeStore i den här versionen
  * En av två OutputTypes i Get-AzureRmDataLakeStoreAccount har ändrats
    - List\<PSDataLakeStoreAccount> till List\<PSDataLakeStoreAccountBasic>
    - Egenskaperna för PSDataLakeStoreAccountBasic är en strikt delmängd av egenskaperna i PSDataLakeStoreAccount
    - Ytterligare egenskaper som finns i PSDataLakeStoreAccount returneras inte av tjänsten.  Den här ändringen är därför till för att återspegla detta korrekt. Dessa ytterligare egenskaper är fortfarande i PSDataLakeStoreAccountBasic, men de är märkta som föråldrade.
* DNS
  * Stöd för CAA-posttyper i Azure DNS
    - Stöder alla åtgärder på CAA-posttyp
* EventHub
  * I migreringsguiden finns information om viktiga ändringar av EventHub i den här versionen
* Insikter
  * I migreringsguiden finns information om viktiga ändringar av Insights i den här versionen
* Nätverk
  * I migreringsguiden finns information om viktiga ändringar av Network i den här versionen
  * Cmdlet för att lista tillgängliga internetleverantörer har lagts till för en angiven Azure-region
    - Get-AzureRmNetworkWatcherReachabilityProvidersList
  * Cmdlet har lagts till för att hämta den relativa latenspoängen för internetleverantörer från en angiven plats till Azure-regioner
    - Get-AzureRmNetworkWatcherReachabilityReport
* Profil
  - Set-AzureRmDefault
    - Använd denna cmdlet om du vill ange en standardresursgrupp.  Det gör parametern -ResourceGroup valfri för vissa cmdletar och använder standardvärdet när ingen resursgrupp är angiven
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - Om det finns en angiven resursgrupp i prenumerationen ställs den in på standardvärdet.  Annars skapas resursgruppen och ställs in på standardvärdet.
  - Get-AzureRmDefault
    - Använd denna cmdlet för att hämta den aktuella standardresursgruppen (och andra kommande standardinställningar).
    - ```Get-AzureRmDefault -ResourceGroup```
  - Clear-AzureRmDefault
    - Använd den här cmdleten för att ta bort den aktuella standardresursgruppen
    - ```Clear-AzureRmDefault -ResourceGroup```
  - Add-AzureRmEnvironment och Set-AzureRmEnvironment
    - Lägg till parametern BatchAudience. Den gör att du kan ange Azure Batch Active Directory-målgruppen som ska användas när du hämtar autentiseringstoken för Batch-tjänsten.
* RecoveryServices.Backup
  * Cmdletar för att utföra ögonblicklig filåterställning har lagts till.
    - Get-AzureRmRecoveryServicesBackupRPMountScript
    - Disable-AzureRmRecoveryServicesBackupRPMountScript
  * Versionen av RecoveryServices.Backup SDK har uppdaterats till den senaste
  * Test för Azure VM-arbetsbelastningen har uppdaterats, så att alla nödvändiga konfigurationer för testkörningar görs av testen själva.
  * Korrigeringar https://github.com/Azure/azure-powershell/issues/3164
* RecoveryServices.SiteRecovery
  * Ändringar för ASR VMware till Azure Site Recovery (cmdletar stöder för närvarande åtgärder för Enterprise till Enterprise, Enterprise till Azure, HyperV till Azure)
    - New-AzureRmRecoveryServicesAsrPolicy
    - New-AzureRmRecoveryServicesAsrProtectedItem
    - Update-AzureRmRecoveryServicesAsrPolicy
    - Update-AzureRmRecoveryServicesAsrProtectionDirection
  * Stöd för AAD-baserat valv har lagts till
  * Cmdletar för att hantera VCenter-resurser har lagts till
    - Get-AzureRmRecoveryServicesAsrVCenter
    - New-AzureRmRecoveryServicesAsrVCenter
    - Remove-AzureRmRecoveryServicesAsrVCenter
    - Update-AzureRmRecoveryServicesAsrVCenter
  * Andra cmdletar har lagts till
    - Get-AzureRmRecoveryServicesAsrAlertSetting
    - Get-AzureRmRecoveryServicesAsrEvent
    - New-AzureRmRecoveryServicesAsrProtectableItem
    - Set-AzureRmRecoveryServicesAsrAlertSetting
    - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
    - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
    - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
    - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
  - I migreringsguiden finns information om viktiga ändringar av ServiceBus i den här versionen
* SQL
  * Stöd har lagts till för att ange och avbryta asynkron updateslo-åtgärd för databasen
    - uppdatera befintlig cmdlet Get-AzureRmSqlDatabaseActivity för att returnera DB updateslo-driftsstatus.
    - lägg till ny cmdlet Stop-AzureRmSqlDatabaseActivity för att avbryta den asynkrona updateslo-åtgärden för databasen.
  * Stöd har lagts till för zonredundans för databaser och elastiska pooler
    - Switchparametern ZoneRedundant har lagts till i New-AzureRmSqlDatabase
    - Switchparametern ZoneRedundant har lagts till i Set-AzureRmSqlDatabase
    - Switchparametern ZoneRedundant har lagts till i New-AzureRmSqlElasticPool
    - Switchparametern ZoneRedundant har lagts till i Set-AzureRmSqlElasticPool
  * Stöd för Server DNS-alias har lagts till
    - Lägger till cmdleten Get-AzureRmSqlServerDnsAlias som hämtar server-dns-alias via server- och aliasnamn eller en lista över server-dns-alias för en azure Sql Server.
    - Lägger till cmdleten New-AzureRmSqlServerDnsAlias som skapar ett nytt server-dns-alias för en viss Azure Sql server
    - Lägger till cmdleten Set-AzurermSqlServerDnsAlias som möjliggör uppdatering till en Azure Sql Server mot vilken server-dns-aliaset pekar
    - Lägger till cmdleten Remove-AzureRmSqlServerDnsAlias som tar bort ett server-dns-alias för en Azure Sql Server
* Azure.Storage
  * Uppgradera till Azure Storage-klientbiblioteket 8.5.0 och Azure Storage DataMovement-biblioteket 0.6.3
  * Lägg till stöd för funktion för ögonblicksbild av filresurs
    - Lägg till ”SnapshotTime”-parametern i Get-AzureStorageShare
    - Lägg till ”IncludeAllSnapshot”-parametern till Remove-AzureStorageShare
