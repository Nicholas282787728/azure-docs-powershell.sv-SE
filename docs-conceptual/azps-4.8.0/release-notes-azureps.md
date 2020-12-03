---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 805928a0ecae0982826d961435744c29691d191b
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427946"
---
# <a name="azure-powershell-release-notes"></a>Viktig information om Azure PowerShell

## <a name="480---october-2020"></a>4.8.0 – oktober 2020
#### <a name="azaccounts"></a>Az.Accounts
* Åtgärdat DateTime-parsningsfel i vanliga bibliotek [#13045]

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Cmdleten New-AzCognitiveServicesAccountApiProperty har lagts till.
* Stöd för parametern ApiProperty för New-AzCognitiveServicesAccount och Set-AzCognitiveServicesAccount

#### <a name="azcompute"></a>Az.Compute
* Åtgärdat problem i Update-ASRRecoveryPlan genom att fylla i FailoverTypes
* De valfria parametrarna -Top och -OrderBy har lagts till i cmdleten Get-AzVmImage. 

#### <a name="azdatabricks"></a>Az.Databricks
* Allmän tillgänglighet för modulen Az.Databricks
* Stöd har lagts till för virtuell nätverkspeering

#### <a name="azdatafactory"></a>Az.DataFactory
* Skrivfel har åtgärdats i utdatameddelanden

#### <a name="azeventhub"></a>Az.EventHub
* Den valfria switchparametern TrustedServiceAccessEnabled har lagts till i cmdleten Set-AzEventHubNetworkRuleSet

#### <a name="azhdinsight"></a>Az.HDInsight
* Ett varningsmeddelande om att parametrarna PublicNetworkAccessType och OutboundPublicNetworkAccessType planeras att göras inaktuella har lagts till
* Ett varningsmeddelande om att parametern DefaultStorageAccountName planeras att ersättas med StorageAccountResourceId har lagts till
* Ett varningsmeddelande om att parametern DefaultStorageAccountKey planeras att ersättas med StorageAccountKey har lagts till
* Ett varningsmeddelande om att parametern DefaultStorageAccountType planeras att ersättas med StorageAccountType har lagts till
* Ett varningsmeddelande om att parametern DefaultStorageContainer planeras att ersättas med StorageContainer har lagts till
* Ett varningsmeddelande om att parametern DefaultStorageRootPath planeras att ersättas med StorageRootPath har lagts till

#### <a name="aziothub"></a>Az.IotHub
* SDK för enheter har uppdaterats

#### <a name="azkeyvault"></a>Az.KeyVault
* Detaljerat datum för borttagning av egenskapen SecretValueText har tillhandahållits

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Varningar om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster har uppdaterats

#### <a name="azmonitor"></a>Az.Monitor
* Felet som gjorde att ett varningsmeddelande inte kunde ignoreras har åtgärdats. [#12889]
* Stöd för parametern SkipMetricValidation i aviseringsregelvillkor. Tillåter att du skapar en aviseringsregel för ett anpassat mått som inte har genererats än, genom att göra så att måttverifieringen hoppas över.

#### <a name="aznetwork"></a>Az.Network
* Office365-princip har lagts till för VPNSite-resurs
    - New-AzO365PolicyProperty

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Verifiering av containernamn har lagts till för arbetsbelastningssäkerhetskopior.

#### <a name="azrediscache"></a>Az.RedisCache
* En korrigering har gjorts så att cmdletarna New-AzRedisCache och Set-AzRedisCache inte misslyckas på grund av behörighetsproblem som rör registrering av Microsoft.Cache RP

#### <a name="azsql"></a>Az.Sql
* BackupStorageRedundancy har lagts till i: 
    - Restore-AzureRmSqlDatabase
    - New-AzSqlDatabaseCopy
    - New-AzSqlDatabaseSecondary
* Skiftlägeskänslighet har tagits bort för parametern BackupStorageRedundancy för alla SQL DB-referenser 
* Namnen på BackupStorageRedundancy-varningsmeddelanden har uppdaterats

#### <a name="azstorage"></a>Az.Storage
* Stöd för att aktivera/inaktivera/hämta egenskaper för mjuk borttagning av resurser för filtjänst för ett lagringskonto
    - Update-AzStorageFileServiceProperty
    - Get-AzStorageFileServiceProperty
* Stöd för att visa filresurser inkluderar borttagna filresurser för ett lagringskonto och hämta förbrukning av enskild filresurs
    - ”Get-AzRmStorageShare”
* Stöd för återställning av en borttagen filresurs
    - Restore-AzRmStorageShare
* Cmdletarna för ändring av egenskaper för Blob Service har ändrats. De ursprungliga egenskaperna hämtas inte från servern utan anger bara de ändrade egenskaperna till servern.
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy  
    - "Enable-AzStorageBlobRestorePolicy"
    - "Disable-AzStorageBlobRestorePolicy"
    - ”Update-AzStorageBlobServiceProperty”
* Åtgärdat hjälpproblem för New-AzStorageAccount-parametern -Kind default value [#12189]
* Åtgärdat problem genom att lägga till exempel som visar hur ContentType anges på korrekt sätt i en blobuppladdning [#12989]

## <a name="470---september-2020"></a>4.7.0 – September 2020
#### <a name="azaccounts"></a>Az.Accounts
* Formaterat kommande meddelanden om icke-bakåtkompatibel ändring
* Uppdaterat Azure.Core till 1.4.1

#### <a name="azaks"></a>Az.Aks
* Valideringslogiken för parametern "New-AzAksCluster", "Set-AzAksCluster" och "New-AzAksNodePool" har lagts till på klientsidan. [#12372]
* Stöd har lagts till för tillägg i "New-AzAksCluster". [#11239]
* Cmdlet:arna "Enable-AzAksAddOn" och "Disable-AzAksAddOn" har lagts till för tillägg. [#11239]
* Parametern "GenerateSshKey" har lagts till för "New-AzAksCluster". [#12371]
* API-versionen har uppdaterats till 2020-06-01.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Visade ytterligare juridiska villkor för vissa API:er.

#### <a name="azcompute"></a>Az.Compute
* Den valfria parametern "EncryptionType" har lagts till i "New-AzVmDiskEncryptionSetConfig"
* Nya cmdlet:ar för ny resurs typ: DiskAccess "Get-AzDiskAccess", "New-AzDiskAccess", "Get-AzDiskAccess"
* De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzSnapshotConfig"
* De valfria parametrarna "-DiskAccessId" och "-NetworkAccessPolicy" har lagts till i "New-AzDiskConfig"
* PatchStatus-egenskapen har lagts till i VirtualMachine-instansvyn
* Egenskapen "VMHealth" har lagts till i den virtuella datorns instansvy, vilket är det returnerade objektet när "get-AzVm" anropas med "-Status"
* Fältet "AssignedHost" har lagts till i instansvyerna "Get-AzVM" och "Get-AzVmss". I fältet visas resurs-ID för den virtuella datorinstansen
* Den valfria parametern "-SupportAutomaticPlacement" har lagts till i "New-AzHostGroup" 
* Parametern "-HostGroupId" har lagts till i "New-AzVm" och "New-AzVmss"

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK har uppdaterats till version 4.11.0

#### <a name="azeventhub"></a>Az.EventHub
* Nya kluster-cmdlet:ar – "New-AzEventHubCluster", "Set-AzEventHubCluster", "Get-AzEventHubCluster", "Remove-AzEventHubCluster", "Get-AzEventHubClustersAvailableRegions" har lagts till.
* Åtgärdat för ärende #10722 : Korrigering för tilldelning av enbart lyssning till AuthorizationRule-rättigheter.

#### <a name="azfunctions"></a>Az.Functions
* Möjligheten att skapa v2-funktioner i regioner som inte stöder det har tagits bort.
* Föråldrad PowerShell 6.2. En varning har lagts till när en användare skapar en PowerShell 6.2-funktionsapp som uppmanar till att skapa en PowerShell 7.0-funktionsapp i stället.

#### <a name="azhdinsight"></a>Az.HDInsight
* Stöd för att skapa kluster med automatisk skalningskonfiguration
    - Lägg till den nya parametern "AutoscaleConfiguration" till cmdleten ”New-AzHDInsightCluster”
* Stöd för att använda automatisk skalningskonfiguration i kluster
    - Lägg till ny cmdlet "Get-AzHDInsihgtClusterAutoscaleConfiguration"
    - Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleConfiguration"
    - Lägg till ny cmdlet "Set-AzHDInsihgtClusterAutoscaleConfiguration"
    - Lägg till ny cmdlet "Remove-AzHDInsihgtClusterAutoscaleConfiguration"
    - Lägg till ny cmdlet "New-AzHDInsihgtClusterAutoscaleScheduleCondition"

#### <a name="azkeyvault"></a>Az.KeyVault
* Stöd har lagts till för RBAC-auktorisering [#10557]
* Förbättrad felhantering i "Set-AzKeyVaultAccessPolicy" [#4007]

#### <a name="azkusto"></a>Az.Kusto
* Allmän tillgänglighet för "Az.Kusto"-modulen

#### <a name="aznetwork"></a>Az.Network
* [Viktig ändring] Uppdaterade nedanstående cmdlets för att justera resursens virtuella router och virtuella hubb
    - "New-AzVirtualRouter": 
        - Parametern-HostedSubnet har lagts till för att stödja underordnad resurs för IP-konfiguration
        - -HostedGateway och -HostedGatewayId har tagits bort
    - 'Get-AzVirtualRouter':
        - Parameteruppsättningen har lagts till på prenumerationsnivå
    - "Remove-AzVirtualRouter"
    - "Add-AzVirtualRouterPeer"
    - "Get-AzVirtualRouterPeer"
    - "Remove-AzVirtualRouterPeer"
* Ny cmdlet har lagts till för Azure Express Route-port
    - "New-AzExpressRoutePortLOA"
* Egenskapen RemoteBgpCommunities har lagts till i VirtualNetwork Peering-resursen
* Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.
* Lade till VpnGatewayIpConfigurations till "Get-AzVpnGateway"-utdata
* Åtgärdade bugg för "Set-AzApplicationGatewaySslCertificate" [#9488]
* Parametern "AllowActiveFTP" har lagts till i "AzureFirewall"
* Nedanstående kommandon för funktionen har uppdaterats: Aktivera konfiguration/borttagning för Internetsäkerhet på VirtualWan P2SVpnGateway.
- "New-AzP2sVpnGateway" har uppdaterats": Den valfria växelparametern "EnableInternetSecurityFlag" har lagts till för kunder som anger värdet true för att aktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.
- "Update-AzP2sVpnGateway" har uppdaterats: De valfria växelparametrarna "EnableInternetSecurityFlag" eller "DisableInternetSecurityFlag" har lagts till för kunder som anger värdet true/false för att aktivera/inaktivera Internetsäkerhet på P2SVpnGateway, som ska användas för plats-till-plats-klienter.
* Den nya cmdleten "Reset-AzP2sVpnGateway" har lagts till för att kunder ska kunna återställa/starta om sina VirtualWan-P2SVpnGateway för felsökning.
* Den nya cmdleten "Reset-AzVpnGateway" har lagts till för att kunder ska kunna återställa/starta om VirtualWan VpnGateway för felsökning.
* "Set-AzVirtualNetworkSubnetConfig" har uppdaterats
    - Ange egenskaper för NSG och routningstabell för undernät till null om det anges explicit i parametrarna [#1548] [#9718]

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Åtgärdat borttagningstillståndet för säkerhetskopieringsobjekt.

#### <a name="azresources"></a>Az.Resources
* Lagt till saknad kontroll för Set-AzRoleAssignment
* Attribut som medför icke-bakåtkompatibel ändring har lagts till i parametern "SubscriptionId" i "Get-AzResourceGroupDeploymentOperation"
* Uppdaterat What-If-cmdlets i ARM-mall så att resursändringar av typen 'Ignorera' visas sist
* Åtgärdat serialiseringsproblem med säkra parametrar och matrisparametrar för distributionscmdlets [#12773]

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Nya cmdletar har lagts till för hanterade kluster och nodtyper:
    - "New-AzServiceFabricManagedCluster"
    - "Get-AzServiceFabricManagedCluster"
    - "Set-AzServiceFabricManagedCluster"
    - "Remove-AzServiceFabricManagedCluster"
    - "Add-AzServiceFabricManagedClusterClientCertificate"
    - "Remove-AzServiceFabricManagedClusterClientCertificate"
    - "New-AzServiceFabricManagedNodeType"
    - "Get-AzServiceFabricManagedNodeType"
    - "Set-AzServiceFabricManagedNodeType"
    - "Remove-AzServiceFabricManagedNodeType"
    - "Add-AzServiceFabricManagedNodeTypeVMExtension"
    - "Add-AzServiceFabricManagedNodeTypeVMSecret"
    - "Remove-AzServiceFabricManagedNodeTypeVMExtension"
    - "Restart-AzServiceFabricManagedNodeTyp"
* Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2020-03-01 för aktuell modell och 2020-01-01-förhandsversion för hanterade kluster.

#### <a name="azsql"></a>Az.Sql
* BackupStorageRedundancy har lagts till i "New-AzSqlInstance" och "Get-AzSqlInstance"
* Cmdlet:en "Get-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till
* Cmdlet:en "Enable-AzSqlServerActiveDirectoryOnlyAuthentication" har lagts till
* Force-parametern har lagts till i "New-AzSqlInstance"
* Cmdlet:ar för logguppspelningstjänst för hanterade databaser har lagts till
    - "Start-AzSqlInstanceDatabaseLogReplay"
    - "Get-AzSqlInstanceDatabaseLogReplay"
    - "Complete-AzSqlInstanceDatabaseLogReplay"
    - "Stop-AzSqlInstanceDatabaseLogReplay"
* Cmdlet:en "Get-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till
* Cmdlet:en "Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till
* Cmdlet:en "Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication" har lagts till
* Cmdletarna "New-AzSqlDatabaseImport" och "New-AzSqlDatabaseExport" har uppdaterats för att stödja funktioner för nätverksisolering
* Cmdleten "New-AzSqlDatabaseImportExisting" har lagts till
* Uppdaterade databas-cmdlet:ar som stöder typspecifikation av lagringsenhet för säkerhetskopiering
* Force-parametern har lagts till i "New-AzSqlDatabase"
* Varning för BackupStorageRedundancy-konfiguration har lagts till i utvalda regioner i "New-AzSqlDatabase"
* Uppdaterade ActiveDirectoryOnlyAuthentication-cmdletar för server och instans så att de innehåller ResourceId och InputObject

#### <a name="azstorage"></a>Az.Storage
* Åtgärdade fel vid uppladdning av blob genom uppgradering till Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]
* Stöd för återställning baserat på tidpunkt
    - "Enable-AzStorageBlobRestorePolicy"
    - "Disable-AzStorageBlobRestorePolicy"
    - "New-AzStorageBlobRangeToRestore"
    - "Restore-AzStorageBlobRange"
* Stöd för att hämta status för blobåterställning genom att köra get-AzureRMStorageAccount med parametern -IncludeBlobRestoreStatus 
    - "Get-AzureRMStorageAccount"
* Meddelande om icke-bakåtkompatibel ändring för kommande ändring av cmdlet-utdata har lagts till
    - "Get-AzStorageContainerStoredAccessPolicy"
    - "Set-AzStorageContainerStoredAccessPolicy"
    - "Set-AzStorageAccountManagementPolicy"
    - "Get-AzStorageAccountManagementPolicy"
    - "Add-AzStorageAccountManagementPolicyAction"
    - "New-AzStorageAccountManagementPolicyRule"
* Uppgraderade Microsoft.Azure.Cosmos.Table SDK till 1.0.8

### <a name="thanks-to-our-community-contributors"></a>Tack till våra community-deltagare
* Thomas Van Laere (@ThomVanL), Lägg till Dockerfile-alpine-3.10 (#12911) 
* Lohith Chowdary Chilukuri (@Lochiluk), Uppdatering av Remove-AzNetworkInterfaceIpConfig.md (#12807) 
* Roberth Strand (@roberthstrand), Get-AzResourceGroup – Nytt exempel och rensning (#12828) 
* Ravi Mishra (@inmishrar), uppdatering av Azure Web App-körningsstack till DOTNETCORE (#12833) 
* @jack-education, uppdaterat set-AzVirtualNetworkSubnetConfig för att tillåta att NSG och routningstabell tas bort från undernät (#12351) 
* @hagop-globanet, uppdatering av Add-AzApplicationGatewayCustomError.md (#12784) 
* Joshua Van Daalen (@greenSacrifice)
  * Uppdatering av stavning av egenskaper till egenskaper (#12821) 
  * Uppdatering av New-AzResourceLock.md-exempel (#12806)
* Eragon Riddle (@eragonriddle), korrigerat fältnamn för parameter i exemplet (#12825) 
* @rossifumax, åtgärdat skrivfel i New-AzConfigurationAssignment.md (#12701)

## <a name="461---august-2020"></a>4.6.1 – augusti 2020
#### <a name="azcompute"></a>Az.Compute
* Korrigerade EncryptionAtHost-parametern i New-AzVm för att ta bort standardvärdet FALSE [#12776]

## <a name="460---august-2020"></a>4.6.0 – augusti 2020
#### <a name="azaccounts"></a>Az.Accounts
* Alla offentliga molnmiljöer läses in när slutpunktsidentifieringen inte returnerar AzureCloud (standard) eller andra offentliga miljöer [#12633]
* SubscriptionPolicies har exponerats i Get-AzSubscription [#12551]

#### <a name="azautomation"></a>Az.Automation
* Parametern -RunOn har lagts till i Set-AzAutomationWebhook för att ange en Hybrid Worker-grupp

#### <a name="azcompute"></a>Az.Compute
* Parametern -EncryptionAtHost har lagts till i New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM och Update-AzVmss
* SecurityProfile har lagts till i Get-AzVM och Get-AzVmss
* Växeln -InstanceView har lagts till som valfri parameter i Get-AzHostGroup
* En ny cmdlet, Invoke-AzVmPatchAssessment, har lagts till

#### <a name="azdatafactory"></a>Az.DataFactory
* Saknade egenskaper har lagts till i klassen PSPipelineRun.

#### <a name="azhdinsight"></a>Az.HDInsight
* Stöd för att skapa kluster med funktionen för kryptering under överföring.

#### <a name="azkeyvault"></a>Az.KeyVault
* Varningsmeddelanden har lagts till för planering att inaktivera mjuk borttagning
* Varningsmeddelanden har lagts till för planering att ta bort attributet SecretValueText

#### <a name="azmaintenance"></a>Az.Maintenance
* Valfria schemarelaterade fält har lagts till i New-AzMaintenanceConfiguration
* En ny cmdlet har lagts till för Get-AzMaintenancePublicConfiguration

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Varningar har lagts till om icke-bakåtkompatibla ändringar för cmdletar för tilldelning och definition av hanterade tjänster

#### <a name="azmonitor"></a>Az.Monitor
* Utökade parametern som angetts i Set-AzDiagnosticSetting för separering av aktivering av loggar och mått [#12482]
* Åtgärdat fel för Add-AzMetricAlertRuleV2 vid hämtning av måttavisering från pipelinen

#### <a name="azresources"></a>Az.Resources
* Get-AzPolicyAlias-svaret har uppdaterats för att ta med information som anger om aliaset kan ändras eller inte av Azure Policy.
* Skapade en ny cmdlet, set-AzRoleAssignment
* Get-AzDeploymentManagementGroupWhatIfResult har lagts till för att hämta What-If-resultat för ARM-mall i hanteringsgruppsomfånget
* En ny cmdlet, Get-AzTenantWhatIfResult, har lagts till för att hämta What-If-resultat för ARM-mall i klientorganisationsomfånget
* -WhatIf och -Confirm har åsidosatts för New-AzManagementGroupDeployment och New-AzTenantDeployment för att använda What-If-resultat för ARM-mall
* Beteenden har åtgärdats för -WhatIf och -Confirm för nya cmdletar för distribution så att de stämmer överens med False och 
* Serialiseringsfel har åtgärdats för -TemplateObject och TemplateParameterObject [#1528] [#6292]
* Attribut som medför icke-bakåtkompatibel ändring har lagts till i Get-AzResourceGroupDeploymentOperation för den kommande ändringen av utdatatyp

#### <a name="azsignalr"></a>Az.SignalR
* Fel i hjälpfilerna Restart-AzSignalR och Update-AzSignalR har åtgärdats
* Cmdletarna Update-AzSignalRNetworkAcl och Set-AzSignalRUpstream har lagts till

#### <a name="azstorage"></a>Az.Storage
* Stöd för blobfrågeacceleration
    -  Get-AzStorageBlobQueryResult
    -  New-AzStorageBlobQueryConfig
* Hjälpfil har lagts till, ytterligare beskrivning har lagts till och stavfel har korrigerats
    -  ”Start-AzStorageBlobCopy”
    -  'Get-AzDataLakeGen2Item'
* Problem med att ladda ned blob när relaterad underordnad katalog saknas har åtgärdats [#12592]
    -  ”Get-AzStorageBlobContent”
* Replikeringsprincip för att ange, hämta, ta bort objekt på Storage-konton stöds
    - New-AzStorageObjectReplicationPolicyRule
    - Set-AzStorageObjectReplicationPolicy
    - Get-AzStorageObjectReplicationPolicy
    - Remove-AzStorageObjectReplicationPolicy
* Stöd har lagts till för att aktivera/inaktivera ChangeFeed i Blob Service för ett Storage-konto
    - ”Update-AzStorageBlobServiceProperty”

## <a name="450---august-2020"></a>4.5.0 – augusti 2020
#### <a name="azaccounts"></a>Az.Accounts
* Uppdaterade ”Connect-AzAccount” så att det accepterar parametern ”MaxContextPopulation” [#9865]
* Uppdaterade SubscriptionClient-versionen till 2019-06-01 och visa klientdomäner [#9838]
* Information om hemklientorganisation och managedBy-klientorganisation som stöds för prenumerationen
* Korrigerade modulnamn, versionsinformation i telemetridata
* Justerade SqlDatabaseDnsSuffix och ServiceManagementUrl om miljöns slutpunkt för metadata returnerar ett inkompatibelt värde

#### <a name="azaks"></a>Az.Aks
* Tog bort ”ClientIdAndSecret” för ”ServicePrincipalIdAndSecret” och ställde in ”ClientIdAndSecret” som ett alias [#12381].
* Tog bort ”Get-AzAks”/”New-AzAks”/”Remove-AzAks”/”Set-AzAks” för ”Get-AzAksCluster”/”New-AzAksCluster”/”Remove-AzAksCluster”/”Set-AzAksCluster” och ställde in de ursprungliga som alias [#12373].

#### <a name="azapimanagement"></a>Az.ApiManagement
* Lade till ny cmdlet: ”Add-AzApiManagementApiToGateway”.
* Lade till ny cmdlet: ”Get-AzApiManagementGateway”.
* Lade till ny cmdlet: ”Get-AzApiManagementGatewayHostnameConfiguration”.
* Lade till ny cmdlet: ”Get-AzApiManagementGatewayKey”.
* Lade till ny cmdlet: ”New-AzApiManagementGateway”.
* Lade till ny cmdlet: ”New-AzApiManagementGatewayHostnameConfiguration”.
* Lade till ny cmdlet: ”New-AzApiManagementResourceLocationObject”.
* Lade till ny cmdlet: ”Remove-AzApiManagementApiFromGateway”.
* Lade till ny cmdlet: ”Remove-AzApiManagementGateway”.
* Lade till ny cmdlet: ”Remove-AzApiManagementGatewayHostnameConfiguration”.
* Lade till ny cmdlet: ”Update-AzApiManagementGateway”.
* Lade till den nya valfria parametern [-GatewayId] till cmdleten ”Get-AzApiManagementApi”.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Använde ”Neka” som standardåtgärd för NetworkRules.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Åtgärdade ett problem där ett undantag uppstår när Enum.Parse försöker att tvinga ett null-värde till aktiverade eller inaktiverade uppräkningsvärden [#12344]

#### <a name="azhdinsight"></a>Az.HDInsight
* Stöd för att skapa kluster med funktionen Kryptering under överföring.
    - Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightCluster”
    - Lägg till den nya parametern ”EncryptionInTransit” till cmdleten ”New-AzHDInsightClusterConfig”
* Stöd för att skapa kluster med funktionen privat länk:
    - Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightCluster”
    - Lägg till de nya parametrarna ”PublicNetworkAccessType” och ”OutboundPublicNetworkAccessType” till cmdleten ”New-AzHDInsightClusterConfig”
* Returnerade information om det virtuella nätverket vid anrop till ”New-AzHDInsightCluster” eller ”Get-AzHDInsightCluster”

#### <a name="aznetwork"></a>Az.Network
* Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”
* Lade till bakåtkompatibel ändringar: PeerAddressType-funktioner för privat peering i ”Remove-AzExpressRouteCircutPeeringConfig”.
* Koden ändrades för att ignorera skiftläge för parametrarna AddressPrefixType och PeerAddressType.
* Ändrade varningsmeddelandet för ”New-AzLoadBalancerFrontendIpConfig”, ”New-AzPublicIpAddress” och ”New-AzPublicIpPrefix”.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Lade till alternativet ”-ForceDelete” för ”Remove-AzOperationalInsightsworkspace”
* Lade till ny cmdlet: ”Get-AzOperationalInsightsDeletedWorkspace”
* Lade till ny cmdlet: ”Restore-AzOperationalInsightsWorkspace”

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Förbättrade sättet Azure Backup-containrar/objekt identifieras.

#### <a name="azresources"></a>Az.Resources
* Lade till egenskaperna ”Condition”, ”ConditionVersion” och ”Description” till ”New-AzRoleAssignment”
    - Detta omfattade alla relevanta ändringar av datamodellerna

#### <a name="azsql"></a>Az.Sql
* Korrigerade ett potentiellt fel med skiftlägesokänsliga servernamn i ”New-AzSqlServer” och ”Set-AzSqlServer”
* Korrigerade att fel databasnamn returnerades vid ett befintligt databasfel i ”New-AzSqlDatabaseSecondary”

#### <a name="azstorage"></a>Az.Storage
* Stöd för att skapa container/blob för SAS-token med de nya behörigheterna x, t
    -  ”New-AzStorageBlobSASToken”
    -  ”New-AzStorageContainerSASToken”
* Stöd för att skapa konto för SAS-token med de nya behörigheterna x, t, f
    -  ”New-AzStorageAccountSASToken”
* Stöd för att hämta förbrukning av enskild filresurs
    - ”Get-AzRmStorageShare”

## <a name="440---july-2020"></a>4.4.0 – juli 2020
#### <a name="azaccounts"></a>Az.Accounts
* En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till
* Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]

#### <a name="azaks"></a>Az.Aks
* Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Projektreferensen till autentisering har tagits bort

#### <a name="azautomation"></a>Az.Automation
* Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.

#### <a name="azcompute"></a>Az.Compute
* En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen

#### <a name="azdatafactory"></a>Az.DataFactory
* Globala parametrar har lagts till för Data Factory.

#### <a name="azeventgrid"></a>Az.EventGrid
* Modulen har uppdaterats så att API-version 2020-06-01 används.
* Nya funktioner har lagts till:
    - Indatamappning
    - Schema för händelseleverans
    - Private Link
    - Cloud Event V10 Schema
    - Service Bus-ämne som mål
    - Azure-funktion som mål
    - Webhook-batchbearbetning
    - Säker webhook (AAD-stöd)
    - IpFiltering
* Uppdaterade cmdletar:
    - ”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:
        - Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.
        - Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.
        - Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.
        - Lägg till ny valfri parameter för leveransschema.
    - ”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:
        - Lägg till nya valfria parametrar för att ge stöd för IpFiltering.
    - ”New-AzEventGridTopic”/”New-AzEventGridDomain”:
        - Lägg till nya valfria parametrar för att ge stöd för indatamappning.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Modulen har uppdaterats så att API 2020-05-01 används
* Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser

#### <a name="azhdinsight"></a>Az.HDInsight
* Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.

#### <a name="azmonitor"></a>Az.Monitor
* Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]

#### <a name="aznetwork"></a>Az.Network
* Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats
* Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk
    - ”Get-AzVirtualApplianceSite”
    - ”New-AzVirtualApplianceSite”
    - ”Remove-AzVirtualApplianceSite”
    - ”Update-AzVirtualApplianceSite”
    - ”New-AzOffice365PolicyProperty”
* Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk
    - ”Get-AzNetworkVirtualAppliance”
    - ”New-AzNetworkVirtualAppliance”
    - ”Remove-AzNetworkVirtualAppliance”
    - ”Update-AzNetworkVirtualAppliance”
    - ”Get-AzNetworkVirtualApplianceSku”
    - ”New-AzVirtualApplianceSkuProperty”
* Application Gateway har introducerats i vanliga cmdletar för Private Link
* StorageSync har introducerats i vanliga cmdletar för Private Link
* SignalR har introducerats i vanliga cmdletar för Private Link

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Projektreferensen till autentisering har tagits bort
* Azure Backup-anpassade cmdletar gör text mer korrekt.
* Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.

#### <a name="azresources"></a>Az.Resources
* ”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.
* Cmdleten ”Unregister-AzResourceProvider” har lagts till.

#### <a name="azsql"></a>Az.Sql
* Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”
* En bugg har åtgärdats i cmdletar för dataklassificering.
* Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”

#### <a name="azstorage"></a>Az.Storage
* Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.
* Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess
    -  'New-AzStorageAccount'
    -  'Set-AzStorageAccount'
* Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto
    - ”Update-AzStorageBlobServiceProperty”
* Stöd har lagts till för att visa blobar med blobversioner
    - ”Get-AzStorageBlob”
* Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner
    - ”Get-AzStorageBlob”
    - ”Remove-AzStorageBlob”
* Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12
    - ”Get-AzStorageBlobContent”
    - ”New-AzStorageBlobSASToken”
    - ”Remove-AzStorageBlob”
    - ”Set-AzStorageBlobContent”
    - ”Start-AzStorageBlobCopy”

#### <a name="azstoragesync"></a>Az.StorageSync
* En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01
* En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till
    - ”Set-AzStorageSyncService”
* IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.

#### <a name="azwebsites"></a>Az.Websites
* Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen

## <a name="430---june-2020"></a>4.3.0 – juni 2020
#### <a name="azaccounts"></a>Az.Accounts
* Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”
* Uppdatera förinlästa sammansättningar [#12024], [#11976]
* Uppdaterad Azure.Core-sammansättning
* Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]

#### <a name="azaks"></a>Az.Aks
* Användning av gamla [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)

#### <a name="azbatch"></a>Az.Batch
* Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.
* Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Stöd för att visa kontofunktioner.
* Stöd för att ändra PublicNetworkAccess.

#### <a name="azcompute"></a>Az.Compute
* Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.
* ”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.
* Understatusar har lagts till i VMCustomScriptExtension [#11297]
* ”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.
* Åtgärdat namn för nytt VM-tillägg för SAP

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK har uppdaterats till 4.9.0

#### <a name="azeventhub"></a>Az.EventHub
* Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”

#### <a name="azfunctions"></a>Az.Functions
* Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar

#### <a name="azhdinsight"></a>Az.HDInsight
* Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Uppdaterade SDK-versionen till 1.1.0
* Stöd har lagts till för exportinställningar och hanterad identitet

#### <a name="azmonitor"></a>Az.Monitor
* Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”
* Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]

#### <a name="aznetwork"></a>Az.Network
* Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”
* Nya cmdletar har lagts till för Azure FirewallPolicy
    - ”New-AzFirewallPolicyDnsSetting”
    - Stöd för mål-FQDN i nätverksregler för brandväggsprincip
* Stöd har lagts till för åtgärder i serverdelsadresspooler
    - ”New-AzLoadBalancerBackendAddressConfig”
    - ”New-AzLoadBalancerBackendAddressPool”
    - ”Set-AzLoadBalancerBackendAddressPool”
    - ”Remove-AzLoadBalancerBackendAddressPool”
    - ”Get-AzLoadBalancerBackendAddressPool”
* Namnvalidering har lagts till för ”New-AzIpGroup”
* Nya cmdletar har lagts till för Azure FirewallPolicy
    - ”New-AzFirewallPolicyThreatIntelWhitelist”
* Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.
    - New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.
    - Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.
* ”Update-AzVpnGateway” har uppdaterats
    - Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.
* Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:
    - ”Reset-AzHubRouter”
* Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn
    - Namn ändras för RuleGroup, RuleCollectionGroup och RuleType
    - Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds
* [Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.
* [Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.
* [Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.
* [Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.
* Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway
    - ”New-AzApplicationGatewayPrivateLinkConfiguration”
    - ”Get-AzApplicationGatewayPrivateLinkConfiguration”
    - ”New-AzApplicationGatewayPrivateLinkConfiguration”
    - ”Set-AzApplicationGatewayPrivateLinkConfiguration”
    - ”Remove-AzApplicationGatewayPrivateLinkConfiguration”
    - ”New-AzApplicationGatewayPrivateLinkIpConfiguration”
* Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.
    - ”New-AzVHubRoute”
    - ”New-AzVHubRouteTable”
    - ”Get-AzVHubRouteTable”
    - ”Update-AzVHubRouteTable”
    - ”Remove-AzVHubRouteTable”
* Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.
    - ”New-AzExpressRouteConnection”
    - ”Set-AzExpressRouteConnection”
    - ”New-AzVirtualHubVnetConnection”
    - ”Update-AzVirtualHubVnetConnection”
    - ”New-AzVpnConnection”
    - ”Update-AzVpnConnection”
    - ”New-AzP2sVpnGateway”
    - ”Update-AzP2sVpnGateway”

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]
* ”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace” 
* Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till
    - ”New-AzOperationalInsightsSavedSearch”
    - ”Set-AzOperationalInsightsSavedSearch”

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Backup har fått stöd för att hämta MAB-objekt.
* Azure Site Recovery stöder disktypen ”StandardSSD_LRS”

#### <a name="azresources"></a>Az.Resources
* ”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]
* Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]
* Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”
* Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”
* Cmdletar för ”Test-Az*Deployment” har uppdaterats för att visa bättre felmeddelanden
* Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar

#### <a name="azsql"></a>Az.Sql
* Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory
* Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.
* Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]

#### <a name="azstorage"></a>Az.Storage
* Skapa lagringskonto med RequireInfrastructureEncryption stöds
    -  'New-AzStorageAccount'
* Logiken för inläsning av Azure.Core flyttades till Az.Accounts

#### <a name="azwebsites"></a>Az.Websites
* Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”
* ”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”
* Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats
* Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats
* Stöd har lagts till för att skapa ASP för Linux-appar
* Undantag har lagts till för kloning över resursgrupper

## <a name="420---june-2020"></a>4.2.0 – juni 2020
#### <a name="azaccounts"></a>Az.Accounts
* Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Uppdaterad sammansättningsversion för dataplan-cmdletar

#### <a name="azapimanagement"></a>Az.ApiManagement
* Uppdaterad sammansättningsversion för cmdletar för tjänsthantering

#### <a name="azbilling"></a>Az.Billing
* Uppdaterad sammansättningsversion för förbrukningscmdletar

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll. 

#### <a name="azdatafactory"></a>Az.DataFactory
* Uppdaterad sammansättningsversion för datafabrik V2-cmdletar

#### <a name="azdatashare"></a>Az.DataShare
* Allmän tillgänglighet för modulen ”Az.DataShare”

#### <a name="azdesktopvirtualization"></a>Az.DesktopVirtualization
* Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Uppgraderad SDK till 0.21.0
* Lade till valfria parametrar till 
    - ”New-AzOperationalInsightsSavedSearch”
    - ”Set-AzOperationalInsightsSavedSearch”

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Uppdaterad sammansättningsversion för PowerBI-cmdletar

#### <a name="azprivatedns"></a>Az.PrivateDns
* Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.
* Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup

#### <a name="azresources"></a>Az.Resources
* Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog
* Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript
* Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject
* Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.
* Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar

#### <a name="azsql"></a>Az.Sql
* Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”
* Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”
* Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory

#### <a name="azstorage"></a>Az.Storage
* Uppdaterad sammansättningsversion för dataplan-cmdletar

## <a name="410---may-2020"></a>4.1.0 – maj 2020
### <a name="highlights-since-the-last-release"></a>Höjdpunkter sedan den senaste uppdateringen
* PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7
* Allmän tillgänglighet för Az.Functions 
* Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage

#### <a name="azaccounts"></a>Az.Accounts
* ”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”
* Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+

#### <a name="azaks"></a>Az.Aks
* API-versionen har uppgraderats till 2019-10-01
* Stöds för att skapa AKS med hjälp av Windows-container
* Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”

#### <a name="azapimanagement"></a>Az.ApiManagement
* Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]
* ”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]
* ”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”. PropertyId-parametern har bytt namn till NamedValueId.
* ”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”. PropertyId-parametern har bytt namn till NamedValueId. 
* ”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”. PropertyId-parametern har bytt namn till NamedValueId.
* ”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”. PropertyId-parametern har bytt namn till NamedValueId.
* Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.
* Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.
* Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.
* Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.
* Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.
* Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”
* Cmdleten ”Update-AzApplicationInsights” har skapats
* Cmdletar har skapats för länkat lagringskonto

#### <a name="azbatch"></a>Az.Batch
* Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.
* Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.
* Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.
  - Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”. Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.
* Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.
* När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.
  - Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”. Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.

#### <a name="azcompute"></a>Az.Compute
* Parametern HostId har lagts till för cmdleten ”Update-AzVM”t
* Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.
* Icke-bakåtkompatibla ändringar
    - Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.
    - Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.
    - AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.
    - Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.
    - Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.
    - Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.
* Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats. 

#### <a name="azdatafactory"></a>Az.DataFactory
* CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt
* Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt
* Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.
* Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt

#### <a name="azfunctions"></a>Az.Functions
* Allmän tillgänglighet för ”Az.Functions”-modulen

#### <a name="azhdinsight"></a>Az.HDInsight
* Stöd för diskkryptering med kundhanterad nyckel.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard

#### <a name="aziothub"></a>Az.IotHub
* En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.
* Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]
* En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.
* En cmdlet har lagts till för att anropa en måttfråga om konfiguration.
* Hantera automatisk distribution av IoT Edge i stor skala. Nya cmdlet:ar är:
    - ”Add-AzIotHubDeployment”
    - ”Get-AzIotHubDeployment”
    - ”Remove-AzIotHubDeployment”
    - ”Set-AzIotHubDeployment”
* En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.
* En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.

#### <a name="azkeyvault"></a>Az.KeyVault
* Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”
* Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas
* Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv
* Stöd för BYOK (Bring Your Own Key) har lagts till
    - ”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel
    - ”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format
* ”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats

#### <a name="azmonitor"></a>Az.Monitor
* Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]
* Stöd för WebTest-tillgänglighetskriterier för måttavisering V2
    - ”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till
    - ”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest
* Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]
* Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]
* ”Get-AzLog” har bytt namn till ”Get-AzActivityLog”

#### <a name="aznetwork"></a>Az.Network
* Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras
    - ”New-AzPublicIpAddress”
    - ”New-AzPublicIpPrefix”
    - ”New-AzLoadBalancerFrontendIpConfig”
* Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider
    - Nya cmdletar har lagts till:
        - New-AzSecurityPartnerProvider
        - Remove-AzSecurityPartnerProvider
        - Get-AzSecurityPartnerProvider
        - Set-AzSecurityPartnerProvider
* ”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”
* Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats
* VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.
    - ”New-AzVirtualWan”
    - ”Update-AzVirtualWan”
* Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt
    - ”New-AzPrivateDnsZoneConfig”
    - ”Get-AzPrivateDnsZoneGroup”
    - ”New-AzPrivateDnsZoneGroup”
    - ”Set-AzPrivateDnsZoneGroup”
    - ”Remove-AzPrivateDnsZoneGroup”
* Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”
* Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”
    - Uppdaterad cmdlet:
        - New-AzFirewall

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Äldre kod har uppdaterats för att tillämpa ny genererad SDK
* Cmdletar har tagits bort på grund av föråldrade API:er
    - ”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)
    - ”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)
    - ”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)
* Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”
* Cmdletar har skapats för länkat lagringskonto
* Cmdletar har skapats för kluster och länkad tjänst

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.
* Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.
* Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.
* Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.
* En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.

#### <a name="azresources"></a>Az.Resources
* En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas
* Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt
* Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]
* ”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]
* En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”
* En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”
   - Alias: ”Get-AzSubscriptionDeploymentWhatIf”
* Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar
* Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar
* En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel
* CorrelationId-loggning har lagts till för distributionsfel
* Egenskapen ”error” har lagts till i utdata från distributionsskript
* Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”
* Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview
* GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview
* Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt
    - ”New-AzDeployment”
    - ”New-AzManagementGroupDeployment”
    - ”New-AzResourceGroupDeployment”
    - ”New-AzTenantDeployment”

#### <a name="azservicefabric"></a>Az.ServiceFabric
* En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till

#### <a name="azsql"></a>Az.Sql
* Förbättrade prestanda för:
    - ”Set-AzSqlDatabaseSensitivityClassification”
    - ”Set-AzSqlInstanceDatabaseSensitivityClassification”
    - ”Remove-AzSqlDatabaseSensitivityClassification”
    - ”Remove-AzSqlInstanceDatabaseSensitivityClassification”
    - ”Enable-AzSqlDatabaseSensitivityRecommendation”
    - ”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”
    - ”Disable-AzSqlDatabaseSensitivityRecommendation”
    - ”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”
* Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”
* Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.

#### <a name="azstorage"></a>Az.Storage
* ”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”
* Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation
    - 'Set-AzStorageAccount'
* Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats
    - ”Remove-AzStorageDirectory”
* Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.
    - ”Update-AzStorageAccountNetworkRuleSet”
    - ”Get-AzStorageAccountNetworkRuleSet”
* Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel
    - ”Add-AzStorageAccountNetworkRule”
* Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7
* Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,
    - 'Get-AzDataLakeGen2ChildItem'
* Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering
    -  'New-AzStorageAccount'
    -  'Set-AzStorageAccount'
* Stöd för nya eller listade Kerberos-nycklar för lagringskontot
    -  ”New-AzStorageAccountKey”
    -  ”Get-AzStorageAccountKey”
* Stöd för redundans med lagringskonto
    - ”Invoke-AzStorageAccountFailover”
* Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats
* Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats
* Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar
* Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen
    - ”Get-AzStorageFile”
    - ”Remove-AzStorageFile”
    - ”Get-AzStorageFileContent”
    - ”Set-AzStorageFileContent”
    - ”Start-AzStorageFileCopy”
* Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen
    - ”New-AzStorageDirectory”
    - ”Remove-AzStorageDirectory”
* Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen
    - ”Get-AzStorageShare”
    - ”New-AzStorageShare”
    - ”Remove-AzStorageShare”
* Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen
    - ”Set-AzStorageShareQuota”

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”

#### <a name="azwebsites"></a>Az.Websites
* Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.

## <a name="380---april-2020"></a>3.8.0 – April 2020
### <a name="highlights-since-the-last-release"></a>Höjdpunkter sedan den senaste uppdateringen
* PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7

#### <a name="azaccounts"></a>Az.Accounts
* Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]

#### <a name="azapimanagement"></a>Az.ApiManagement
* Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version
* "Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern

#### <a name="azcdn"></a>Az.Cdn
* Fast ChinaCDN-relaterad prissättning för SKU-visning

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Identitet som stöds, kryptering, UserOwnedStorage

#### <a name="azcompute"></a>Az.Compute
* Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.
* ”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.

#### <a name="aziothub"></a>Az.IotHub
* Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:
    - 'Get-AzIotHubDeviceTwin'
    - 'Update-AzIotHubDeviceTwin'
* En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.
* Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:
    - 'Get-AzIotHubModuleTwin'
    - 'Update-AzIotHubModuleTwin'
* Hantera IoT-automatisk konfiguration av enhetshantering i stor skala. Nya cmdlet:ar är:
    - 'Add-AzIotHubConfiguration'
    - 'Get-AzIotHubConfiguration'
    - 'Remove-AzIotHubConfiguration'
    - 'Set-AzIotHubConfiguration'
* En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.

#### <a name="azkeyvault"></a>Az.KeyVault
* Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv
* Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]
* Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]
* Har lagt till stöd för privat slutpunkt

#### <a name="azmaintenance"></a>Az.Maintenance
* Publicerar slutversion av underhålls-cmdletar för GA

#### <a name="azmonitor"></a>Az.Monitor
* Har lagt till cmdletar för privat länkomfång
    - 'Get-AzInsightsPrivateLinkScope'
    - 'Remove-AzInsightsPrivateLinkScope'
    - 'New-AzInsightsPrivateLinkScope'
    - 'Update-AzInsightsPrivateLinkScope'
    - 'Get-AzInsightsPrivateLinkScopedResource'
    - 'New-AzInsightsPrivateLinkScopedResource'
    - 'Remove-AzInsightsPrivateLinkScopedResource'

#### <a name="aznetwork"></a>Az.Network
* Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.
    - 'New-AzVirtualNetworkGateway'
    - 'Set-AzVirtualNetworkGateway'
    - 'New-AzVirtualNetworkGatewayConnection'
    - 'Set-AzVirtualNetworkGatewayConnection'
* Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites
    - 'New-AzLocalNetworkGateway'
    - 'New-AzVpnSiteLink'
* Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)
    - Lade till 'Set-AzExpressRouteCircuitConnectionConfig'
        - tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties
    - Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'
        - Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix
* Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.
    - New-AzVirtualNetworkGatewayConnection
    - Set-AzVirtualNetworkGatewayConnection

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad
* Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel

#### <a name="azsql"></a>Az.Sql
* Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"
* Stöd för granskning för ett lagringskonto i VNet.

#### <a name="azstorage"></a>Az.Storage
* Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version
* Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras
    - 'New-AzStorageAccount'
    - 'Set-AzStorageAccount'
* Stöd för DataLake Gen2
    - 'New-AzDataLakeGen2Item'
    - 'Get-AzDataLakeGen2Item'
    - 'Get-AzDataLakeGen2ChildItem'
    - 'Move-AzDataLakeGen2Item'
    - 'Set-AzDataLakeGen2ItemAclObject'
    - 'Update-AzDataLakeGen2Item'
    - 'Get-AzDataLakeGen2ItemContent'
    - 'Remove-AzDataLakeGen2Item'

## <a name="0100-preview---april-2020"></a>0.10.0-förhandsversion – April 2020
### <a name="general"></a>Allmänt
* Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub. Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs. Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](/azure-stack/operator/powershell-install-az-module)
* Supportprofil för AZ-moduler 2019-03-01-hybrid:
  - Az.Billing
  - Az.Compute
  - Az.DataBoxEdge
  - Az.EventHub
  - Az.IotHub
  - Az.KeyVault
  - Az.Monitor
  - Az.Network
  - Az.Resources
  - Az.Storage
  - Az.Websites
* Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub
* Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ
* En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](/azure-stack/operator/powershell-install-az-module)

## <a name="370---march-2020"></a>3.7.0 – mars 2020
#### <a name="azaccounts"></a>Az.Accounts
* Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]

#### <a name="azcompute"></a>Az.Compute
* Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:
    - DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference
* Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.
* Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”. [#11354]
* Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg
    - ”Set-AzVMAEMExtension”
    - ”Get-AzVMAEMExtension”
    - ”Remove-AzVMAEMExtension”
    - ”Update-AzVMAEMExtension”
* Åtgärdade fel i exempel på hjälpdokument
* Visade det exakta strängvärdet för VM PowerState i tabellformat.
* ”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad. [#11257]

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK har uppdaterats till 4.8.0
* Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”
* Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”

#### <a name="azhdinsight"></a>Az.HDInsight
* Stöd för att ange en minimal TLS-version som stöds när klustret skapas.

#### <a name="aziothub"></a>Az.IotHub
* Stöd har lagts till för att hantera distribuerade inställningar per enhet. Nya cmdletar:
    - ”Get-AzIotHubDistributedTracing”
    - ”Set-AzIotHubDistributedTracing”

#### <a name="azkeyvault"></a>Az.KeyVault
* Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”

#### <a name="azmonitor"></a>Az.Monitor
* Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”

#### <a name="aznetwork"></a>Az.Network
* Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter
    - ”New-AzVirtualHubVnetConnection”
    - ”Update-AzVirtualHubVnetConnection”
    - ”New-AzVirtualHub”
    - ”Update-AzVirtualHub”
* SQL Management SDK-beroende har tagits bort

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Förbättrade felmeddelanden

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.
* Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning
* Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.
* Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.
* Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare
* Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip

#### <a name="azresources"></a>Az.Resources
* Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]
* Lade till correlationId-loggning för felscenarier
* Liten dokumentationsändring för ”Get-AzResourceLock”. Lade till exempel.
* Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]
* Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)

#### <a name="azsql"></a>Az.Sql
* En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover
* Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till
* Den sparade känslighet rangordningen när kolumner klassificeras i databasen.

#### <a name="azsupport"></a>Az.Support
* Allmän tillgänglighet för ”Az.Support”-modulen

#### <a name="azwebsites"></a>Az.Websites
* Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar
    - ”Get-AzWebAppTrafficRouting”
    - ”Update-AzWebAppTrafficRouting”
    - ”Add-AzWebAppTrafficRouting”
    - ”Remove-AzWebAppTrafficRouting”

## <a name="361---march-2020"></a>3.6.1 – mars 2020
#### <a name="azaccounts"></a>Az.Accounts
* Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]
* Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]
* Az-version har lagts till i UserAgent

#### <a name="azapimanagement"></a>Az.ApiManagement
* Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]
* ”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]
* ”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument
* ”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.

#### <a name="aziothub"></a>Az.IotHub
* Lade till stöd för att hantera enheter i en IoT-hubb. Nya cmdletar:
    - Add-AzIotHubDevice
    - Get-AzIotHubDevice
    - Remove-AzIotHubDevice
    - Set-AzIotHubDevice
* Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb. Nya cmdletar:
    - ”Add-AzIotHubModule”
    - ”Get-AzIotHubModule”
    - ”Remove-AzIotHubModule”
    - ”Set-AzIotHubModule”
* Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.
* Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.
* Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet. Nya cmdletar:
    - ”Get-AzIotHubDeviceParent”
    - ”Set-AzIotHubDeviceParent”
* Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.

#### <a name="azmonitor"></a>Az.Monitor
* Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]

#### <a name="aznetwork"></a>Az.Network
* SQL Management SDK har uppdaterats.
* Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.
    - Fältet ActionsRequired mappar till ActionRequired.
* PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”

#### <a name="azresources"></a>Az.Resources
* Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”
* Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]
* Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]
* Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]
* Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand
* Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer
* ”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan
* Utökade Tag-cmdlets stöder -ResourceId
    - Get-AzTag -ResourceId
    - New-AzTag -ResourceId
    - Remove-AzTag -ResourceId
* Ny Tag-cmdlet har lagts till
    - Update-AzTag -ResourceId
* Flyttade ScopedDeployment från SDK 3.3.0

#### <a name="azsql"></a>Az.Sql
* PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”
* Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser
    - Hämta/ange LTR-princip på en hanterad databas
    - Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats
    - Ta bort en LTR-säkerhetskopia
    - Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas
* MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer
* MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance
* SQL SDK-versionen för Az.Network har ändrats

#### <a name="azstorage"></a>Az.Storage
* AllowProtectedAppendWrite stöds i ImmutabilityPolicy
    - ”Set-AzRmStorageContainerImmutabilityPolicy”
* Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version
    - ”New-AzStorageTable”
    - ”Get-AzStorageTable”

#### <a name="azwebsites"></a>Az.Websites
* Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”
* Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats
* Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen
* Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper
* Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots

## <a name="350---february-2020"></a>3.5.0 – februari 2020
### <a name="highlights-since-the-last-major-release"></a>Höjdpunkter sedan den senaste större uppdateringen
* Uppdaterade telemetri på klientsidan.
* Az.IotHub lade till cmdletar som stöd för att hantera enheter.
* Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.

#### <a name="azaccounts"></a>Az.Accounts
* Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan

#### <a name="azautomation"></a>Az.Automation
* Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Uppdaterade SDK till 7.0
* Förbättrade felmeddelande vid serversvar om tom brödtext

#### <a name="azcompute"></a>Az.Compute
* Tillät tomt värde för ProximityPlacementGroupId under uppdatering

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF

#### <a name="aziothub"></a>Az.IotHub
* Lade till stöd för att hantera enheter i en IoT-hubb. Nya cmdletar:
    - Add-AzIotHubDevice
    - Get-AzIotHubDevice
    - Remove-AzIotHubDevice
    - Set-AzIotHubDevice

#### <a name="azkeyvault"></a>Az.KeyVault
* Åtgärdade duplicerad text för Add-AzKeyVaultKey.md

#### <a name="azmonitor"></a>Az.Monitor
* Åtgärdade beskrivning av cmdleten Get-AzLog.
* En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.
    - Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).

#### <a name="aznetwork"></a>Az.Network
* Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.
* Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.
* Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.
* Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar
    - Inga nya cmdletar har lagts till. Lättar begränsningen för brandväggsprincip på VNet-brandväggar

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Lade till stöd för Restore-as-files för SQL-databaser.

#### <a name="azresources"></a>Az.Resources
* Omstrukturerade cmdletar för malldistribution
    - Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: *-AzManagementGroupDeployment
    - Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: *-AzTenantDeployment
    - Omstrukturerade *-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen
    - Skapade alias *-AzSubscriptionDeployment för *-AzDeployment-cmdletar
* Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts
* Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.
* Återskapade hjälpfiler

#### <a name="azsql"></a>Az.Sql
* Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.
* Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering
* Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp

#### <a name="azstoragesync"></a>Az.StorageSync
* Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.

## <a name="340---february-2020"></a>3.4.0 – februari 2020
### <a name="highlights-since-the-last-major-release"></a>Höjdpunkter sedan den senaste större uppdateringen
* Första Az.CosmosDB-versionen 0.1.0 har släppts
* Stöd för Az.Network ConnectionMonitor V2 har lagts till

#### <a name="azaccounts"></a>Az.Accounts
* Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt
* Uppdatera referensen till Azure Powershell Common till 1.3.5-preview

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct** _ och _ *Set-AzApiManagementProduct**
  - Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472
* **Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till

#### <a name="azcompute"></a>Az.Compute
* Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.
* Lägg till cmdleten Update-AzDiskEncryptionSet
* Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:
    - New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig
* Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.

#### <a name="azdatafactory"></a>Az.DataFactory
* Uppdatera ADF .Net SDK-versionen till 4.7.0

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Lägger till LIST-åtgärder för resurser
* Lägger till funktion för att utföra åtgärder för hälsokontrollsteg

#### <a name="azhdinsight"></a>Az.HDInsight
* Åtgärda dokumentfel för New-AzHDInsightCluster.

#### <a name="azkeyvault"></a>Az.KeyVault
* Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.

#### <a name="aznetwork"></a>Az.Network
* Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.
* Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik
    - Cmdleten New-AzFirewall har uppdaterats:
        - Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till
        - Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”
* Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.
* Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.
* Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till
    - Nya cmdletar har lagts till:
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration
        - New-AzApplicationGatewayRewriteRuleActionSet
* Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas
    - Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation
* Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata
* Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery-stöd för att ta bort en replikerad disk.
* Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.

#### <a name="azresources"></a>Az.Resources
* Gör -Scope valfritt i cmdletarna *-AzPolicyAssignment med standardinställning till kontextprenumeration
* Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift

#### <a name="azsql"></a>Az.Sql
Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.

#### <a name="azstorage"></a>Az.Storage
* Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto
    - New-AzStorageAccount
* Visa RequestId när StorageException inte har ExtendedErrorInformation
* Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState
* Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet

## <a name="330---january-2020"></a>3.3.0 – januari 2020
#### <a name="azaccounts"></a>Az.Accounts
* Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix

#### <a name="azcdn"></a>Az.Cdn
* Information om felsvar visas i New-AzCdnEndpoint-cmdleten

#### <a name="azcompute"></a>Az.Compute
* Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till
  - Hämta gränslagringscontainern
* Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till
  - Skapa en ny gränslagringscontainer
* Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till
  - Ta bort gränslagringscontainern
* Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till
  - Anropa åtgärd för att uppdatera data i gränslagringscontainer
* Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till
  - Hämta gränslagringskontot
* Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till
  - Skapa ett nytt gränslagringskonto
* Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till
  - Ta bort gränslagringskontot
* Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”
  - Anropa åtgärd för att uppdatera resursdata
* Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till
  - Ange autentiseringsuppgifter för az databoxedge-lagringskonto

#### <a name="azdatafactory"></a>Az.DataFactory
* Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd
* Uppdatera ADF .Net SDK-versionen till 4.6.0
* Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md

#### <a name="azeventhub"></a>Az.EventHub
* Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning

#### <a name="azhdinsight"></a>Az.HDInsight
* Åtgärda Invoke-AzHDInsightHiveJob.md-fel.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt
  - Get-AzMlOpCluster
  - Get-AzMlOpClusterKey
  - New-AzMlOpCluster
  - Remove-AzMlOpCluster
  - Set-AzMlOpCluster
  - Test-AzMlOpClusterSystemServicesUpdateAvailability
  - Update-AzMlOpClusterSystemService

#### <a name="aznetwork"></a>Az.Network
* Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.
* Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.
* Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.
* Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.

#### <a name="azresources"></a>Az.Resources
* Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.

#### <a name="azsql"></a>Az.Sql
* Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.
* Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Lägg till DR som en ny giltig licenstyp

#### <a name="azstorage"></a>Az.Storage
* Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version
    - Update-AzStorageAccountNetworkRuleSet
* Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats
    - Get-AzureRMStorageAccount

## <a name="320---december-2019"></a>3.2.0 – December 2019

### <a name="general"></a>Allmänt
* Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler

#### <a name="azaccounts"></a>Az.Accounts
* Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview
* Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview

#### <a name="azbatch"></a>Az.Batch
* Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.

#### <a name="azdatafactory"></a>Az.DataFactory
* Uppdatera ADF .Net SDK-versionen till 4.5.0

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program
* Lägg till SocketAddr för automatisk komplettering

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Undantagshantering

#### <a name="azkeyvault"></a>Az.KeyVault
* Åtgärdat fel vid åtkomst av värde som kanske inte har angetts
* Hantering av ECC-certifikat (Elliptic Curve Cryptography)
    - Stöd har lagts till för att ange kurvan för certifikatprinciper

#### <a name="azmonitor"></a>Az.Monitor
* Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar. Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även dedikerad, datatyp)

#### <a name="aznetwork"></a>Az.Network
* Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.

#### <a name="azresources"></a>Az.Resources
* Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.
* Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.

#### <a name="azsql"></a>Az.Sql
* Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2

#### <a name="azstorage"></a>Az.Storage
* Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering
    - New-AzStorageContainerSASToken
    - New-AzStorageBlobSASToken
* Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token
    - Revoke-AzStorageAccountUserDelegationKeys
* Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.
* Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* Lägg till parameteraliaset QuotaGiB i parametern Quota
    - Set-AzStorageShareQuota
* Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen
    - Set-AzStorageContainerAcl

## <a name="310---november-2019"></a>3.1.0 – November 2019
### <a name="highlights-since-the-last-major-release"></a>Höjdpunkter sedan den senaste större uppdateringen
* Az.DataBoxEdge 1.0.0 har släppts
* Az.SqlVirtualMachine 1.0.0 har släppts

#### <a name="azcompute"></a>Az.Compute
* Funktion för att använda en virtuell dator igen
    - Lägg till parameter för att använda igen till cmdleten Set-AzVM
* Funktionen AutomaticRepairs i VM-skalningsuppsättningar:
    - Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss
* Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM
* Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss
* Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk
* Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri
* Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion
* Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition
* Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till
    - Hämta ordning
* Cmdleten `New-AzDataBoxEdgeOrder` har lagts till
    - Skapa ny ordning
* Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till
    - Ta bort ordning
* Cmdleten `New-AzDataBoxEdgeShare` har ändrats
    - Nu skapas lokal filresurs
* Cmdleten `Set-AzDataBoxEdgeRole` har lagts till
    - Nu kan IotRole mappas till filresursen
* Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till
    - Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten
* Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till
    - Hämtar information om utlösare
* Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till
    - Skapa nya utlösare
* Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till
    - Ta bort utlösare

#### <a name="azdatafactory"></a>Az.DataFactory
* Uppdatera ADF .Net SDK-versionen till 4.4.0
* Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem

#### <a name="azeventhub"></a>Az.EventHub
* Korrigering av problem #10301: Korrigera datumformat för SAS-token

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject
* Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject
* Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.

#### <a name="azprivatedns"></a>Az.PrivateDns
* Uppdaterade PrivateDns .NET SDK till version 1.0.0

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.
* Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.
* Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.

#### <a name="azrediscache"></a>Az.RedisCache
* Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache. Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.
* Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache

#### <a name="azresources"></a>Az.Resources
- Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.
- Uppdaterade hjälpexempel för skapandet av policydefinition
- Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.
- Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.
- Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.

#### <a name="azsql"></a>Az.Sql
* Stöd har lagts till för databasen ReadReplicaCount.
* Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts

## <a name="300---november-2019"></a>3.0.0 – November 2019
### <a name="general"></a>Allmänt
* Az. PrivateDns 1.0.0 har släppts

#### <a name="azaccounts"></a>Az.Accounts
* Lägg till ett utfasningsmeddelande för aliaset Resolve-error.

#### <a name="azadvisor"></a>Az.Advisor
* Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.

#### <a name="azbatch"></a>Az.Batch
* `CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`. Det finns även en ny `LowPriorityCoreQuota`.
  - Detta påverkar **Get-AzBatchAccount**.
* **New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.
* Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt. Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.
  - Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:
    - `AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.
    - `StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.
* Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.
  - Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**. Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.
  - `ApplicationId` är nu ett alias för `ApplicationName`.
* Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.
* Bytte namn på `Version` till `Name` på `PSApplicationPackage`.
* Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.
* Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.
* Tog bort **Set-AzBatchPoolOSVersion**. Den här åtgärden stöds inte längre.
* `TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.
* Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.
* `DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.
* Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.
  - **Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.
  - Nya icke-verifierade avbildningar returneras nu också. Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.
* Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.
* Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik. Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.
* När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften. Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.
* Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`. Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.
* Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).
* Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).

#### <a name="azcdn"></a>Az.Cdn
* Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.
* Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.

#### <a name="azcompute"></a>Az.Compute
* Funktion för diskkrypteringsuppsättning
    - Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk
    - Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig
* Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig
* Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning
* Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss
* Icke-bakåtkompatibla ändringar
    - Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning
    - PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion

#### <a name="azdatafactory"></a>Az.DataFactory
* Uppdatera ADF .Net SDK-versionen till 4.3.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar
* Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.
* Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient
* Korrigera överföringen av ursprunglig syncflag för badoffset-återställning
* Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats
* Korrigera bugg i Concat

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Åtgärdade diverse stavfel i modul

#### <a name="azhdinsight"></a>Az.HDInsight
* Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.
* Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.
* Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0
* Fem cmdletar har tagits bort:
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* Tre cmdletar har lagts till:
    - Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.
    - Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.
    - Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.
* Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.
* Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.
* Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.
* Ändrade utdatatyp för följande cmdletar:
*  - Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.
*  - Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.
*  - Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.
* Lade till testfall för vissa scenarier.
* Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.

#### <a name="aziothub"></a>Az.IotHub
* Icke-bakåtkompatibla ändringar:
    - Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.
    - Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.
    - Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.
    - Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.
    - Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.
    - Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.
    - Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.
    - Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.
    - Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.
    - Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.
    - Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.
    - Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.
* Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.
* Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.
* Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.
* Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.
* Azure Site Recovery-stöd för Standard SSD för Azure till Azure.
* Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.
* Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.
* En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort

#### <a name="azresources"></a>Az.Resources
* Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2

#### <a name="aznetwork"></a>Az.Network
* Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.
    - Uppdaterad cmdlet:
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Set-AzPrivateEndpointConnection
* Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.
    - Ny cmdlet:
        - Get-AzPrivateLinkResource
* Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.
    - Lägg till egenskapen EnableProxyProtocol i PrivateLinkService
    - Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection
    - Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.
* Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku
* Nya cmdletar som stöder Azure-brandväggsprincipen
* Lägg till stöd för den underordnade resursen RouteTables för VirtualHub
    - Nya cmdletar har lagts till:
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan
    - Cmdletar har uppdaterats med valfria parametrar:
        - New-AzVirtualHub: lade till parameter-SKU
        - Update-AzVirtualHub: lade till parameter-SKU
        - New-AzVirtualWan: lade till parametern VirtualWANType
        - Update-AzVirtualWan: lade till parametern VirtualWANType
* Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection
    - Nya cmdletar har lagts till:
        - Update-AzureRmVirtualHubVnetConnection
    - Cmdletar har uppdaterats med valfria parametrar:
        - New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till
        - New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till
        - Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till
        - New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till
        - Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till
* Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip
    - Nya cmdletar har lagts till:
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - Cmdletar har uppdaterats med valfria parametrar:
        - New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till
* Stöd för operator för geomatchning har lagts till på CustomRule
    - Geomatchning har lagts till i operatorn på FirewallCondition
* Stöd har lagts till för brandväggsprinciperna perListener och perSite
    - Cmdletar har uppdaterats med valfria parametrar:
        - New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till
        - New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till
* Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt
* Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall
* Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån
    - Nya cmdletar har lagts till:
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.

#### <a name="azsql"></a>Az.Sql
* Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.
* Inaktuella gamla cmdletar för granskning från kod.
* Tog bort inaktuella alias:
* Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)
* Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)
* Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy
* Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk
* Inaktualisera cmdletar för inställningar för avancerad hotidentifiering
* Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.

#### <a name="azstorage"></a>Az.Storage
* Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle

## <a name="280---october-2019"></a>2.8.0 – oktober 2019
### <a name="general"></a>Allmänt
* AZ. HealthcareApis 1.0.0-version

#### <a name="azaccounts"></a>Az.Accounts
* Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet
    - Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068

#### <a name="azautomation"></a>Az.Automation
* Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.

#### <a name="azbatch"></a>Az.Batch
* **Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.

#### <a name="azcompute"></a>Az.Compute
* Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss
* Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey
* Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.
* Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.

#### <a name="azdatafactory"></a>Az.DataFactory
* Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.
* Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.
* Uppdatera ADF .Net SDK-versionen till 4.2.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Korrigera kontovalidering så att konton med ”-” kan skickas utan domän

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* PowerShell-versionen har uppdaterats till 1.0.0
* Uppdaterade SDK-versionen till 1.0.2
* Uppdatera i tester för att referera till en ny SDK-version
* Utdatastrukturen har uppdaterats från kapslad till förenklad.

#### <a name="aziothub"></a>Az.IotHub
* Lägg till ny routningskälla: DigitalTwinChangeEvents
* Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId

#### <a name="azmonitor"></a>Az.Monitor
* Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver
* Använd vanligt aviseringsschema som är aktiverat för mottagarna. Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare
* Webhooks har nu stöd för Azure Active Directory-autentisering.

#### <a name="aznetwork"></a>Az.Network
* Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.
* Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk
    - Nya cmdletar har lagts till:
        - New-AzureRmTrafficSelectorPolicy
    - Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection
* Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler
    - Uppdaterade cmdletar:
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Förbättra hanteringen av undantag i Cortex-cmdletar
* Nya generationer och SKU:er för VirtualNetworkGateways
  - Introducera nya generationer för VirtualNetworkGateways.
  - Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.

#### <a name="azrediscache"></a>Az.RedisCache
* Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”

#### <a name="azsql"></a>Az.Sql
* Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen

#### <a name="azstorage"></a>Az.Storage
* Uppdatera Lagringsklientbibliotek till 11.1.0
* Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink
    -  Get-AzRmStorageContainer
* Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp – uppdatering av ASP för en app misslyckades

## <a name="270---september-2019"></a>2.7.0 – september 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen
* Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen. Använd ”Set-AzApiManagement” i stället.

#### <a name="azautomation"></a>Az.Automation
* Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”
* Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode
* Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.

#### <a name="azcompute"></a>Az.Compute
* Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig
* Lägg till Incremental-parameter till New-AzSnapshotConfig
* Lägg till en funktion för virtuella datorer med låg prioritet:
    - MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.
    - MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.
* Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.
* Korrigera null-undantaget för Get-AzRemoteDesktopFile.
* Korrigera VHD-metoden för sökning relativt till slut.
* Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.

#### <a name="azdatafactory"></a>Az.DataFactory
* Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus
* ADF .Net SDK har uppdaterats till 4.1.3

#### <a name="azhdinsight"></a>Az.HDInsight
* Anrop för icke-bakåtkompatibla ändringar

#### <a name="aziothub"></a>Az.IotHub
* Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.
* Lägg till stöd för att hantera meddelandeberikning för en IotHub. Nya cmdlet:ar är:
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview
   - Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden. Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.
   - API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**. Test av scenarier har uppdaterats för att anpassas till den här ändringen.
   - Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**. Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna. **Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.
   - Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n. Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.
   - Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n. Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.
* Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2
    - New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde
    - Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde
* Förbättringar i schemalagd frågeregel (SQR)
 - Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)
 - ”Enabled”-parametern illustreras korrekt i hjälpfiler
 - Exempel för den valfria parametern ”ActionGroup” har lagts till
 - Förbättrade hjälpfiler
* Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”

#### <a name="aznetwork"></a>Az.Network
* Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”
* Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling
* Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort
* Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information
* Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag
* Felaktig mappning av säkerhetsregelmodeller har korrigerats
* Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP
    - Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface
    - Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration
    - Modellklassen PSIpConfigurationConnectivityInformation har lagts till
* ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs
* MultiLink-stöd i virtuellt WAN
    - Nya cmdletar
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - Uppdaterad cmdlet:
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut
* Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto

#### <a name="azresources"></a>Az.Resources
* Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen
* Lägger till nya cmdletar för att hantera program och tjänster:
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.

#### <a name="azsignalr"></a>Az.SignalR
* Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar

#### <a name="azsql"></a>Az.Sql
* Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”
* vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.
* Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy
* Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.
* Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).

#### <a name="azstorage"></a>Az.Storage
* Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats
* Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.
    -  Set-AzStorageBlobContent
* Stöd för hantering av Azure-filresurser med API för hanteringsplan
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP
* Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows
* Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen

## <a name="260---august-2019"></a>2.6.0 – augusti 2019
#### <a name="general"></a>Allmänt
* Åtgärdade diverse skrivfel i flera moduler

#### <a name="azaccounts"></a>Az.Accounts
* Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)

#### <a name="azaks"></a>Az.Aks
* Åtgärda problem med utdata för "Get-AzAks"
    * Mer information här: https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351
    - Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId
* **Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752
* Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"

#### <a name="azbatch"></a>Az.Batch
* Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler

#### <a name="azcdn"></a>Az.Cdn
* Åtgärdade skrivfel i CDN-modulens konverteringshjälp

#### <a name="azcompute"></a>Az.Compute
* Lägg till VmssId i New-AzVMConfig-cmdleten
* Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss
* Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator
* Lägg till funktioner för Host och HostGroup
    - Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - HostId-parametern läggs till i New-AzVMConfig och New-AzVM
* Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn
* Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"

#### <a name="azdatafactory"></a>Az.DataFactory
* Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen
* Uppdaterade ADF .Net SDK-versionen till 4.1.2
* Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime
* Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.

#### <a name="azeventhub"></a>Az.EventHub
* Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet
* Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT
* lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten
* Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener

#### <a name="azmonitor"></a>Az.Monitor
* Åtgärdade felaktigt parameternamn i hjälpdokumentationen

#### <a name="aznetwork"></a>Az.Network
* Uppdaterade New-AzPrivateLinkServiceIpConfig
    - Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.
    - Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.
* Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas
* Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.
* Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.
* Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"
    - Lade till exempel
    - Uppdaterade beskrivningen av parametern "-Name"
* Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource
* Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"

#### <a name="azresources"></a>Az.Resources
* Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource
    - Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper
    - Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget
* Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen

#### <a name="azservicebus"></a>Az.ServiceBus
* Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet
* Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet
* Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Åtgärda buggar med tillägg av nodtyps-cmdlet:
    - NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret. Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681
    - Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret. Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407
    - AzServiceFabricApplicationCertificate-cmdleten görs inaktuell

#### <a name="azsql"></a>Az.Sql
* Uppdatera dokumentation om gamla gransknings-cmdletar.

#### <a name="azstorage"></a>Az.Storage
* Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar
* Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Stöd för rehydratiseringsprioritet i kopieringsblob
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot

## <a name="250---july-2019"></a>2.5.0 – July 2019
#### <a name="azaccounts"></a>Az.Accounts
* Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey

#### <a name="azautomation"></a>Az.Automation
* Korrigera skrivfel i resurssträng

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Stöd för NetworkRuleSet har lagts till.

#### <a name="azcompute"></a>Az.Compute
* Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication
    - Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK-versionen har uppdaterats till 4.1.0
* Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun

#### <a name="azeventhub"></a>Az.EventHub
* Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken
* verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats

#### <a name="azkeyvault"></a>Az.KeyVault
* Stöd har lagts till för att ange KeySize för certifikatprinciper

#### <a name="azlogicapp"></a>Az.LogicApp
* Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper
    - Ny MapType-parameter har lagts till för filtrering

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Stöd för API-versionen 2019-06-01 (GA) har lagts till

#### <a name="aznetwork"></a>Az.Network
* Lägg till stöd för privat slutpunkt och privat länktjänst
    - Nya cmdletar
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork
    - Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig
        - Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.
        - Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.
* AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet
* Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler
    - Uppdaterade cmdletar
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection
* Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration
    - Uppdaterad cmdlet:
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe
    - Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till. Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Uppdaterade standardversionen för sparade sökningar till 1.
* Åtgärdade hantering av anpassad log null regex

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Uppdatera Get-AzRecoveryServicesBackupJob.md
* Uppdatera Get-AzRecoveryServicesBackupContainer.md
* Uppdatera Get-AzRecoveryServicesVault.md
* Uppdatera Wait-AzRecoveryServicesBackupJob.md
* Uppdatera Set-AzRecoveryServicesVaultContext.md
* Uppdatera Get-AzRecoveryServicesBackupItem.md
* Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md
* Uppdatera Restore-AzRecoveryServicesBackupItem.md
* Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs
* Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md

#### <a name="azresources"></a>Az.Resources
- Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment
- Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01

#### <a name="azservicebus"></a>Az.ServiceBus
* Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken
* verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats

#### <a name="azsql"></a>Az.Sql
* Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet
* Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser
* Korrigera ett skrivfel i ett varningsmeddelande.

#### <a name="azstorage"></a>Az.Storage
* Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används

#### <a name="azstoragesync"></a>Az.StorageSync
* Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.
* Åtgärda problem 9551 så att TierFilesOlderThanDays föredras

#### <a name="azwebsites"></a>Az.Websites
* Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp
* Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp
* Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots

## <a name="240---july-2019"></a>2.4.0 – juli 2019
#### <a name="azaccounts"></a>Az.Accounts
* Lägg till stöd för profil-cmdletar
* Lägg till stöd för miljöer och dataplaner i genererade cmdletar
* Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell

#### <a name="azadvisor"></a>Az.Advisor
* GA-version av Az.Advisor
* Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen

#### <a name="azapimanagement"></a>Az.ApiManagement
* Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671
    - **Get-AzApiManagementSubscription**
        - Stöd för att fråga prenumerationer efter användare och produkt har lagts till
        - Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till
* Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432
    - **Import-AzApiManagementApi**
        - Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till

#### <a name="azautomation"></a>Az.Automation
* Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.

#### <a name="azcompute"></a>Az.Compute
* Lägg till parametern HyperVGeneration i New-AzImageConfig

#### <a name="azdatafactory"></a>Az.DataFactory
* Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.

#### <a name="azeventgrid"></a>Az.EventGrid
* Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”

#### <a name="aziothub"></a>Az.IotHub
* Lägg till stöd för att återskapa principnycklar för auktorisering.

#### <a name="aznetwork"></a>Az.Network
* ”RoutingPreference” har lagts till i offentliga IP-taggar
* Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Åtgärda problem med null-referens i Get-AzPolicyState
    - Mer information här: https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Kommandot get-policy för IaaSVM:er har åtgärdats

#### <a name="azresources"></a>Az.Resources
    - Korrigera hjälptext för den översta parametern i Get-AzPolicyState
    - Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias
    - Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject
    - En mängd dokument- och exempeluppdateringar för Policy-cmdletar

#### <a name="azservicebus"></a>Az.ServiceBus
* Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes

#### <a name="azsql"></a>Az.Sql
* Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version
* Stöd för granskning för Azure SQL Server\Database med nya cmdletar.
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning

#### <a name="azstorage"></a>Az.Storage
* Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:
    -  Enable-AzStorageStaticWebsite
* Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel
* Visa mer felinformation när cmdleten misslyckas med StorageException
* Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen

## <a name="232---june-2019"></a>2.3.2 – juni 2019
#### <a name="azaccounts"></a>Az.Accounts
* Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop
    - Mer information här: https://github.com/Azure/azure-powershell/issues/8983
* Åtgärda problem med alias från AzureRM i Az-cmdletar
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.
* Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats

#### <a name="azdns"></a>Az.Dns
* Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.

#### <a name="azeventgrid"></a>Az.EventGrid
* Har uppdaterats för att använda API-versionen 2019-06-01.
* Nya cmdletar:
    - New-AzureRmEventGridDomain
        - Skapar en ny Azure Event Grid-domän.
    - Get-AzureRmEventGridDomain
        - Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.
    - Remove-AzureRmEventGridDomain
        - Tar bort en Azure Event Grid-domän.
    - New-AzureRmEventGridDomainKey
        - Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.
    - Get-AzureRmEventGridDomainKey
        - Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.
    - New-AzureRmEventGridDomainTopic:
        - Skapar ett nytt Azure Event Grid-domänämne.
    - Get-AzureRmEventGridDomainTopic
        - Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure
    - Remove-AzureRmEventGridDomainTopic:
        - Tar bort ett befintligt Azure Event Grid-domänämne.
* Uppdaterade cmdletar:
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:
        - Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.
        - Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.
        - Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).
        - Lade till ny valfria parametrar för att ange:
            - Förfallodatum för händelseprenumeration
            - Avancerade filterparametrar.
        - Lägg till ny uppräkning för servicebusqueue som mål.
        - Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:
        - Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.
    - Remove-AzureRmEventGridSubscription
        - Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.
        - Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)
* New-AzFrontDoorWafManagedRuleObject
    - Lägg till nya värden för automatisk komplettering

#### <a name="aznetwork"></a>Az.Network
* Lägg till stöd för resurs för virtuell nätverksgateway
    - Nya cmdletar
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* Lägg till AvailablePrivateEndpointType
    - Nya cmdletar
        - Get-AzAvailablePrivateEndpointType
* Lägg till PrivatePrivateLinkService
    - Nya cmdletar
        - Get-AzPrivateLinkService
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* Lägg till PrivateEndpoint
    - Nya cmdletar
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection
    - New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.
    - Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.
* Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.
* Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.
* Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit
* Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar
* En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.
* Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats
* Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats
* Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats
* Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till
* Cmdleten Get-AzNetworkServiceTag har lagts till
* Lägg till stöd för flera offentliga IP-adresser för Azure Firewall
    - Cmdleten New-AzFirewall har uppdaterats:
        - Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till
        - Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till
        - Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata
        - Inaktuella parametrar -PublicIpName och -VirtualNetworkName
* Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.
    - New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.
    - Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.
    - Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”

#### <a name="azresources"></a>Az.Resources
* Stöd för ytterligare alternativ för att exportera en mall
    - Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup
    - Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup
    - Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall

#### <a name="azsql"></a>Az.Sql
* Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection
* Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip
* Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas
    - New-AzStorageAccount
* Beskrivningen av cmdleten för bloboföränderlighet har förtydligats
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten
* Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot

## <a name="220---june-2019"></a>2.2.0 – juni 2019
#### <a name="azcdn"></a>Az.Cdn
* Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.

#### <a name="azcompute"></a>Az.Compute
* Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.
    - Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar
* Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName

#### <a name="aznetwork"></a>Az.Network
* Uppdatera ResourceId och InputObject för NAT-gateway
    - Lägg till alias för ResourceId och InputObject

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Åtgärda Null-referensproblem i Get-AzPolicyEvent

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1

#### <a name="azservicebus"></a>Az.ServiceBus
* Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability
* Åtgärda saknat tecken i Service Fabric-kommandorader

#### <a name="azsql"></a>Az.Sql
* Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.
* Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy
* Döp om cmdletar för hotidentifiering till Advanced Threat Protection
* Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.

#### <a name="azwebsites"></a>Az.Websites
* åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna

## <a name="210---may-2019"></a>2.1.0 – maj 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång
    - **Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång
    - **New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång
    - **New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte
    - **New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.
    - **New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik
    - **Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång
    - **Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång
* Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten
    - **Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen
    - **New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region
    - **Remove-AzApiManagementCache** – Ta bort ett cacheminne
    - **Remove-AzApiManagementCache** – Ta bort ett cacheminne
* Skapade nya cmdletar för hantering av API-schema
    - **New-AzApiManagementSchema** – Skapa ett nytt schema för ett API
    - **Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et
    - **Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et
    - **Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et
* Skapa ny cmdlet för att generera en användartoken.
    - **New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./
* Skapade en ny cmdlet för att hämta nätverksstatus
    - **Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av. Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.
* Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten
    - Lade till stöd för den nya SKU:n Consumption
    - Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption
    - Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel). Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.
    - Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.
* Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata
* Uppdaterad cmdleten för att visa infogade felmeddelanden
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]
* Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format
* Uppdaterade cmdlet **Import-AzApiManagementApi**
    - Importera API från dokumentspecifikationen OpenApi 3.0
    - Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).
    - Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.
* Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml
* Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml
* Uppdaterad cmdlet **New-AzApiManagementApi**
    - Konfigurera API med OpenId auktoriseringsservern.
    - Skapa ett API i ApiVersionSet
    - Klona ett API med SourceApiId och SourceApiRevision.
    - Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.
* Uppdaterad cmdlet **Set-AzApiManagementApi**
    - Konfigurera API med OpenId auktoriseringsservern.
    - Uppdatera ett API till ApiVersionSet
    - Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.
* Uppdaterad cmdlet **New-AzApiManagementRevision**
    - Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer). Den nya revisionen antar ApiId från den överordnade instansen.
    - Tillhandahålla ApiRevisionDescription
    - Åsidosätta ServiceUrl vid kloning av ett API.
* Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**
    - Konfigurera AAD eller AADB2C med en Authority
    - Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy
* Uppdaterad cmdlet **New-AzApiManagementSubscription**
    - Kompensera för ny SubscriptonModel med Scope och UserId
    - Kompensera för gammal prenumerationsmodell med ProductId och UserId
    - Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.
* Uppdaterad cmdlet **Set-AzApiManagementSubscription**
    - Kompensera för ny SubscriptonModel med Scope och UserId
    - Kompensera för gammal prenumerationsmodell med ProductId och UserId
    - Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.
* Uppdaterade följande cmdletar för att acceptera ResourceId som indata
    - New-AzApiManagementContext
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - Get-AzApiManagementApiRelease
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - Get-AzApiManagementApiVersionSet
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - Get-AzApiManagementAuthorizationServer
    - Get-AzApiManagementBackend
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - Get-AzApiManagementCertificate
    - Remove-AzApiManagementApiVersionSet
    - Remove-AzApiManagementSubscription

#### <a name="azautomation"></a>Az.Automation
* Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.
    - Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977
    - Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600
* Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.
    * Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347
* Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder. Nu returnerar den endast den matchande noden.

#### <a name="azcompute"></a>Az.Compute
* Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.
* Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk

#### <a name="azmonitor"></a>Az.Monitor
* Korrigera felaktiga parameternamn i hjälpexempel

#### <a name="aznetwork"></a>Az.Network
* Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell
    - Uppdaterad cmdlet:
        - Get-AzEffectiveRouteTable
* Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate

#### <a name="azresources"></a>Az.Resources
* Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden

#### <a name="azsql"></a>Az.Sql
* Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard

## <a name="200---may-2019"></a>2.0.0 – maj 2019
#### <a name="azaccounts"></a>Az.Accounts
* Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.
* Förbättra felmeddelande när det inte går att skapa konton.

#### <a name="azcompute"></a>Az.Compute
* Funktion för närhetsplaceringsgrupper.
    - Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.
* TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.
* Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss
* Icke-bakåtkompatibla ändringar
    - Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.
    - Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure

#### <a name="azdns"></a>Az.Dns
* Automatisk delegering av DNS för NameServer
    - Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.
    - Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor
* Byt namn på WAF-cmdletar så att de omfattar ”Waf”
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* Två cmdletar har tagits bort:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess
* Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:
    - Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.
    - Användare med HDInsight-operatörsrollen påverkas inte.

#### <a name="azmonitor"></a>Az.Monitor
* Nya cmdletar för SQR API (schemalagd frågeregel)
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - [Mer](/rest/api/monitor/scheduledqueryrules) information om SQR API
    - Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)

#### <a name="aznetwork"></a>Az.Network
* Lägg till stöd för NAT Gateway-resurs
    - Nya cmdletar
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Uppdaterade cmdletar
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.
    - New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.
    - Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Stöd för att fråga efter information om principutvärdering.
    - Lägg till parametern ”-Expand” för Get-AzPolicyState. Stöd för -Expand PolicyEvaluationDetails.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.
* Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.
* Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.
* Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.
* Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.
* Andra mindre korrigeringar.

#### <a name="azrelay"></a>Az.Relay
* Korrigera stavfel i kundriktade meddelanden

#### <a name="azservicebus"></a>Az.ServiceBus
* Nya cmdletar har lagts till för NetworkRuleSet för namnområden

#### <a name="azstorage"></a>Az.Storage
* Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)
* Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.
* Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”
    - New-AzStorageAccount
* Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp
* Get-AzWebApp*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella

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