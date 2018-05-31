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
# <a name="release-notes"></a><span data-ttu-id="34017-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="34017-103">Release notes</span></span>

<span data-ttu-id="34017-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="34017-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="34017-105">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="34017-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="34017-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34017-106">AzureRM.Profile</span></span>
* <span data-ttu-id="34017-107">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="34017-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="34017-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="34017-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="34017-109">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="34017-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="34017-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="34017-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="34017-111">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="34017-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="34017-112">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="34017-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="34017-113">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="34017-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="34017-114">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="34017-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="34017-115">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="34017-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="34017-116">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="34017-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="34017-117">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="34017-117">Added support for MSI identity</span></span>
* <span data-ttu-id="34017-118">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="34017-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="34017-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="34017-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="34017-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="34017-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="34017-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="34017-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="34017-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="34017-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="34017-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="34017-123">AzureRM.Batch</span></span>
* <span data-ttu-id="34017-124">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="34017-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="34017-125">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="34017-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="34017-126">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="34017-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="34017-127">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="34017-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="34017-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34017-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="34017-129">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="34017-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="34017-130">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="34017-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="34017-131">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="34017-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="34017-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34017-132">AzureRM.Network</span></span>
* <span data-ttu-id="34017-133">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="34017-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="34017-134">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="34017-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="34017-135">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="34017-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="34017-136">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="34017-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="34017-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="34017-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="34017-138">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="34017-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="34017-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="34017-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="34017-140">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="34017-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="34017-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="34017-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="34017-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="34017-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="34017-143">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="34017-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="34017-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="34017-144">AzureRM.Sql</span></span>
* <span data-ttu-id="34017-145">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="34017-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="34017-146">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="34017-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="34017-147">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="34017-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="34017-148">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="34017-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="34017-149">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="34017-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="34017-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="34017-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="34017-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="34017-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="34017-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="34017-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="34017-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="34017-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="34017-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="34017-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="34017-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="34017-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="34017-156">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="34017-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>