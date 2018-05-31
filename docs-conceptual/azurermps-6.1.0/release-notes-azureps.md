---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/23/2018
ms.locfileid: "34462141"
---
# <a name="release-notes"></a>Viktig information

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

---
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