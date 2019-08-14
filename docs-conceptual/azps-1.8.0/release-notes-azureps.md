---
ms.openlocfilehash: faf9313d642a3ca45731f4527aafdfd7f5096a78
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861272"
---
## <a name="180---april-2019"></a>1.8.0 – april 2019
### <a name="highlights-since-the-last-major-release"></a>Höjdpunkter sedan den senaste större uppdateringen
* Allmän tillgänglighet för `Az`-modulen
* Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce
* Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till
* Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till
* Stöd för Python 2-runbookflöden i Az.Automation har lagts till
* Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration

#### <a name="azaccounts"></a>Az.Accounts
* Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt

#### <a name="azbatch"></a>Az.Batch
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azcdn"></a>Az.Cdn
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azcompute"></a>Az.Compute
* Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.
* Åtgärda dokumentationen för jokertecken

#### <a name="azdatafactory"></a>Az.DataFactory
* Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azeventgrid"></a>Az.EventGrid
* Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.

#### <a name="azeventhub"></a>Az.EventHub
* Nya cmdletar har lagts till för NetworkRuleSet för namnområden 

#### <a name="azhdinsight"></a>Az.HDInsight
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="aziothub"></a>Az.IotHub
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azkeyvault"></a>Az.KeyVault
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.
* Åtgärda dokumentationen för jokertecken

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azmedia"></a>Az.Media
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azmonitor"></a>Az.Monitor
  * Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * Monitor SDK har uppdaterats till version 0.22.0-preview

#### <a name="aznetwork"></a>Az.Network
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.
* Åtgärda dokumentationen för jokertecken

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.
* Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats
* En alternativ metod för att hämta platser i AzureFileShare har lagts till
* ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon

#### <a name="azrediscache"></a>Az.RedisCache
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.

#### <a name="azresources"></a>Az.Resources
* Åtgärda dokumentationen för jokertecken

#### <a name="azsql"></a>Az.Sql
* Ersätt Monitor SDK-beroende med vanlig kod
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.
* Förbättrad process för klassificering av flera kolumner.
* Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.
* Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.
* Stöd för tidszonsparametern när hanterade instanser skapas.
* Åtgärda dokumentationen för jokertecken

#### <a name="azwebsites"></a>Az.Websites
* åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning
* Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.
* SDK för WebSites har uppdaterats.
* Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.

## <a name="170---april-2019"></a>1.7.0 – april 2019
### <a name="highlights-since-the-last-major-release"></a>Höjdpunkter sedan den senaste större uppdateringen
* Allmän tillgänglighet för `Az`-modulen
* Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce
* Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till
* Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till
* Stöd för Python 2-runbookflöden i Az.Automation har lagts till
* Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration

#### <a name="azaccounts"></a>Az.Accounts
* Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort
* Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring

#### <a name="azautomation"></a>Az.Automation
* Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats. Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.
* Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation

#### <a name="azcompute"></a>Az.Compute
* Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig
* Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer. 

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK-versionen har uppdaterats till 3.0.2
* Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.

#### <a name="azresources"></a>Az.Resources
* Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls
* Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”
    - Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället
    - Mer information här: https://github.com/Azure/azure-powershell/issues/6856
* Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier
    - Mer information här: https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* Stöd för dataklassificering av databaser.

#### <a name="azstorage"></a>Az.Storage
* Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot
    - New-AzStorageContext
* Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 – mars 2019
### <a name="highlights-since-the-last-major-release"></a>Höjdpunkter sedan den senaste större uppdateringen
* Allmän tillgänglighet för `Az`-modulen
* Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce
* Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till
* Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till
* Stöd för Python 2-runbookflöden i Az.Automation har lagts till
* Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration

#### <a name="azautomation"></a>Az.Automation
* Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:
    * Dynamisk gruppering
    * För-/efterskrift
    * Inställning för omstart

#### <a name="azcompute"></a>Az.Compute
* Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData
* Uppdatera Compute-klientbibliotek till 25.0.0.

#### <a name="azkeyvault"></a>Az.KeyVault
* Stöd för jokertecken för KeyVault-cmdletar har lagts till

#### <a name="aznetwork"></a>Az.Network
* Lägg till stöd för Threat Intelligence för Azure Firewall
* Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP
* Pipe-stöd för avregistrering av container har lagts till

#### <a name="azresources"></a>Az.Resources
* Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup
* Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM

#### <a name="azsql"></a>Az.Sql
* Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.

#### <a name="azstorage"></a>Az.Storage
* Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots' 

## <a name="150---march-2019"></a>1.5.0 – mars 2019
#### <a name="azaccounts"></a>Az.Accounts
* Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar
* Uppdatera exempel för Connect-AzAccount

#### <a name="azautomation"></a>Az.Automation
* Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats
* Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna. Nu returneras alla noder

#### <a name="azcdn"></a>Az.Cdn
* Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella

#### <a name="azcompute"></a>Az.Compute
* Lägg till stöd för jokertecken för Get-cmdletar

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK-versionen har uppdaterats till 3.0.1

#### <a name="azlogicapp"></a>Az.LogicApp
* Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat

#### <a name="aznetwork"></a>Az.Network
* Lägg till stöd för jokertecken för Network-cmdletar

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Stöd har lagts till för SQL Server i virtuella Azure-datorer
* SDK-uppdatering
* Get-ProtectableItem-incheckning i VMappContainer har tagits bort
* Name och ServerName har lagts till som parametrar för Get-ProtectableItem

#### <a name="azresources"></a>Az.Resources
* Lägg till parametern `-TemplateObject` i cmdletar för distribution
    - Mer information här: https://github.com/Azure/azure-powershell/issues/2933
* Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`
    - Mer information här: https://github.com/Azure/azure-powershell/issues/8240
* Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs
    - Mer information här: https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* AuditingEndpointsCommunicator uppdateras.
    - Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.

#### <a name="azstorage"></a>Az.Storage
* Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 – februari 2019
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Inaktuell AddAzureASAccount-cmdlet

#### <a name="azautomation"></a>Az.Automation
* Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats
* Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration
* Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.

#### <a name="azcompute"></a>Az.Compute
* Problemet med ID-parameteruppsättningar har åtgärdats
* Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts
* Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage
* Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL

#### <a name="azeventhub"></a>Az.EventHub
* Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub 

#### <a name="azkeyvault"></a>Az.KeyVault
* Taggning i Set-AzKeyVaultSecret har åtgärdats

#### <a name="azlogicapp"></a>Az.LogicApp
* Grundläggande SKU har lagts till för Integrationskonton
* XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till
* Nya cmdletar för integrationskontosammansättningar
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* Nya cmdletar för batchkonfiguration för integrationskonto
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* Logic App-SDK har uppdaterats till version 4.1.0

#### <a name="azmonitor"></a>Az.Monitor
* Hjälpen för Get-AzMetric har uppdaterats

#### <a name="aznetwork"></a>Az.Network
* Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Ytterligare stöd för datakällorna New och Get ApplicationInsights.
    - Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta. 
    - Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name. 

#### <a name="azresources"></a>Az.Resources
* Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166
* Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235
* Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219
* Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats

#### <a name="azsql"></a>Az.Sql
* Lägg till stöd för hyperskalanivån för SQL DB
* Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan

#### <a name="azwebsites"></a>Az.Websites
* Rätt exempel i Get-AzWebAppSlotMetrics

## <a name="130---february-2019"></a>1.3.0 – februari 2019
#### <a name="azaccounts"></a>Az.Accounts
* Uppdatera till den senaste versionen av ClientRuntime

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Allmän tillgänglighet för Az.AnalysisServices-modulen.

#### <a name="azcompute"></a>Az.Compute
* AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar
* Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics
* Uppdatera hjälpbeskrivning och exempel för Update-AzImage

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Allmän tillgänglighet för Az.RecoveryServices-modulen.

#### <a name="azresources"></a>Az.Resources
* Korrigera taggar för resursgrupper 
    - Mer information här: https://github.com/Azure/azure-powershell/issues/8166
* Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction 
    - Mer information här: https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy
* Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto
* Åtgärda nullref-undantag i Get-AzSqlCapability

## <a name="121---january-2019"></a>1.2.1 – januari 2019
#### <a name="azaccounts"></a>Az.Accounts
* Version med rätt version av autentisering

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Version med uppdaterat autentiseringsberoende

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Version med uppdaterat autentiseringsberoende

## <a name="120---january-2019"></a>1.2.0 – januari 2019
#### <a name="azaccounts"></a>Az.Accounts
* Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1
* Uppdatera felaktiga URL:er för onlinehjälp
* Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm

#### <a name="azaks"></a>Az.Aks
* Uppdatera felaktiga URL:er för onlinehjälp

#### <a name="azautomation"></a>Az.Automation
* Stöd för Python 2-runbookflöden har lagts till
* Uppdatera felaktiga URL:er för onlinehjälp

#### <a name="azcdn"></a>Az.Cdn
* Uppdatera felaktiga URL:er för onlinehjälp

#### <a name="azcompute"></a>Az.Compute
* Lägga till cmdleten Invoke-AzVMReimage
* Lägga till TempDisk-parameter i Set-AzVmss
* Korrigera varningsmeddelande för New-AzVM

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Uppdatera felaktiga URL:er för onlinehjälp

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK-versionen har uppdaterats till 3.0.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Åtgärda problem med ADLS-slutpunkt vid användning av MSI
    - Mer information här: https://github.com/Azure/azure-powershell/issues/7462
* Uppdatera felaktiga URL:er för onlinehjälp

#### <a name="aziothub"></a>Az.IotHub
* Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.

#### <a name="azkeyvault"></a>Az.KeyVault
* Uppdatera felaktiga URL:er för onlinehjälp

#### <a name="aznetwork"></a>Az.Network
* Uppdatera felaktiga URL:er för onlinehjälp

#### <a name="azresources"></a>Az.Resources
* Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”
* Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs
* Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode
* Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522
* Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747
* Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”
    - Mer information här: https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932
* Korrigera några felmeddelanden.
* Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.
* Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.

#### <a name="azsignalr"></a>Az.SignalR
* Uppdatera felaktiga URL:er för onlinehjälp

#### <a name="azsql"></a>Az.Sql
* Uppdatera felaktiga URL:er för onlinehjälp
* Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden
* Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen
* Stöd för anpassad sortering på hanterad instans

#### <a name="azstorage"></a>Az.Storage
* Uppdatera felaktiga URL:er för onlinehjälp
* Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Uppdatera felaktiga URL:er för onlinehjälp

#### <a name="azwebsites"></a>Az.Websites
* Uppdatera felaktiga URL:er för onlinehjälp
* Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.
* Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app

## <a name="110---january-2019"></a>1.1.0 – januari 2019
#### <a name="azaccounts"></a>Az.Accounts
* Lade till omfattningen ”Lokal” till Enable-AzureRmAlias

#### <a name="azcompute"></a>Az.Compute
* Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage
* Uppdaterade beskrivningen av ID i hjälpfiler
* Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.
    - Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken

#### <a name="azeventgrid"></a>Az.EventGrid
* Uppdaterat för användning av API-versionen 2019-01-01.
* Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01
    - New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:
        - Time-To-Live för händelse,
        - Maximalt antal leveransförsök för händelserna,
        - Slutpunkt för obeställbar meddelanden.
    - Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:
        - Time-To-Live för händelse,
        - Maximalt antal leveransförsök för händelserna,
        - Slutpunkt för obeställbar meddelanden.
* Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.
* Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.

#### <a name="aziothub"></a>Az.IotHub
* Har uppdaterats till den senaste versionen av SDK:n lotHub

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzLogicApp visar en lista över alla som inte har angivet namn

#### <a name="azresources"></a>Az.Resources
* Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource
    - Mer information här: https://github.com/Azure/azure-powershell/issues/7875
* Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition
* Korrigerade stavfel i New-AzDeployment-dokumentationen
* Gjorde parametern -MailNickname obligatorisk för New-AzADUser
    - Mer information här: https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts

#### <a name="azsql"></a>Az.Sql
* Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.

#### <a name="azstorage"></a>Az.Storage
* Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous
    - New-AzStorageContext
* Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp
* Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts

## <a name="100---december-2018"></a>1.0.0 – december 2018
### <a name="general"></a>Allmänt

- Allmän tillgänglighet för Az-modulen
- Onlinehjälp för varje modul
- Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)
- Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azaccounts"></a>Az.Accounts
- Har ändrats från Az.Profile
- Fasta tabellformat för profil- och kontexttyper

### <a name="azapimanagement"></a>Az.ApiManagement
- Korrigeringar för #7002
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azbatch"></a>Az.Batch
- Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.
- Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azbilling"></a>Az.Billing
- Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azcognitivservices"></a>Az.CognitivServices
- Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount
- Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- Stöd för ManagedIdentity

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azmonitor"></a>Az.Monitor
- Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azkeyvault"></a>Az.KeyVault
- Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper

### <a name="azmachinelearning"></a>Az.MachineLearning
- Inkluderade cmdletarna från modulen Az.MachineLearningCompute

### <a name="azmedia"></a>Az.Media
- Tog bort inaktuella -Tags-alias från New-AzMediaService

### <a name="aznetwork"></a>Az.Network
Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway
    - Nya cmdletar har lagts till:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.
    - Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azprofile"></a>Az.Profile
- Modulnamnet har ändrats till Az.Accounts

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azresources"></a>Az.Resources
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azservicefabric"></a>Az.ServiceFabric
- Stöd för specificering av certifikat efter eget namn och tumavtryck
- Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azsignalr"></a>Az.SIgnalR
- Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR

### <a name="azsql"></a>Az.Sql
- Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar
- Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azstorage"></a>Az.Storage
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

### <a name="azwebsites"></a>Az.Websites
- Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)

## <a name="070---december-2018"></a>0.7.0 – december 2018

### <a name="general"></a>Allmänt

* Mindre ändringar för kommande övergång från AzureRM till Az

### <a name="azcompute"></a>Az.Compute

* Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Åtgärdade avslutande snedstreck i domänen för adls-konto

### <a name="azfrontdoor"></a>Az.FrontDoor

* Brutna länkar korrigerades
    - I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.
    - I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.
* Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.

### <a name="azresources"></a>Az.Resources

* Korrigering för https://github.com/Azure/azure-powershell/issues/7679
    - Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.

### <a name="azsql"></a>Az.Sql

* Mindre ändringar för kommande övergång från AzureRM till Az
* Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna
* Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.

### <a name="azstorage"></a>Az.Storage

* Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount
* Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts
    - Start-AzureStorageFileCopy
* Stöd för statisk webbplatskonfiguration
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp och Set-AzureRmWebAppSlot 
    - Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux. Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.

## <a name="061---november-2018"></a>0.6.1 – november 2018

### <a name="azapimanagement"></a>Az.ApiManagement
* Uppdatera beroenden för problemet med typmappning

### <a name="azautomation"></a>Az.Automation
* Swagger baserade Azure Automation-cmdletar
* Cmdletar för Uppdateringshantering har lagts till
* Cmdletar för källkontroll har lagts till
* Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till
* Kommandot för DSC-registreringsnod har åtgärdats

### <a name="azcompute"></a>Az.Compute
* Problem med SystemAssigned-identitet har åtgärdats
* Uppdatera beroenden för problemet med typmappning

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Uppdatera beroenden för problemet med typmappning

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* uppdatera exempelbeskrivningen för marketplace-cmdletar

### <a name="aznetwork"></a>Az.Network
* Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till
* ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till
* Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port. 
* Åtgärda problem med minnesanvändning i VirtualNetwork-karta

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Åtgärda för att ändra principen för en skyddad fildelning.
* Tidszonsprincipen har konverterats till versaler.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats
* Uppdatera beroenden för problemet med typmappning

### <a name="azrelay"></a>Az.Relay
* Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.

### <a name="azresources"></a>Az.Resources
* Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`
* Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata
* Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703

### <a name="azservicefabric"></a>Az.ServiceFabric
* Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar

### <a name="azsql"></a>Az.Sql
* Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.
    - Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.
    - Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats

## <a name="050---november-2018"></a>0.5.0 – november 2018
#### <a name="general"></a>Allmänt
* Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar

#### <a name="azprofile"></a>Az.Profile
* Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime
* Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId
* Uppdaterade TenantId-beskrivningen för Connect-AzAccount
* Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän
    - https://github.com/Azure/azure-powershell/issues/6936
* Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen
    - https://github.com/Azure/azure-powershell/issues/7453
* Åtgärda problem med DataLake-slutpunkter vid användning av MSI
    - https://github.com/Azure/azure-powershell/issues/7462
* Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Lade till åtgärden Get-AzCognitiveServicesAccountSkus.

#### <a name="azcompute"></a>Az.Compute
* Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk
* Get-AzVMImage visar AutomaticOSUpgradeProperties
* Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Uppdatera DataLake-paketet till 1.1.10.
* Lägg till standardsamtidighet för flertrådade åtgärder.

#### <a name="azinsights"></a>Az.Insights
* Åtgärdade problem #7267 (autoskalningsområde)
    - Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).
* Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas
    - Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning

#### <a name="aznetwork"></a>Az.Network
* PeeringType ändrades till en obligatorisk parameter för följande cmdletar:
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Cmdletar för principreparation har lagts till

#### <a name="azresources"></a>Az.Resources
* Korrigering för https://github.com/Azure/azure-powershell/issues/7402
    - Tillåt att resurser listas med parametern -ResourceId för Get-AzResource

#### <a name="azservicebus"></a>Az.ServiceBus
* Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Åtgärda att lägga till certifikat till Linux-Vmss.
* Åtgärdade Add-AzServiceFabricClusterCertificate
    - Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).
    - Visa undantag korrekt (Azure/service-fabric-issues#1054).
* Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.

## <a name="040---october-2018"></a>0.4.0 – oktober 2018
#### <a name="azprofile"></a>Az.Profile
* Åtgärdade problemet med Get-AzSubscription i CloudShell
* Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime

#### <a name="azcompute"></a>Az.Compute
* Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm
* Argumentslutförare för ResourceName har lagts till i alla cmdletar.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Lägger till stöd för regler för virtuellt nätverk
    - Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.
    - Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.
    - Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.
    - Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.

#### <a name="aznetwork"></a>Az.Network
* Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.
* Argumentslutförare för ResourceName har lagts till i alla cmdletar.

#### <a name="azresources"></a>Az.Resources
* Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot. Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.

## <a name="030---october-2018"></a>0.3.0 – oktober 2018
#### <a name="azurestorage"></a>Azure.Storage
* Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.
    - Get-AzStorageUsage
    
#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.

#### <a name="azcompute"></a>Az.Compute
* Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs
* Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.
* Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* ADF .Net SDK-versionen har uppdaterats till 2.3.0.

#### <a name="aznetwork"></a>Az.Network
* Funktionalitet för NetworkProfile har lagts till. nya cmdletar har lagts till
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Länk för tjänstassociering på modell för undernät har lagts till
* Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till
* Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till

#### <a name="azrediscache"></a>Az.RedisCache
* Tillåt att alla strängar används som storleksparametrar framöver. Lägg till P5 i popup-fönstret PSArgumentCompleter

#### <a name="azresources"></a>Az.Resources
* Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till
* Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare

#### <a name="azsql"></a>Az.Sql
* Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats

#### <a name="azwebsites"></a>Az.Websites
* Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container
* Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows

## <a name="020---september-2018"></a>0.2.0 – september 2018
 Första versionen