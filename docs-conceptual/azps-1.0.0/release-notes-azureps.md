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
* Lägger till stöd för virtuella nätverksregler
    - Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt Azure Data Lake Store-nätverk.
    - Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för det virtuella nätverket till det angivna Data Lake Store-kontot.
    - Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för det virtuella nätverket i det angivna Data Lake Store-kontot.
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