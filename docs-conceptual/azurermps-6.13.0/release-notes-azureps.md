---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153948"
---
# <a name="release-notes"></a>Viktig information

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

---
## <a name="6130---november-2018"></a>6.13.0 – november 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Uppdatera beroenden för problemet med typmappning

#### <a name="azurermautomation"></a>AzureRM.Automation
* Swagger baserade Azure Automation-cmdletar
* Cmdletar för Uppdateringshantering har lagts till
* Cmdletar för källkontroll har lagts till
* Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till
* Kommandot för DSC-registreringsnod har åtgärdats

#### <a name="azurermcompute"></a>AzureRM.Compute
* Problem med SystemAssigned-identitet har åtgärdats
* Uppdatera beroenden för problemet med typmappning

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Uppdatera beroenden för problemet med typmappning

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* uppdatera exempelbeskrivningen för marketplace-cmdletar

#### <a name="azurermnetwork"></a>AzureRM.Network
* Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till
* ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till
* Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port. 
* Åtgärda problem med minnesanvändning i VirtualNetwork-karta

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices
* Åtgärda för att ändra principen för en skyddad fildelning.
* Tidszonsprincipen har konverterats till versaler.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices
* Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats
* Uppdatera beroenden för problemet med typmappning

#### <a name="azurermrelay"></a>AzureRM.Relay
* Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.

#### <a name="azurermresources"></a>AzureRM.Resources
* Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`
* Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata
* Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar

#### <a name="azurermsql"></a>AzureRM.Sql
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

## <a name="6120---november-2018"></a>6.12.0 – november 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime
* Byt namn på parametern TenantId i cmdleten Connect-AzureRmAccount till Tenant och lägg till ett alias för TenantId
* Uppdatera TenantId-beskrivning för Connect-AzureRmAccount
* Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän
    - https://github.com/Azure/azure-powershell/issues/6936
* Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen
    - https://github.com/Azure/azure-powershell/issues/7453
* Åtgärda problem med DataLake-slutpunkter vid användning av MSI
    - https://github.com/Azure/azure-powershell/issues/7462
* Åtgärda problem med att Disconnect-AzureRmAccount kastades om den inte anslöts
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* Bytte namn på cmdlet DLL-filnamnet till Microsoft.Azure.Commands.Automation.dll

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Lägg till åtgärden Get-AzureRmCognitiveServicesAccountSkus.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Lägg till cmdletarna Add-AzureRmVmssVMDataDisk och Remove-AzureRmVmssVMDataDisk
* Get-AzureRmVMImage visar AutomaticOSUpgradeProperties
* Åtgärdade att alternativvärden för SetAzureRmVMChefExtension -BootstrapOptions och -JsonAttribute inte ställdes in som json-format.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Uppdatera DataLake-paketet till 1.1.10.
* Lägg till standardsamtidighet för flertrådade åtgärder.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Åtgärdade problem #7267 (autoskalningsområde)
    - Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).
* Åtgärdade problem #7513 [Insights] Set-AzureRMDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas
    - Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning

#### <a name="azurermnetwork"></a>AzureRM.Network
* PeeringType ändrades till en obligatorisk parameter för följande cmdletar:
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Cmdletar för principreparation har lagts till

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices
* Stöd har lagts till för Azure-filresurser i återställningstjänster.

#### <a name="azurermresources"></a>AzureRM.Resources
* Korrigering för https://github.com/Azure/azure-powershell/issues/7402
    - Tillåt att resurser listas med parametern -ResourceId för Get-AzureRmResource

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Åtgärda att lägga till certifikat till Linux-Vmss.
* Åtgärda Add-AzureRmServiceFabricClusterCertificate
    - Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).
    - Visa undantag korrekt (Azure/service-fabric-issues#1054).
* Åtgärda Update-AzureRmServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.

## <a name="6110---october-2018"></a>6.11.0 – oktober 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Åtgärda problemet med Get-AzureRmSubscription i CloudShell
* Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime

#### <a name="azurermbackup"></a>AzureRM.Backup
* Inaktuella Azure Backup-cmdletar.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Nya storlekar har lagts till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för ”New-AzureRmVm”
* Argumentslutförare för ResourceName har lagts till i alla cmdletar.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Lägger till stöd för virtuella nätverksregler
    - Get-AzureRmDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt Azure Data Lake Store-nätverk.
    - Add-AzureRmDataLakeStoreVirtualNetworkRule: Lägger till en regel för det virtuella nätverket till det angivna Data Lake Store-kontot.
    - Set-AzureRmDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för det virtuella nätverket i det angivna Data Lake Store-kontot.
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzureRmNetworkWatcherConnectivity.
* Argumentslutförare för ResourceName har lagts till i alla cmdletar.

#### <a name="azurermresources"></a>AzureRM.Resources
* Åtgärda problem där Get-AzureRMRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot. Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.

## <a name="6100---october-2018"></a>6.10.0 – Oktober 2018
#### <a name="azurestorage"></a>Azure.Storage
* Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Stöd för Get-AzureRmCognitiveServicesAccountSkus utan ett befintligt konto.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Åtgärda fel där Get-AzureRmVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs
* Ett exempel för ”SimpleParameterSet” har lagts till i hjälpen för cmdleten New-AzureRmVmss.
* Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK-versionen har uppdaterats till 2.3.0.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Funktionalitet för NetworkProfile har lagts till. nya cmdletar har lagts till
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* Länk för tjänstassociering på modell för undernät har lagts till
* De nya cmdletarna New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap och Remove-AzureRmVirtualNetworkTap har lagts till
* Cmdletarna Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig och Remove-AzureRmNEtworkInterfaceTapConfig har lagts till

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Tillåt att alla strängar används som storleksparametrar framöver. Lägg till P5 i popup-fönstret PSArgumentCompleter

#### <a name="azurermresources"></a>AzureRM.Resources
* Parametern -Mode som saknades i Set-AzureRmPolicyDefinition har lagts till
* Åtgärda buggen för cmdleten Get-AzureRmProviderOperation för åtgärder med ursprung som innehåller användare

#### <a name="azurermsql"></a>AzureRM.Sql
* Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats

#### <a name="azurermstorage"></a>AzureRM.Storage
* Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Ny cmdlet: Get-AzureRMWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container
* Nya cmdletar: New-AzureRMWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows

## <a name="690---september-2018"></a>6.9.0 – September 2018
#### <a name="general"></a>Allmänt
* AzureRM.SignalR har lagts till i samlingsmodulen för AzureRM

#### <a name="azurermprofile"></a>AzureRM.Profile
* Mindre ändringar i den gemensamma koden för lagring
* Hjälpfiler har uppdaterats för att innehålla fullständiga parametertyper.
* -ServicePrincipal har ändrats så att den inte längre är obligatorisk i parameteruppsättningen ServicePrincipalCertificateWithSubscriptionId 

#### <a name="azurestorage"></a>Azure.Storage
* Stöd för att skapa lagringskontext med OAuth. 
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Standard_Microsoft har lagts till i SKU:n för CDN-prissättning. 

#### <a name="azurermcompute"></a>AzureRM.Compute
* Flytta beroenden i nyckelvalv och minne till de gemensamma beroendena
* Lägg till stöd för flera storlekar av virtuella datorer i AEM-cmdletar
* Lägg till parametern PublicIPPrefix i New-AzureRmVmssIpConfig
* Lägg till parametern ResourceId till cmdleten Invoke-AzureRmVMRunCommand
* Lägg till cmdleten Invoke-AzureRmVmssVMRunCommand

#### <a name="azurermdns"></a>AzureRM.Dns
* Stöd har lagts till för aliasposter när DNS-poster skapas

#### <a name="azurerminsights"></a>AzureRM.Insights
* Problem #6833 och #7102 (området Diagnostikinställningar) har åtgärdats
    - Problem med standardnamnet, d.v.s. ”tjänsten” när diagnostikinställningar skapas och listas/hämtas
    - Problem med att skapa diagnostikinställningar med kategorier
* Utfasningsmeddelande har lagts till för tidsintervallsparametrar för mått
    - Tidsintervallsparametrar går fortfarande att använda (det här är en bakåtkompatibel ändring), men de ignoreras i serverdelen eftersom endast PT1M är giltigt

#### <a name="azurermnetwork"></a>AzureRM.Network
* Ändringar i LoadBalancer-cmdletar
  - LoadBalancerInboundNatPoolConfig: parametrarna IdleTimeoutInMinutes, EnableFloatingIp och EnableTcpReset har lagts till
  - LoadBalancerInboundNatRuleConfig: parametern EnableTcpReset har lagts till
  - LoadBalancerRuleConfig: parametern EnableTcpReset har lagts till
  - LoadBalancerProbeConfig: stöd för värdet ”Https” för parameterprotokoll har lagts till
* Nya kommandon för den nya underresursen för LoadBalancers OutboundRule har lagts till
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* Ny HostedWorkloads-egenskap har lagts till för PSNetworkInterface
* Nya cmdletar har lagts till för funktionen: Azure Firewall via ARM
  - Get-AzureRmFirewall har lagts till
  - Set-AzureRmFirewall har lagts till
  - New-AzureRmFirewall har lagts till
  - Remove-AzureRmFirewall har lagts till
  - New-AzureRmFirewallApplicationRuleCollection har lagts till
  - New-AzureRmFirewallApplicationRule har lagts till
  - New-AzureRmFirewallNatRuleCollection har lagts till
  - New-AzureRmFirewallNatRule har lagts till
  - New-AzureRmFirewallNetworkRuleCollection har lagts till
  - New-AzureRmFirewallNetworkRule har lagts till
* Stöd för betrott rotcertifikat och konfiguration för autoskalning har lagts till i Application Gateway
  - Nya cmdletar har lagts till:
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - Cmdletar har uppdaterats med valfri parameter – TrustedRootCertificate
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - Cmdletar har uppdaterats med valfri parameter – AutoscaleConfiguration
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* Lägg till cmdlet för gränssnittsslutpunkten Get-AzureInterfaceEndpoint
* Stöd för flera adressprefix i ett undernät har lagts till. Uppdaterade cmdletar:
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig – Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* Lägger till cmdletar för delegering av undernät.
  - New-AzureRmDelegation: Skapar en ny delegering som kan läggas till i ett undernät
  - Remove-AzureRmDelegation: Hämtar ett undernät och tar bort det angivna delegeringsnamnet från undernätet
  - Add-AzureRmDelegation: Hämtar ett undernät och lägger till det angivna tjänstnamnet som en delegering till undernätet
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices
* Stöd för hanterad disk

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Insights-beroende har uppdaterats.

#### <a name="azurermresources"></a>AzureRM.Resources
* Uppdatera New-AzureRmResourceGroupDeployment med den nya parametern RollbackAction
    - Lägg till stöd för OnErrorDeployment med den nya parametern.
* Stöd för hanterad identitet på principtilldelningar.
* Parametrar med standardvärden krävs inte längre när du tilldelar en princip med ”New-AzureRmPolicyAssignment”
* Lägg till den nya cmdleten Get-AzureRmPolicyAlias för att hämta principalias

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Problem #7161 har åtgärdats

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* Uppdatera SKU-namn till Free_F1 och Standard_S1
* Lägg till versionsfältet i PSSignalRResource-objektet och en anslutningssträng i PSSignalRKeys-objektet.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Stöd för oföränderlighetsprincip i AzureRm.Storage 
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Två nya cmdletar har lagts till: Get-AzureRmDeletedWebApp och Restore-AzureRmDeletedWebApp
* New-AzureRmAppServicePlan – En HyperV-växel har lagts till för skapa en app service-plan med Windows-containrar
* New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot – Nya parametrar (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) har lagts till för att skapa och hantera Windows-containerappar

## <a name="681---august-2018"></a>6.8.1 – augusti 2018
#### <a name="general"></a>Allmänt
* Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.
* Uppdaterade Common Runtime-sammansättningar

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.
* Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6603
    - Import-AzureRmApiManagementApi- och *-AzureRmApiManagementCertificate-cmdletar kan nu hantera relativa sökvägar
* Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6879
    - CertificateInformation är en inställbar egenskap som gör att Set-AzureRmApiManagement-cmdleten fungerar ordentligt. Åtgärdat genom uppgradering till NuGet för 4.0.4-preview
* Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6853
    - Odata-filtret för sökning efter namn på produkt har åtgärdats
* Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6814
    - Odata-filtret för sökning efter namn på API har åtgärdats
* Stöd har lagts till för AzureMonitor-loggare


#### <a name="azurermcompute"></a>AzureRM.Compute
* Ett problem med att mål saknas i felutdata har åtgärdats.
* Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats
* Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.
* Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina

#### <a name="azurermnetwork"></a>AzureRM.Network
* Standardvisning av cmdlet-utdata har ändrats för att visas i tabellvy

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet


#### <a name="azurermresources"></a>AzureRM.Resources
* Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Åtgärdade problem
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Stöd har lagts till för trafikroutningsmetoden MultiValue
    - Ny parameter, ”MaxReturn”, för MultiValue-routning
* Stöd har lagts till för trafikroutningsmetod för undernät
    - Stöd för IP-adressintervall (undernät) i slutpunkter
* Stöd har lagts till för anpassade rubriker i profiler
* Stöd har lagts till för förväntade statuskodintervall i profiler
* Stöd har lagts till för anpassade rubriker i slutpunkter

## <a name="680---august-2018"></a>6.8.0 – augusti 2018
#### <a name="general"></a>Allmänt
* Problem med standardresursgrupp som inte har konfigurerats har åtgärdats.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Utgångsegenskap har lagts till i token som returneras under Connect-AzureRmAccount

#### <a name="azurermcompute"></a>AzureRM.Compute
* Ett problem med att mål saknas i felutdata har åtgärdats.
* Problem med lagringskontotyper för virtuell dator med en hanterad disk har åtgärdats
* Åtgärda cmdletar för AEM-tillägg för andra miljöer, till exempel Azure Kina

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Korrigera exempel för New-AzureRmIotHubExportDevices och New-AzureRmIotHubImportDevices

#### <a name="azurermnetwork"></a>AzureRM.Network
* Standardmodeller har ändrats för att visas i tabellvy

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Åtgärda fel i Update-AzureRmPowerBIEmbeddedCapacity vid försök att skala pausad kapacitet

#### <a name="azurermresources"></a>AzureRM.Resources
* Ett problem med att skapa hanterade program från MarketPlace har åtgärdats.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Korrigeringar för problem
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Stöd för trafikroutningsmetoden MultiValue
    - Ny parameter, ”MaxReturn”, för MultiValue-routning
* Stöd för trafikroutningsmetod för undernät
    - Stöd för IP-adressintervall (undernät) i slutpunkter
* Stöd för anpassade rubriker i profiler
* Stöd för förväntade statuskodintervall i profiler
* Stöd för anpassade rubriker i slutpunkter

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Problem med standardresursgrupp som inte har konfigurerats korrekt har åtgärdats.

## <a name="670---august-2018"></a>6.7.0 – augusti 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.
* Lägg till användar-id i standardkontextnamnet för att undvika kontextkonflikter
    - https://github.com/Azure/azure-powershell/issues/6489
* Åtgärda problem med Clear-AzureRmContext som orsakade problem med att välja en kontext #6398
* Aktivera den klientorganisationsdomän som ska skickas till parametern -TenantId för Connect-AzureRmAccount
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage
* Ta bort begränsningen på 5 TB för Azure-filresurskvoten
* Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermbatch"></a>AzureRM.Batch
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermbilling"></a>AzureRM.Billing
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.
* Lägg till parametern EvictionPolicy i New-AzureRmVmssConfig
* Använd standardplatsen i DiskFileParameterSet för New-AzureRmVm om ingen plats har angetts.
* Korrigera parameterbeskrivningen i Save-AzureRmVMImage
* Korrigera cmdleten Get-AzureRmVMDiskEncryptionStatus för vissa singlepass-relaterade scenarier

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Korrigera felsökning när DebugPreference anges från powershell-kommandoraden
* Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAcl
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.
* Uppdatera exemplet för Set-AzureRmDataLakeStoreItemAclEntry

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermdns"></a>AzureRM.Dns
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermmedia"></a>AzureRM.Media
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Exempel för Set-AzureRmLocalNetworkGateway har lagts till
* Exempel och beskrivningar för Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey och New-AzureRmVirtualNetworkGatewayConnection har lagts till
* Exempel för Remove-AzureRmVirtualNetworkGatewayIpConfig och Reset-AzureRmVirtualNetworkGateway
* Exempel för Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till
* Exempel för Set-AzureRmVirtualNetworkGatewayConnectionSharedKey har lagts till
* Exempel för Set-AzureRmVirtualNetworkGatewayConnection har lagts till
* Cmdletar för ApplicationSecurityGroup, RouteTable and Usage har genererats om med den senaste kodgeneratorn
* Förtydligade ett felmeddelande för Get-AzureRmVirtualNetworkSubnetConfig vid försök att hämta ett undernät som inte avslutas

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices
* Lade till principfilter i cmdleten Get-AzureRmRecoveryServicesBackItem. Kommandot returnerar listan med säkerhetskopieringsobjekt som skyddas av det angivna princip-ID:t.
* Microsoft.Azure.Management.RecoveryServices.Backup uppdaterades till förhandsversionen av 3.0.0.
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.
* Parametern TargetResourceGroupName lades till i Restore-AzureRmRecoveryServicesBackupItem. Den resursgrupp som de hanterade diskarna återställs till. Gäller för säkerhetskopiering av virtuell dator med hanterade diskar.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermresources"></a>AzureRM.Resources
* Distribution av supportmall i prenumerationsomfånget. Lägg till nya cmdletar:
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Korrigera ett problem där fel inträffar när en kontext skickas till Set-AzureRmResource
    - https://github.com/Azure/azure-powershell/issues/5705
* Korrigera exempel i New-AzureRmResourceGroupDeployment
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermsql"></a>AzureRM.Sql
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermtags"></a>AzureRM.Tags
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Har uppdaterats till den senaste versionen av Azure ClientRuntime.

## <a name="660---july-2018"></a>6.6.0 – juli 2018
#### <a name="general"></a>Allmänt
* Alla hjälpfiler har uppdaterats för att ta med fullständiga parametertyper och korrekta indata-/utdatatyper.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Common.Strategy-biblioteket har uppdaterats för att kunna verifiera att den aktuella konfigurationsfilen för en resurs är kompatibel med målresursen.
* ps1xml-typer har lagts till i Common.Storage

#### <a name="azurestorage"></a>Azure.Storage
* Lade till stöd för hämtning av lagringskontext från DefaultProfile
* Lade till Ps1XmlAttribute till utdatatypegenskaper för cmdletar.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6370
    - En bugg har åtgärdats i Automapper för att översätta PsApiManagementApi till ApiContract
* Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6515
    - En bugg har åtgärdats i File.Save för att inte överbelasta kodningstypen
* Åtgärdat problem https://github.com/Azure/azure-powershell/issues/6560
    - Har uppgraderats till Nuget-versionen 4.0.3 vilket åtgärdar mönsterundantaget på apiId

#### <a name="azurermcompute"></a>AzureRM.Compute
* Åtgärda problem med fel vid skapandet av en virtuell dator med hjälp av DiskFileParameterSet i New-AzureRmVm på grund av namnbyte på PremiumLRS-lagringskontotypen.
* Åtgärda cmdleten Invoke-AzureRmVMRunCommand
* Uppdatera Get-AzureRmAvailabilitySet för att aktivera funktionen för att lista alla tillgänglighetsuppsättningar i en prenumeration.  (Parametern ResouceGroupName är nu frivillig.)
* Uppdatera SimpleParameterSet för "New-AzureRmVm" för att aktivera accelererat nätverk på berättigade virtuella datorer.
* Uppdatera den enkla parameteruppsättningen för New-AzureRmVmss så att det inte går att skapa de virtuella datorerna när en användarangiven lastbalanserare redan finns.
* Uppdatera exempel för New-AzureRmDisk
* Lägg till exempel för "New-AzureRmVM"
* Uppdatera beskrivning för Set-AzureRmVMOSDisk
* Uppdatera Exempel 1 för Set-AzureRmVMBginfoExtension för stavningskontroll och prefix. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK-versionen har uppdaterats till 1.1.0.
* Stöd för delning av Integration Runtime (lokal installation) mellan datafabriker.
     - Lägg till ny parameter – SharedIntegrationRuntimeResourceId i cmdleten Set-AzureRmDataFactoryV2IntegrationRuntime.
     - Lägg till ny valfri parameter – LinkedDataFactoryName i cmdleten Remove-AzureRmDataFactoryV2IntegrationRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* DataPlane SDK-versionen (Microsoft.Azure.DataLake.Store) har uppdaterats till 1.1.9

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats

#### <a name="azurerminsights"></a>AzureRM.Insights
* Formatering har åtgärdats för OutputType i hjälpfiler
* Använda Microsoft.Azure.Management.Monitor SDK 0.19.1-preview

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Åtgärda problem med piping i Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermnetwork"></a>AzureRM.Network
* Exempel har lagts till för LoadBalancerInboundNatPoolConfig-cmdletar.

#### <a name="azurermresources"></a>AzureRM.Resources
* Åtgärda problem när både taggnamn och värde anges för "Get-AzureRmResource"
    - https://github.com/Azure/azure-powershell/issues/6765
* Åtgärda pipingscenario med "Set-AzureRmResource"

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Piping för InputObject and ResourceId i borttagna cmdletar har uppdaterats
* några problem har åtgärdats
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Lägg till stöd för Server Advanced Threat Protection med följande cmdletar:
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* Lägg till stöd för Sårbarhetsbedömning med följande cmdletar:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Exempel i Remove-AzureRmSqlServerFirewallRule har åtgärdats
* Åtgärda felaktig hantering av datum och tid för andra kulturer än usa-baserade kulturer i Get-AzureSqlSyncGroupLog

#### <a name="azurermstorage"></a>AzureRM.Storage
* Lägg till Ps1XmlAttribute i utdatatypegenskaper för cmdletar
* Visa utdata för cmdleten StorageAccount i tabellvyn
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* Ta bort felaktig instruktion från hjälpen för cmdleten Tag
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 – juli 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Hjälp för ”Get-AzureRmContextAutosaveSetting” har uppdaterats

#### <a name="azurestorage"></a>Azure.Storage
* Stöd för uppladdning av blob eller fil med lässkyddad SAS-token
* Set-AzureStorageBlobContent
* Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Lägg till den nödvändiga egenskapen ResourceGroupName i AS.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Uppdatera hjälp och lägg till exempel för ”New-AzureRMAutomationSchedule”

#### <a name="azurermcompute"></a>AzureRM.Compute
* Lägg till parametern -Tag förUpdate/New-AzureRmAvailabilitySet
* Lägg till exempel för ”Add-AzureRmVmssExtension”
* Lägg till exempel för ”Remove-AzureRmVmssExtension”
* Uppdatera hjälp för ”Set-AzureRmVMAccessExtension”
* Uppdatera SimpleParameterSet för New-AzureRmVmss för att ställa in SinglePlacementGroup på falskt som standard och lägg till växlingsparametern ”SinglePlacementGroup” som gör att användare kan skapa VMSS i en enda placeringsgrupp.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* En skrivskyddad egenskap, ”PendingReplicationOperationsCount”, har lagts till för klassen PSEventHubDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Uppdatera felmeddelande för Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Felet ”parameteruppsättningen gick inte att matcha” har korrigerats i New-AzureRmLogicApp

#### <a name="azurermnetwork"></a>AzureRM.Network
* Aktivera peering mellan virtuella nätverk i flera klienter för Set/Add-AzureRmVirtualNetworkPeering
* Nedanstående cmdletar för Application Gateway har uppdaterats
    - New-AzureRmApplicationGateway: EnableFIPS-flagga har lagts till för stöd för zoner
    - New-AzureRmApplicationGatewaySku: nya SKU:er, Standard_v2 och WAF_v2, har lagts till
    - Set-AzureRmApplicationGatewaySku : nya SKU:er, Standard_v2 och WAF_v2, har lagts till
* RouteTable-cmdletar har återskapats med den senaste versionen av generatorn

#### <a name="azurermrelay"></a>AzureRM.Relay
* Markdown-filer har uppdaterats och korrigerar problem med parameternamn i exemplet

#### <a name="azurermresources"></a>AzureRM.Resources
* Uppdatera cmdletar för rolltilldelning och rolldefinition:
    - Ta bort extra anrop för rolldefinitioner som görs som en del av sidindelning.
* Åtgärda Get-AzureRMRoleAssignment-cmdlet
    - Åtgärda parameterfunktioner för kommandot -ExpandPrincipalGroups
* Åtgärda problem med ”Get-AzureRmResource” där ”-ResourceType”-parametern var skiftlägeskänsligt

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Parametrar för att stoppa och hoppa över har lagts till i listan över cmdletar
* Cmdletar för migrering från Standard- till Premium-namnområden har lagts till:
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* En skrivskyddad egenskap, ”PendingReplicationOperationsCount” har lagts till för klassen PSServiceBusDRConfigurationAttributes som anger antalet väntande replikeringsåtgärder medan replikeringen pågår

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Uppdatera exempel för ”New-AzureRmServiceFabricCluster”

#### <a name="azurermsql"></a>AzureRM.Sql
* Nya cmdletar för Management.Sql som gör att kunderna kan lägga till certifikat för transparent datakryptering till SQL Server-instans eller en hanterad instans har lagts till
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* När `Set-AzureRmWebApp -AssignIdentity` och `Set-AzureRmWebAppSlot -AssignIdentity` är inställda på falskt tar de nu bort identitetsegenskapen från platsobjektet. Även förhandsgranskningstaggen tas bort.
* `Get-AzureRmWebAppMetrics`, `Get-AzureRmAppServicePlanMetrics`-exempel har uppdaterats
* `Set-AzureRmWebApp -PhpVersion` har stöd för ”av” som en giltig php-version

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
* Nya kommandon har lagts till för funktionen: ExpressRoute Partner API:er via ARM
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
