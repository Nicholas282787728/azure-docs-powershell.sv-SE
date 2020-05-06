---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.openlocfilehash: 1491f3f23deb767b754a98b3fab616356daa71f3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "67863768"
---
# <a name="release-notes"></a>Viktig information

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

## <a name="20170925---version-440"></a>2017.09.25 – Version 4.4.0
* AnalysisServices
  * Ett nytt dataplans-cmdlet har lagts till för att tillåta synkronisering av databaser från instans utan skrivskydd till skrivskyddad instanser
    - Hjälpfil för cmdleten har inkluderats
    - Minnesinterna tester och scenariotester har lagts till (endast live)
  * Åtgärdat buggar i cmdlet Add-AzureAsAccount
* Automation
  * Åtgärdat hjälpdokument för cmdletar som åtgärdats i den tidigare versionen.
  * Lagt till 4 nya cmdlet som stöd för stegvis distribution av DSC-nodkonfigurationer.
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * Integrera med Cognitive Services Management SDK, version 2.0.0.
  * Nu har Get-AzureRmCognitiveServicesAccount stöd för korrekt sidindelning.
* Compute
  * Funktionen körningskommando:
    - Ny cmdlet: Invoke-AzureRmVMRunCommand anropar ett körningskommando på en virtuell dator
    - Ny cmdlet: Get-AzureRmVMRunCommandDocument visar tillgängliga dokument för körningskommando
  * Lägg till parametern StorageAccountType för att ange Set-AzureRmDataDisk
  * Tillgänglighetszonen har stöd för virtuell dator, VM-skalningsuppsättning och disk
    - Ny parameter: Zone har lagts till i New-AzureRmVM, New-AzureRmVMConfig, New-AzureRmVmssConfig, New-AzureRmDiskConfig
  * Rullande uppgraderingsfunktion för VM-skalningsuppsättning:
    - Ny cmdlet: Start-AzureRmVmssRollingOSUpgrade anropar löpande OS-uppgradering av VM-skalningsuppsättning
    - Ny cmdlet: Set-AzureRmVmssRollingUpgradePolicy anger uppgraderingsprincip för löpande uppgradering av VM-skalningsuppsättning.
    - Ny cmdlet: Stop-AzureRmVmssRollingOSUpgrade avbryter löpande OS-uppgradering av VM-skalningsuppsättning
    - Ny cmdlet: Get-AzureRmVmssRollingUpgradePolicy visar status för uppgraderingsprincip för löpande uppgradering av VM-skalningsuppsättning.
  * Switchparametern AssignIdentity införs för systemtilldelad identitet.
    - Ny parameter: AssignIdentity har lagts till i New-AzureRmVMConfig, New-AzureRmVmssConfig och Update-AzureRmVM
  * Funktionen för kryptering av Vmss-disk:
    - Ny cmdlet: Set-AzureRmVmssDiskEncryptionExtension aktiverar diskkryptering på VM-skalningsuppsättningen
    - Ny cmdlet: Disable-AzureRmVmssDiskEncryption inaktiverar diskkryptering på VM-skalningsuppsättningen
    - Ny cmdlet: Get-AzureRmVmssDiskEncryptionStatus visar status för diskkryptering på VM-skalningsuppsättningen
    - Ny cmdlet: Get-AzureRmVmssVMDiskEncryptionStatus visar status för diskkryptering på virtuella datorer i en VM-skalningsuppsättning
* ContainerInstance
  * Lägg till PowerShell-cmdletar för Azure Container Instance
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* Insikter
  * Ny cmdlet: Disable-AzureRmActivityLogAlert
    - En ny cmdlet för att inaktivera en befintlig aktivitetsloggavisering.
    - Du kan även ange taggarna med denna cmdlet.
  * Ny cmdlet: Enable-AzureRmActivityLogAlert
    - En ny cmdlet för att aktivera en befintlig aktivitetsloggavisering.
    - Du kan även ange taggarna med denna cmdlet.
  * Ny cmdlet: Get-AzureRmActivityLogAlert
    - En ny cmdlet för att hämta en eller flera aktivitetsloggaviseringar.
    - Aviseringarna kan hämtas efter namn, resursgrupp eller prenumeration.
  * Ny cmdlet: New-AzureRmActionGroup
    - En ny cmdlet för att skapa ett ActionGroup-objekt i minnet (utan någon begäran).
  * Ny cmdlet: New-AzureRmActivityLogAlertCondition
    - En ny cmdlet för att ett lövvillkorsobjekt för aktivitetsloggavisering i minnet (utan någon begäran).
  * Ny cmdlet: Set-AzureRmActivityLogAlert
    - En ny cmdlet för att skapa eller uppdatera en aktivitetsloggavisering.
  * Ny cmdlet: Remove-AzureRmActivityLogAlert
    - En ny cmdlet för att ta bort en aktivitetsloggavisering.
  * Ny cmdlet: Set-AzureRmActionGroup
    - En ny cmdlet för att skapa en ny eller uppdatera en befintlig åtgärdsgrupp.
  * Ny cmdlet: Get-AzureRmActionGroup
    - En ny cmdlet för att hämta en eller flera åtgärdsgrupper.
    - Åtgärdsgrupperna kan hämtas efter namn, resursgrupp eller prenumeration.
  * Ny cmdlet: Remove-AzureRmActionGroup
    - En ny cmdlet för att ta bort en åtgärdsgrupp.
  * Ny cmdlet: New-AzureRmActionGroupReceiver
    - En ny cmdlet för att skapa en ny åtgärdsgruppmottagare i minnet.
* KeyVault
  * Nya/uppdatera Cmdletar med stöd för mjuk borttagning för KeyVault-certifikat
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* Nätverk
  * Stöd för slutpunktstjänster har lagts till i Virtual Network-undernät
    - Uppdaterat Add-AzureRmVirtualSubnetConfig: Valfria parametern -ServiceEndpoint lades till
    - Uppdaterat New-AzureRmVirtualSubnetConfig: Valfria parametern -ServiceEndpoint lades till
    - Uppdaterat Set-AzureRmVirtualSubnetConfig: Valfria parametern -ServiceEndpoint lades till
  * Cmdlet har lagts till för att lista slutpunktstjänster som är tillgängliga på platsen
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * Möjligheten att konfigurera extern, radius-baserad P2S-autentisering till följande cmdletar har lagts till
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * Cmdlet har lagts till för att tillåta generering av VpnProfiles för extern radius-baserad P2S
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * Stöd för SKU-parametern har lagts till i offentliga IP-adresser och lastbalanserare
    - Uppdaterat New-AzureRMLoadBalancer: Valfria parametern -Sku har lagts till
    - Uppdaterat New-AzureRMPublicIpAddress: Valfria parametern -Sku har lagts till
  * Stöd för DisableOutboundSNAT har lagts till i Load Balancer-regler
    - Uppdaterat New-AzureRMLoadBalancerRuleConfig: Valfria parametern DisableOutboundSNAT har lagts till
    - Uppdaterat Add-AzureRMLoadBalancerRuleConfig: Valfria parametern DisableOutboundSNAT har lagts till
    - Uppdaterat Set-AzureRMLoadBalancerRuleConfig: Valfria parametern DisableOutboundSNAT har lagts till
  * Stöd har lagts till för IkeV2 P2S
    - Uppdaterat New-AzureRmVirtualNetworkGateway: Valfria parametern -VpnClientProtocol har lagts till, standard som [ "SSTP", "IkeV2" ]
    - Uppdaterat Set-AzureRmVirtualNetworkGateway: Valfria parametern -VpnClientProtocol har lagts till
  * Stöd för flervärdesregler har lagts till i Network Security Rules och i Effective Network Security Rules
    - Uppdaterat Add-AzureRmNetworkSecurityRuleConfig: Uppdaterat parametrarna SourcePortRange DestinationPortRange, SourceAddressPrefix för att acceptera en lista med strängar
    - Uppdaterat New-AzureRmNetworkSecurityRuleConfig: Uppdaterat parametrarna SourcePortRange DestinationPortRange, SourceAddressPrefix för att acceptera en lista med strängar
    - Uppdaterat Set-AzureRmNetworkSecurityRuleConfig: Uppdaterat parametrarna SourcePortRange DestinationPortRange, SourceAddressPrefix för att acceptera en lista med strängar
    - Uppdaterat Add-AzureRmNetworkSecurityRuleConfig: Uppdaterat parametrarna SourcePortRange DestinationPortRange, SourceAddressPrefix för att acceptera en lista med strängar
    - Uppdaterat New-AzureRmNetworkSecurityGroup: Uppdaterat parametern SecurityRules för acceptera parametrarna SourcePortRange, DestinationPortRange, SourceAddressPrefix som är lista med strängar i objektet PSSecurityRule
    - Uppdaterat Get-AzureRmEffectiveNetworkSecurityGroup: Parametern TagMap har lagts till
    - Uppdaterat Get-AzureRmEffectiveNetworkSecurityGroup: Uppdaterat det returnerade PSEffectiveSecurityRule-objektet med parametrarna SourcePortRange, DestinationPortRange, SourceAddressPrefix som är lista med strängar.
  * Stöd för DDOS-skydd för virtuella nätverk har lagts till
    - Uppdaterat New-AzureRmVirtualNetwork: Switchparametrarna EnableDDoSProtection och EnableVmProtection har lagts till
    - Egenskaperna EnableDDoSProtection och EnableVmProtection har lagts till i PSVirtualNetwork-objektet
  * Stöd för intern lastbalanserare med hög tillgänglighet har lagts till
    - Uppdaterat Add-AzureRmLoadBalancerRuleConfig: Lade till Alla som ett giltigt värde för parametern Protocol
    - Uppdaterat New-AzureRmLoadBalancerRuleConfig: Lade till Alla som ett giltigt värde för parametern Protocol
    - Uppdaterat Set-AzureRmLoadBalancerRuleConfig: Lade till Alla som ett giltigt värde för parametern Protocol
  * Stöd för programsäkerhetsgrupper har lagts till
    - New-AzureRmApplicationSecurityGroup har lagts till
    - Get-AzureRmApplicationSecurityGroup har lagts till
    - Remove-AzureRmApplicationSecurityGroup har lagts till
    - Uppdaterat New-AzureRmNetworkInterface: Valfria parametrarna ApplicationSecurityGroup och ApplicationSecurityGroupId har lagts till
    - Uppdaterat New-AzureRmNetworkInterfaceIpConfig: Valfria parametrarna ApplicationSecurityGroup och ApplicationSecurityGroupId har lagts till
    - Uppdaterat Add-AzureRmNetworkInterfaceIpConfig: Valfria parametrarna ApplicationSecurityGroup och ApplicationSecurityGroupId har lagts till
    - Uppdaterat Set-AzureRmNetworkInterfaceIpConfig: Valfria parametrarna ApplicationSecurityGroup och ApplicationSecurityGroupId har lagts till
    - Uppdaterat New-AzureRmNetworkSecurityRuleConfig: Valfria parametrarna SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup och DestinationApplicationSecurityGroupId har lagts till
    - Uppdaterat Add-AzureRmNetworkSecurityRuleConfig: Valfria parametrarna SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup och DestinationApplicationSecurityGroupId har lagts till
    - Uppdaterat New-AzureRmNetworkSecurityRuleConfig: Valfria parametrarna SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup och DestinationApplicationSecurityGroupId har lagts till
  * Nya kommandon har lagts till för skriptet VpnDeviceConfiguration
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* Profil
  * Stöd för Start-Job för AzureRm-cmdletar.
    * Alla AzureRmCmdletar lägger till parametern -AzureRmContext, som kan acceptera en kontext (utdata från en kontext-cmdlet).
      - Vanligt mönster för jobb med kontextpersistence INAKTIVERAT:`Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - Vanligt mönster för jobb med kontextpersistence AKTIVERAT:`Start-Job {New-AzureRmVM [... other parameters]}`
  * Bevara inloggningsinformation mellan sessioner, nya cmdletar:
    - Enable-AzureRmContextAutosave – Aktivera bevarade autentiseringsuppgifter mellan sessioner.
    - Disable-AzureRmContextAutosave – Inaktivera bevarade autentiseringsuppgifter mellan sessioner.
  * Hantera kontextinformation, nya cmldetar
    - Select-AzureRmContext – Välj den aktiva namngivna kontexten.
    - Rename-AzureRmContext – Byt namn på en befintlig kontext för enklare referens.
    - Remove-AzureRmContext – Ta bort en befintlig kontext.
    - Remove-AzureRmAccount – Ta bort alla autentiseringsuppgifter, prenumerationer och klientorganisationer som är kopplade till ett konto.
  * Hantera kontextinformation, ändrade cmdletar:
    - Scope = (Process | CurrentUser) har lagts till i alla cmdletar som ändrar autentiseringsuppgifter
    - Get-AzureRmContext – Parametern ListAvailable har lagts till för att lista alla sparade kontexter
* Resurser
  * Cmdletar för PolicySetDefinition har lagts till
    - Cmdlet New-AzureRmPolicySetDefinition för att skapa en principuppsättningsdefinition
    - Cmdlet Get-AzureRmPolicySetDefinition för att lista alla principuppsättningsdefinitioner eller för att hämta en viss principuppsättningsdefinition
    - Cmdlet Remove-AzureRmPolicySetDefinition för att ta bort en principuppsättningsdefinition
    - Cmdlet Set-AzureRmPolicySetDefinition för att uppdatera en befintlig principuppsättningsdefinition
  * Lagt till parametrarna -PolicySetDefinition, -Sku och -NotScope i cmdletarna New-AzureRmPolicyAssignment och Set-AzureRmPolicyAssignment
  * Lagt till stöd för att skicka princip-URL till cmdletarna New-AzureRmPolicyDefinition och Set-AzureRmPolicyDefinition
  * Lagt till parametern -Mode i cmdlet New-AzureRmPolicyDefinition
  * Lagt till stöd för att ta bort rolltilldelning med hjälp av PSRoleAssignment-objekt
    - Användare kan nu använda PSRoleassignmnet inputobject med cmdlet Remove-AzureRMRoleAssignment för att ta bort rolltilldelningen.
  * Lagt till cmdletarna ManagedApplication
    - Cmdlet New-AzureRmManagedApplication för att skapa ett hanterat program
    - Cmdlet Get-AzureRmManagedApplication för att lista alla hanterade program under en prenumeration eller för att hämta ett visst hanterat program
    - Cmdlet Remove-AzureRmManagedApplication för att ta bort ett hanterat program
    - Cmdlet Set-AzureRmManagedApplication för att uppdatera ett befintligt hanterat program
  * Lagt till cmdletarna ManagedApplicationDefinition
    - Cmdlet New-AzureRmManagedApplicationDefinition för att skapa en definition för hanterade program med hjälp av uri för zip-fil eller med hjälp av json-filerna mainTemplate och createUiDefinition
    - Cmdlet Get-AzureRmManagedApplicationDefinition för att lista alla definitioner för hanterade program under en resursgrupp eller för att hämta en viss definition för hanterade program
    - Cmdlet Remove-AzureRmManagedApplicationDefinition för att ta bort en definition för hanterade program
    - Cmdlet Set-AzureRmManagedApplicationDefinition för att uppdatera en befintlig definition för hanterade program
* SQL
  * Lägger till stöd för regler för virtuellt nätverk
    - Lägger till cmdlet Get-AzureRmSqlServerVirtualNetworkRule som hämtar reglerna för virtuellt nätverk via ett visst regelnamn eller som en lista över regler för virtuellt nätverk på en Azure Sql-server.
    - Lägger till cmdlet Set-AzureRmSqlServerVirtualNetworkRule som ändrar vilket virtuellt nätverk regeln pekar mot.
    - Lägger till cmdlet Remove-AzureRmSqlServerVirtualNetworkRule som tar bort en regel för virtuellt nätverk för en Azure Sql-server.
    - Lägger till cmdlet New-AzureRmSqlServerVirtualNetworkRule som skapar en ny regel för virtuellt nätverk för en Azure Sql-server.
* Websites
  * Lägg till PremiumV2-nivå för App Service Plans
* Azure.Storage
  * Uppgradera till Azure Storage-klientbiblioteket 8.4.0 och Azure Storage DataMovement-biblioteket 0.6.1
  * Lägg till stöd för PremiumPageBlobTier i API för att ladda upp och kopiera blob
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * Förfina konsolutdataformatet för AzureStorageContainer, AzureStorageBlob, AzureStorageQueue, AzureStorageTable
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>2017.08.10 – version 4.3.1
  * Uppdatering för att åtgärda problem med signering av sammansättning

## <a name="20170807---version-430"></a>2017.08.07 – version 4.3.0
* AnalysisServices
  * Programfel i Set-AzureRmAnalysisServciesServer har åtgärdats
    - Om ingen admin angetts så tas admin bort.
  * BackupBlobContainerUri in New-AzureRmAnalysisServicesServer och Set-AzureRmAnalysisServicesServer har lagts till
    - Inställning/inaktivering av säkerhetskopia av blobcontainer för säkerhetskopiering/återställning av Azure Analysis Services Server har aktiverats
  * SKU-sökning i New-AzureRmAnalysisServicesServer och Set-AzureRmAnalysisServicesServer har uppdaterats
    - Hårdkodad SKU i dynamisk sökning har ändrats.
  * Add-AzureAnalysisServicesAccount som stöd för inloggning med tjänstens huvudnamn
* Automation
  * Ändringar har gjorts av AutomationDSC*-cmdletar för att hämta över 100 poster
  * Har löst problemet med att utförliga strömmar slutar fungera efter anrop av Automation-cmdletar (till exempel Get-AzureRmAutomationVariable, Get-AzureRmAutomationJob).
  * Stöd för versionshantering av NodeConfiguration-version har lagts till i StartAzureAutomationDscCompilationJob och ImportAzureAutomationDscNodeConfiguration
  * Korrigering av programfel för befintliga problem – Problemet med alias #3775 och runOn-alias och stöd för HybridWorkers har åtgärdats.
* Compute
  * Set-AzureRmVMAEMExtension: Lägg till stöd för nya Premium-diskstorlekar
  * Set-AzureRmVMAEMExtension: Lägg till stöd för M-serien
  * Lägg till ForceUpdateTag-parametern i Add-AzureRmVmssExtension
  * Lägg till Primary-parametern i New-AzureRmVmssIpConfig
  * Lägg till EnableAcceleratedNetworking-parametern i Add-AzureRmVmssNetworkInterfaceConfig
  * Lägg till InstanceId i Set-AzureRmVmss
  * Exponera MaintenanceRedeployStatus för Get-AzureRmVM -Status-utdata
  * Exponera begränsning och kapacitet för tabellformatet i Get-AzureRmComputeResourceSku
* DataLakeStore
  * Korrigering av problemet: https://github.com/Azure/azure-powershell/issues/4323
* EventHub
  * ResourceGroup-egenskapen har lagts till i NamespaceAttributes
    - ”ResourceGroup” hämtar namnet på den resursgrupp där namnområdet finns
  * Cmdletar med Parametersets för namnområde och EventHub för drift av AuthorizationRule har uppdateras
    - New-AzureRmEventHubAuthorizationRule – Lägger till en ny AuthorizationRule i befintligt NameSpace eller EventHub.
    - Get-AzureRmEventHubAuthorizationRule – Hämtar AuthorizationRule/lista över AuthorizationRules för befintligt NameSpace eller EventHub.
    - Set-AzureRmEventHubAuthorizationRule – Uppdaterat egenskaper för befintlig AuthorizationRule för EventHub NameSpace.
    - Remove-AzureRmEventHubAuthorizationRule – Tar bort befintlig AuthorizationRule för befintligt NameSpace eller EventHub.
    - New-AzureRmEventHubKey – Skapar ny primär/sekundär nyckel för AuthorizationRule för befintligt NameSpace eller EventHub.
    - Get-AzureRmEventHubKey – Hämtar ny primär/sekundär nyckel för AuthorizationRule för befintligt NameSpace eller EventHub.
* Nätverk
    * Stöd för IPv6 och ny valfri parameter har lagts till -PeerAddressType
      * New-AzureRmExpressRouteCircuitPeeringConfig:
      * Set-AzureRmExpressRouteCircuitPeeringConfig: Stöd för IPv6 har lagts till. Ny valfri parameter har lagts till
      * Remove-AzureRmExpressRouteCircuitPeeringConfig: Stöd för IPv6 har lagts till. Ny valfri parameter har lagts till
    * Parametern -ProbeEnabled har markerats som inaktuell
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* Profil
    * Datainsamling har aktiverats som standard. Användningsdata samlas in av Microsoft för att förbättra användarupplevelsen. Data är anonyma och omfattar inte värden för kommandoradsargument.
      - Använd cmdleten Disable-AzureRmDataCollection för att inaktivera funktionen
      - Använd cmdleten Enable-AzureRmDataCollection för att aktivera funktionen
* Resurser
    * Lägg till stöd för verifiering av omfång för följande rolldefinitions- och rolltilldelningskommandon innan förfrågan skickas till ARM
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
  * Följande nya kommandon för AuthorizationRules för NameSpace, Queue och Topic har lagts till. i enlighet med parameterinställningen har auktoriseringsreglerna utförts.
    - New-AzureRmServiceBusAuthorizationRule – Lägger till en ny AuthorizationRule i befintlig ServiceBus NameSpace/Queue/Topic.
    - Get-AzureRmServiceBusAuthorizationRule – Hämtar AuthorizationRule/lista över AuthorizationRules för befintlig ServiceBus NameSpace/Queue/Topic.
    - Set-AzureRmServiceBusAuthorizationRule – Uppdaterar egenskaperna för befintlig AuthorizationRule för Servicebus NameSpace/Queue/Topic.
    - New-AzureRmServiceBusKey – Skapar en ny primär/sekundär nyckel för AuthorizationRule för befintlig ServiceBus NameSpace/Queue/Topic.
    - Get-AzureRmServiceBusKey – Hämtar primär/sekundär nyckel för AuthorizationRule för befintlig ServiceBus NameSpace/Queue/Topic.
    - Remove-AzureRmServiceBusNamespaceAuthorizationRule – Tar bort befintlig AuthorizationRule för ServiceBus NameSpace/Queue/Topic.
  * Egenskap för resursgrupp har lagts till i NamespceAttributes

* SQL
    * Uppdaterar Set-AzureRmSqlServerTransparentDataEncryptionProtector så att en varning visas och bekräftelse krävs om krypteringsskyddstypen är AzureKeyVault
    * Lägger till nya uppdaterade cmdletar för granskningsinställningar
      - Get-AzureRmSqlDatabaseAuditing-cmdlet som hämtar granskningsinställningarna för en Azure SQL-databas.
      - Get-AzureRmSqlServerAuditing-cmdlet som hämtar granskningsinställningarna för en Azure SQL-server.
      - Set-AzureRmSqlDatabaseAuditing-cmdlet som ändrar granskningsinställningarna för en Azure SQL-databas.
      - Set-AzureRmSqlServerAuditing-cmdlet som ändrar granskningsinställningarna för en Azure SQL-server.
    * Avvecklar befintliga cmdletar för granskningsprincipen
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * Parsning av schemafil för Update-AzureRmSqlSyncGroup är nu skiftlägeskänslig.
* Storage
    * Lägg till NetworkRule-stöd för cmdletar för lagringskontot i resursläget
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>2017.07.17 – version 4.2.1
* Compute
  - Åtgärda problemet med VM-disken och VM-diskens ögonblicksbild för att skapa och uppdatera cmdletar, (länk)[<https://github.com/azure/azure-powershell/issues/4309>]
    - New-AzureRmDisk
    - New-AzureRmSnapshot
    - Update-AzureRmDisk
    - Update-AzureRmSnapshot
* Profil
  - Åtgärda problemet med icke-interaktiv användarautentisering i RDFE (länk) [<https://github.com/Azure/azure-powershell/issues/4299>]

* ServiceManagement
  - Åtgärda problemet med icke-interaktiv användarautentisering (länk) [<https://github.com/Azure/azure-powershell/issues/4299>]

## <a name="2017711---version-420"></a>2017.7.11 – version 4.2.0
* AnalysisServices
    * Lägg till nytt API för dataplanen
        - API för att hämta AS-serverloggen har introducerats, Export-AzureAnalysisServicesInstanceLog
* Automation
    * Korrekt inställning av värdet TimeZone för vecko- och månadsscheman för New-AzureRmAutomationSchedule
        - Mer information finns i det här problemet: https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - Ny cmdlet, Get-AzureBatchJobPreparationAndReleaseTaskStatus, har lagts till.
    - Start och slut för byteintervall har lagts till i parametrarna för Get-AzureBatchNodeFileContent.
* CognitiveServices
    * Integrera med Cognitive Services Management SDK, version 1.0.0.
    * Åtgärda ett fel med kontrollen av längden på kontonamnet.
* Compute
    * Stöd för lagringskontotypen för avbildningsdisken:
        - Parametern ”StorageAccountType” har lagts till i Set-AzureRmImageOsDisk och Add-AzureRmImageDataDisk
    * Funktionen PrivateIP och PublicIP i Vmss Ip-konfigurationen:
        - Namnen ”PrivateIPAddressVersion”, ”PublicIPAddressConfigurationName”, ”PublicIPAddressConfigurationIdleTimeoutInMinutes”, ”DnsSetting” har lagts till i New-AzureRmVmssIpConfig
        - Parametern ”PrivateIPAddressVersion” för att ange IPv4 eller IPv6 har lagts till i New-AzureRmVmssIpConfig
    * Funktion för prestandaunderhåll:
        - Växlingsparametern ”PerformMaintenance” har lagts till i Restart-AzureRmVM.
        - Get-AzureRmVM -Status visar information om prestandaunderhåll för angiven virtuell dator
    * Identitetsfunktion för virtuell dator:
        - Parametern ”IdentityType” har lagts till i New-AzureRmVMConfig och UpdateAzureRmVM
        - Get-AzureRmVM visar identitetsinformationen för den angivna virtuella datorn
    * Funktion för Vmss-identitet:
        - Parametern ”IdentityType” har lagts till i New-AzureRmVmssConfig
        - Get-AzureRmVmss visar identitetsinformationen för angiven Vmss
    * Funktion för Vmss-startdiagnostik:
        - Ny cmdlet för att ställa in diagnostik av Vmss-objekt: Set-AzureRmVmssBootDiagnostics
        - Parametern ”BootDiagnostic” har lagts till i New-AzureRmVmssConfig
    * Funktionen Vmss LicenseType:
        - Parametern ”LicenseType” har lagts till i New-AzureRmVmssConfig
    * Stöd för RecoveryPolicyMode:
        - Parametern ”RecoveryPolicyMode” har lagts till i New-AzureRmVmssConfig
    * Funktion för beräkningsresurs-SKU:
        - Ny cmdlet, ”Get-AzureRmComputeResourceSku”, listar alla beräkningsresurs-SKU:er
* DataFactories
    * Avverka New-AzureRmDataFactoryGatewayKey
    * Introducera funktionen för gateway-auktoriseringsnyckeln genom att lägga till New-AzureRmDataFactoryGatewayAuthKey och Get-AzureRmDataFactoryGatewayAuthKey
* DataLakeAnalytics
    * Lägg till stöd för beräkningsprincip-CRUD med hjälp av följande kommandon:
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * Lägg till stöd för metadata för jobbrelationen för hjälp med återkommande jobb och jobbpipeliner. Följande kommandon har uppdaterats eller lagts till:
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * Tokenmålgruppen för jobb- och katalog-API:er har uppdaterats för att använda rätt Data Lake-specifik målgrupp i stället för Azure Resource-målgruppen.
* DataLakeStore
    * Stöd har lagts till för användarhanterade KeyVault-nyckelrotationer i cmdleten Set-AzureRMDataLakeStoreAccount
    * Uppdatering av livskvalitet har lagts till för att automatiskt utlösa ett `enableKeyVault`-anrop när ett användarhanterat KeyVault läggs till eller en nyckel roteras.
    * Tokenmålgruppen för jobb- och katalog-API:er har uppdaterats för att använda rätt Data Lake-specifik målgrupp i stället för Azure Resource-målgruppen.
    * Ett fel som begränsar storleken på filer som skapas/läggs till med följande cmdletar har åtgärdats:
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* DNS
    * Åtgärda fel i pipingscenariot för Get-AzureRmDnsZone
        - Mer information finns här: https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * Stöd för att aktivera/inaktivera Operations Management Suite (OMS) har lagts till
    * Nya cmdletar
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * Lägg till nya parametrar för att ställa in anpassade Spark-konfigurationer i Add-AzureRmHDInsightConfigValues
        - Parametrarna SparkDefaults och SparkThriftConf för Spark 1.6
        - Parametrarna Spark2Defaults och Spark2ThriftConf för Spark 2.0
* Insikter
    * Problem nr. 4215 (ändringsbegäran) tar bort 15-dagarsgränsen i tidsperioden för cmdleten Get-AzureRmLog. Även mindre ändringar av enhetens testnamn.
    * Problem nr. 3957 är åtgärdat för Get-AzureRmLog
        - Problem nr. 1: Serverdelen returnerar poster på sidor med 200 poster vardera, som är länkade genom fortsättningstoken till nästa sida. Kunderna har sett att cmdleten endast returnerar 200 poster när de visste att det fanns fler. Detta hände oavsett vilket värde som ställdes in för MaxEvents, såvida inte värdet var mindre än 200.
        - Problem nr. 2: Dokumentationen innehöll felaktiga data om denna cmdlet, t.ex. att standardtidsperioden var 1 timme.
        - Korrigering nr. 1: Cmdleten följer nu fortsättningstoken som returneras av serverdelen tills den når MaxEvents eller slutet på uppsättningen.<br>Standardvärdet för MaxEvents är 1 000 och det högsta värdet är 100 000. Ett värde för MaxEvents som är mindre än 1 ignoreras och standardvärdet används i stället. Dessa värden och beteenden har inte ändrats. De dokumenteras nu på rätt sätt.<br>Ett alias för MaxEvents har lagts till, MaxRecords, eftersom namnet på cmdleten inte talar om händelser längre, utan endast om loggarna.
        - Korrigering nr. 2: Dokumentationen innehåller korrekt och mer detaljerad information: nytt alias, korrekt tidsperiod, rätt standard, minimum- och maximumvärden.
* KeyVault
    * Ta bort e-postadressen från katalogfrågan när -UserPrincipalName anges för cmdletarna Set-AzureRMKeyVaultAccessPolicy och Remove-AzureRMKeyVaultAccessPolicy.
      - Båda cmdletarna har nu en -EmailAddress-parameter som kan användas i stället för parametern -UserPrincipalName när frågor efter e-postadress är olämpliga.  Om det finns fler än en matchande e-postadress i katalogen misslyckas cmdleten.
* Nätverk
    * New-AzureRmIpsecPolicy: SALifeTimeSeconds och SADataSizeKilobytes är inte längre obligatoriska parametrar
        - SALifeTimeSeconds anges som standard till 27 000 sekunder
        - SADataSizeKilobytes anges som standard till 102 400 000 KB
    * Stöd har lagts till för anpassad chiffersvitkonfiguration med SSL-princip och för att ange alla SSL-alternativ för API:t i Application Gateway
        - Valfri parameter har lagts till: -PolicyType, -PolicyName, -MinProtocolVersion, -Ciphersuite
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - Get-AzureRmApplicationGatewayAvailableSslOptions har lagts till (Alias: List-AzureRmApplicationGatewayAvailableSslOptions)
        - Get-AzureRmApplicationGatewaySslPredefinedPolicy har lagts till (Alias: List-AzureRmApplicationGatewaySslPredefinedPolicy)
    * Omdirigeringsstöd har lagts till i Application Gateway
        - Add-AzureRmApplicationGatewayRedirectConfiguration har lagts till
        - Get-AzureRmApplicationGatewayRedirectConfiguration har lagts till
        - New-AzureRmApplicationGatewayRedirectConfiguration har lagts till
        - Remove-AzureRmApplicationGatewayRedirectConfiguration har lagts till
        - Set-AzureRmApplicationGatewayRedirectConfiguration har lagts till
        - Valfri parameter har lagts till: -RedirectConfiguration
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - Valfri parameter har lagts till: -DefaultRedirectConfiguration
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - Valfri parameter har lagts till: -RedirectConfiguration
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - Valfri parameter har lagts till: -RedirectConfigurations
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Stöd för azure-webbplatser har lagts till i Application Gateway
        - New-AzureRmApplicationGatewayProbeHealthResponseMatch har lagts till
        - Valfria parametrar har lagts till: -PickHostNameFromBackendHttpSettings, -MinServers, -Match
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - Valfria parametrar har lagts till: -PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled, -Path
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * Uppdatera Get-AzureRmPublicIPaddress för att hämta publicipaddress-resurser som skapas via en VM-skalningsuppsättning
    * Cmdlet har lagts till för att hämta aktuell användning för virtuellt nätverk
        - Get-AzureRmVirtualNetworkUsageList
* Profil
    * Åtgärdat fel när Import-AzureRmContext eller Save-AzureRmContext används
        - Mer information finns i det här problemet: https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * Introducerar en ny modul för Azure Site Recovery-åtgärder.
        - Alla cmdletar börjar med AzureRmRecoveryServicesAsr*
* SQL
    * Lägg till cmdletar för datasynkronisering för PowerShell i AzureRM.Sql
    * Uppdaterade AzureRmSqlServer-cmdletar för att använda den nya REST API-versionen som undviker tidsgränser när servern skapas.
    * Föråldrade cmdletar för serveruppgradering eftersom den gamla serverversionen (2.0) inte längre finns.
    * Lägg till en ny valfri växlingsparameter "AssignIdentity" i cmdletarna New-AzureRmSqlServer och Set-AzureRmSqlServer för att ge stöd för etablering av en resursidentitet för SQL server-resursen
    * Parametern ResourceGroupName är nu valfri för Get-AzureRmSqlServer
        - Mer information finns i följande problem: https://github.com/Azure/azure-powershell/issues/635
* ServiceManagement för ExpressRoute:
    * Cmdleten New-AzureBgpPeering har uppdaterats för att lägga till följande nya alternativ:
        - PeerAddressType: Värdena för "IPv4" eller "IPv6" kan specificeras för att skapa en BGP-peering av motsvarande adressfamiljtyp
    * Cmdleten Set-AzureBgpPeering har uppdaterats för att lägga till följande nya alternativ:
        - PeerAddressType: värdena för "IPv4" eller "IPv6" kan anges för att uppdatera BGP-peering av motsvarande adressfamiljtyp
    * Cmdleten Remove-AzureBgpPeering har uppdaterats för att lägga till följande nya alternativ:
        - PeerAddressType: värdena "IPv4", "IPv6" eller All kan specificeras för att ta bort BGP-peering av motsvarande adressfamiljtyp eller alla

## <a name="20170607---version-410"></a>2017.06.07 – version 4.1.0
* AnalysisServices
    * Nya SKU:er har lagts till: B1, B2, S0
    * Stöd för att skala upp/ned har lagts till
* CognitiveServices
    * Uppdatera detaljerad visning av licensavtal när Cognitive Services-resurser skapas
* Compute
    * Åtgärda Test-AzureRmVMAEMExtension för virtuella maskiner med flera hanterade diskar
    * Set-AzureRmVMAEMExtension har uppdaterats: Lägg till information om cachelagring för Premium Managed Disks
    * Add-AzureRmVhd: Storleksgränsen för VHD har ökats till 4 TB.
    * Stop-AzureRmVM: Förtydliga dokumentationen för parametern STayProvisioned
    * New-AzureRmDiskUpdateConfig
      * Föråldrade parametrar CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId
    * Set-AzureRmDiskUpdateImageReference: Föråldrad cmdlet
    * New-AzureRmSnapshotUpdateConfig
      * Föråldrade parametrar CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId
    * Set-AzureRmSnapshotUpdateImageReference: Föråldrad Cmdlet
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * Aktivera hanterad KeyVault-kryptering för DataLake-lagring
* DevTestLabs
    * Uppdatera cmdletar så att de fungerar med den aktuella och uppdaterade DevTest Labs API-versionen.
* IotHub
    * Lägg till routningsstöd för IoTHub-cmdletar
* KeyVault
  * Nya cmdletar har stöd för hanterade KeyVault-lagringskontonycklar
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* Nätverk
    * Get-AzureRmNetworkUsage: Ny cmdlet visar nätverksanvändning och kapacitetsinformation
    * Nya GatewaySku-alternativ har lagts till för VirtualNetworkGateways
        * VpnGw1, VpnGw2, VpnGw3 är de nya SKU:erna som har lagts till för VPN-gatewayer
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * Åtgärdade hjälpexempel
* NotificationHubs
    * Transparent uppdatering av NotificationHubs-cmdletar för nytt API
* Profil
    * Resolve-AzureRmError
      * Ny cmdlet visar information om fel och undantag som utlöses av cmdletar, inklusive serverförfrågan/svarsdata
    * Send-Feedback
      * Sändning av feedback utan inloggning har aktiverats
    * Get-AzureRmSubscription
      * Åtgärda fel vid hämtning av CSP-prenumerationer
* Resurser
    * Åtgärdat problem där Get-AzureRMRoleAssignment ger en felaktig förfrågan om antalet rolltilldelningar är fler än 1 000
        * Användarna kan nu använda Get-AzureRMRoleAssignment även om de rolltilldelningar som returneras är fler än 1 000
* SQL
    * Restore-AzureRmSqlDatabase: Uppdatera dokumentationsexempel
* Storage
    * Lägg till stöd för AssignIdentity-inställningen för cmdletar för lagringskontot i resursläget
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * Lägg till stöd för kundnyckeln för cmdletar för lagringskontot i resursläget
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * Nya övervakningsinställningar ”MonitorIntervalInSeconds”, ”MonitorTimeoutInSeconds”, ”MonitorToleratedNumberOfFailures”
    * Nytt övervakningsprotokoll ”TCP”
* ServiceManagement
    * Add-AzureVhd: Storleksgränsen för VHD har ökats till 4 TB.
    * New-AzureBGPPeering: Stöd för LegacyMode
* Azure.Storage
    * Uppdatera hjälp för parametrar som godkänner jokertecken och uppdatera StorageContext-typ

## <a name="20170523---version-402"></a>2017.05.23 – version 4.0.2
* Profil
    * Add-AzureRmAccount
      * Parameteralias `-EnvironmentName` har lagts till för bakåtkompatibilitet med 2.x-versioner av AzureRM.profile

## <a name="20170512---version-401"></a>2017.05.12 – version 4.0.1
 * Åtgärda problemet med New-AzureStorageContext i offline-scenarier: https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>2017.05.10 – version 4.0.0


* Den här versionen innehåller större ändringar. Se [migreringsguiden](https://aka.ms/azps-migration-guide) för information om ändringar hur de påverkar befintliga skript.
* ApiManagement
  - Stöd har lagts till för att konfigurera externa grupper i New-AzureRmApiManagementGroup.
* Fakturering
  - Ny cmdlet Get-AzureRmBillingPeriod
    + cmdlet för att hämta azure-faktureringsperioder för prenumerationen.
  - Uppdaterad cmdlet Get-AzureRmBillingInvoice
  - ny egenskap BillingPeriodNames
  - utdata i listvyn
* Compute
  - Uppdaterade cmdletar Set-AzureRmVMAEMExtension och Test-AzureRmVMAEMExtension för att stödja Premium-hanterade diskar
  - Krypteringsinställningar för säkerhetskopiering av IaaS-VM:ar och återställning vid fel
  - Alternativet ChefServiceInterval byter namn till ChefDaemonInterval. Den gamla kommer dock fortsätta att fungera.
  - Duplicerade egenskaper för DataDiskNames och NetworkInterfaceIDs har tagits bort från PS VM-objekt.
  - Parametrarna DataDiskNames och NetworkInterfaceIDs har gjorts valfria i Remove-AzureRmVMDataDisk och Remove-AzureRmVMNetworkInterface.
  - Rörledningsproblemet vid Get cmdlets när Get cmdlets returnerar ett listobjekt.
  - Cmdletar som är i konflikt med RDFE-cmdletar har bytt namn. Mer information finns i problemet https://github.com/Azure/azure-powershell/issues/2917
    + `New-AzureVMSqlServerAutoBackupConfig` har bytt namn till `New-AzureRmVMSqlServerAutoBackupConfig`
    + `New-AzureVMSqlServerAutoPatchingConfig` har bytt namn till `New-AzureRmVMSqlServerAutoPatchingConfig`
    + `New-AzureVMSqlServerKeyVaultCredentialConfig` har bytt namn till `New-AzureRmVMSqlServerKeyVaultCredentialConfig`
* Förbrukning
  - Ny cmdlet Get-AzureRmConsumptionUsageDetail
    + cmdlet för att användningsinformation för prenumerationen.
* ContainerRegistry
  - Lägg till PowerShell-cmdletar för Azure-containerregistret
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - Stöd läggs till för hämta och lista katalogpaket
  - Stöd läggs till för att lista följande katalogobjekt från djupare överordnade:
    + Tabell
    + TVF
    + Visa
    + Statistik
* DataLakeStore
  - Spårningsloggning för `Import-AzureRMDataLakeStoreItem` och `Export-AzureRMDataLakeStoreItem` har inaktiverats som standard för att förbättra prestandan. Om du vill ha loggningsspårning, använder du parametrarna `-DiagnosticLogLevel` och `-DiagnosticLogPath`
  - En bugg som ibland gjorde att PowerShell kraschade vid uppladdning av många små filer till ADLS har fixats.
* EventHub
  - Felkorrigering:
    + Korrigering för cmdlet-felet i Set-AzureRmEventHubNamespace: ”Nivå” kan inte vara null när den ska vara ”SkuName”
    + Set-AzureRmEventHub – korrigering av objektreferensen inte inställd till en instans av ett objektfel vid uppdatering av EventHub
* Insikter
  - Add-AzureRm*AlertRule
    + Returnerar ett objekt: newResource, statusCode, requestId
  - Get-AzureRmAlertRule
    + Utdata räknas nu upp istället för att betraktas som ett enda objekt. Typen har inte ändrats, det är fortfarande en lista.
  - Remove-AzureRmAlertRule
    + StatusCode följer statuskoden som returneras av begäran, innan var det alltid Ok.
  - Add-AzureRmAutoscaleSetting
    + Returnerar nu ett enskilt objekt (inte en lista som tidigare) som innehåller statusCode, requestId och den nyligen skapade/uppdarerade resursen.
    + Statuskoden följer den status som begäran returnerar, innan var den alltid Ok.
  - New-AzureRmAutoscaleRule
    + Parametern ScaleActionType har utökats, den tar nu emot följande värden: ChangeCount, PercentChangeCount, ExactCount.
  - Remove-AzureRmAutoscaleSetting
    + StatusCode i utdata följer statusCode som returnerades av begäran. Innan var den alltid Ok.
  - Get-AzureRMLogProfile
    + Utdata räknas nu upp. Innan ansågs den som ett enda objekt. Utdatatypen fortsätter att vara en lista som tidigare.
  - Remove-AzureRmLogProfile
    + PassThru-parametern har implementerats.
  - Mått-API
    + SDK:n hämtar nu mått från MDM.
  - Get-AzureRmMetricDefinition
    + Utdata är fortfarande en lista, men listans struktur har ändrats.
  - Get-AzureRmMetric
    + Anropet har ändrats. Detta är den nya syntaxen: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]
    + Utdata är en lista och strukturen för dess element har förändrats.
* KeyVault
  - Lägger till stöd för säkerhetskopiering/återställning av KeyVault-hemligheter
    + Hemligheter kan säkerhetskopieras och återställas, vilket matchar de funktioner som stöds för nycklar för tillfället

  - Säkerhetskopierings-cmdletar för nycklar och hemligheter accepterar nu ett motsvarande objekt som indataparameter
    + Anroparen kan kedja hämtning och säkerhetskopiering: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - Säkerhetskopierings-cmdletar stöder nu en -Force växel för att skriva över en befintlig fil
    + Observera att försök att skriva över en befintlig fil inte längre kommer att misslyckas, utan istället tillfrågas användaren hur denne vill fortsätta.
* LogicApp
  - Nya parametrar för katastrofåterställnings-cmdletars utbyteskontrollnummer:
    + Valfri -AgreementType-parameter ("X12", eller "Edifact") för att specificera de relevanta kontrollnumren
* MachineLearning
  - Använd en ny version av Azure Machine Learning .Net-SDK:n och lägg till en ny cmdlet
    + Add-AzureRmMlWebServiceRegionalProperty
  - Mindre textkorrigeringar i hjälptexten.
* Nätverk
  - Lade till cmdleten Test-AzureRmNetworkWatcherConnectivity
    + Returnerar anslutningsinformation för en angiven käll-VM och ett mål
    + Om anslutningen mellan källa och mål inte går att upprätta, returnerar cmdleten information om problemet
* Profil
  - Lade till cmdleten Send-Feedback: låter en användare starta en uppsättning prompter som skickar feedback till Azure PowerShell-teamet.
  - Följande alias har tagits bort eftersom de är i konflikt med befintliga cmdlet-namn i Azure-modulen:
    + `Enable-AzureDataCollection` (stöds av `Enable-AzureRmDataCollection`)
    + `Disable-AzureDataCollection` (stöds av `Disable-AzureRmDataCollection`)
* Vidarebefordran
  - Lägger till cmdletar för Azure-Relay, som låter användare skapa och hantera alla Azure Relay-resurser.
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* Resurser
  - Stöd för distributioner över resursgrupper för New-AzureRmResourceGroupDeployment
    + Användare kan nu använda kapslade distributioner för att distribuera till olika resursgrupper.
* ServiceBus

  - Felkorrigering: Egenskapsvärdena för ServiceBus-köobjektet var satt till null, objektet används som indataparameter i cmdleten Set-AzureRmServiceBusQueue för att uppdatera kön.
    - Egenskaper som påverkas är LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount och MessageCount
* ServiceFabric

  - Lade till cmdletar för Service Fabric
    + Add-AzureRmServiceFabricApplicationCertificate       Lägg till ett certifikat som kommer att användas som programcertifikat
    + Add-AzureRmServiceFabricClientCertificate       Lägg till ett namn eller tumavtryck till klusterinställningarna för klientautentiseringen
    + Add-AzureRmServiceFabricClusterCertificate       Lägg till ett sekundärt klustercertifikat till klustret för att rulla över det tidigare certifikatet
    + Add-AzureRmServiceFabricNodes Lägg till noder/VM:ar av en specifik nodtyp till ett kluster
    + Add-AzureRmServiceFabricNodeType Lägg till en nodtyp/VM:ar till ett befintligt kluster
    + Get-AzureRmServiceFabricCluster hämta information om klusterresursen
    + New-AzureRmServiceFabricCluster Skapa ett nytt ServiceFabric-kluster. Det här kommandot har många överlagringar för att täcka olika scenarier
    + Remove-AzureRmServiceFabricClientCertificate       Ta bort ett klientcertifikat från att användas för åtkomst till ett kluster
    + Remove-AzureRmServiceFabricClusterCertificate       Ta bort ett klustercertifikat från att användas för klustersäkerhet
    + Remove-AzureRmServiceFabricNodes       Ta bort noder från en specifik nodtyp från ett kluster
    + Remove-AzureRmServiceFabricNodeType       Ta bort en nodtyp från ett kluster
    + Remove-AzureRmServiceFabricSettings       Ta bort en eller flera ServiceFabric-inställningar från ett kluster
    + Set-AzureRmServiceFabricSettings       Lägg till eller uppdatera en eller flera ServiceFabric-inställningar för ett kluster
    + Set-AzureRmServiceFabricUpgradeType       Ändra ServiceFabric-uppgraderingstypen för ett kluster
    + Update-AzureRmServiceFabricDurability       Ändra hållbarhetsnivån för ett kluster
    + Update-AzureRmServiceFabricReliability       Ändra tillförlitlighetsnivån för ett kluster
* SQL
  - Lade till parametern -SampleName till New-AzureRmSqlDatabase
  - Uppdateringar till redundansgrupp-cmdletar
  - Tog bort Tagg-parametrarna
  - Tog bort parametrarna PartnerResourceGroupName och PartnerServerName från cmdleten Remove-AzureRmSqlDatabaseFailoverGroup
  - Lade till parametern GracePeriodWithDataLossHours till cmdletarna New- och Set- som så småningom kommer ersätta GracePeriodWithDataLossHour
  - Dokumentation har utökats och uppdaterats
  - Formateringen för returnerade objekt har ändrats och en del fel har korrigerats där fält inte alltid var ifyllda
  - Egenskaperna DatabaseNames och PartnerLocation har lagts till i redundansgruppobjektet
  - Felet som gjorde att Switch-cmdleten returnerade omedelbart istället för att vänta tills åtgärden var slutförd har korrigerats
  - Felet med heltalsspill har korrigerats för när ett högt respitperiodvärde används
  - Justera respitperioden till minst 1 timme om en lägre sådan anges
  - Ta bort "Usage_Anomaly" från godkända värden för "ExcludedDetectionType"-parametern för cmdleten Set-AzureRmSqlDatabaseThreatDetectionPolicy och cmdleten Set-AzureRmSqlServerThreatDetectionPolicy.
* Storage
  - Uppgradera SRP SDK till 6.3.0
  - New/Set-AzureRmStorageAccount:Lägg till en ny parameter för att stödja EnableHttpsTrafficOnly
  - New/Set/Get-AzureRmStorageAccount: Returnerat lagringskonto innehåller ett nytt attribut EnableHttpsTrafficOnly
* Azure.Storage
  - Uppgradera till Azure Storage-klientbiblioteket 8.1.1 och Azure Storage DataMovement-biblioteket 0.5.1
  - Lägg till en ny cmdlet för att stödja den inkrementella kopieringsfunktionen i blobbar
