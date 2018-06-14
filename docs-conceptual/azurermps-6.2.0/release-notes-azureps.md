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
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853465"
---
# <a name="release-notes"></a><span data-ttu-id="7cc12-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="7cc12-103">Release notes</span></span>

<span data-ttu-id="7cc12-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="7cc12-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="7cc12-105">6.2.0 – juni 2018</span><span class="sxs-lookup"><span data-stu-id="7cc12-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7cc12-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7cc12-106">AzureRM.Profile</span></span>
* <span data-ttu-id="7cc12-107">Åtgärda problemet med att version 10.0.3 av Newtonsoft.Json inte lästes in vid modulimporten</span><span class="sxs-lookup"><span data-stu-id="7cc12-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7cc12-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7cc12-108">AzureRM.Compute</span></span>
* <span data-ttu-id="7cc12-109">VMSS VM-uppdateringsfunktion</span><span class="sxs-lookup"><span data-stu-id="7cc12-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="7cc12-110">Cmdletarna Update-AzureRmVmssVM och New-AzureRmVMDataDisk har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="7cc12-111">Lägg till parametern VirtualMachineScaleSetVM till cmdleten Add-AzureRmVMDataDisk så att det går att lägga till en datadisk i den virtuella Vmss-datorn.</span><span class="sxs-lookup"><span data-stu-id="7cc12-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="7cc12-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7cc12-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="7cc12-113">SDK:n för ADF .Net har uppdaterats till version 0.8.0-preview som innehåller följande ändringar:</span><span class="sxs-lookup"><span data-stu-id="7cc12-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="7cc12-114">Åtgärden för att konfigurera fabrikslagringsplatsen har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="7cc12-115">QuickBooks LinkedService har uppdaterats för att visa egenskaperna consumerKey och consumerSecret</span><span class="sxs-lookup"><span data-stu-id="7cc12-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="7cc12-116">Flera modelltyper från SecretBase till Object har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7cc12-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="7cc12-117">Utlösaren Blob Events har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="7cc12-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7cc12-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7cc12-119">Uppdatera dokumentation med exempel på utdata</span><span class="sxs-lookup"><span data-stu-id="7cc12-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="7cc12-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7cc12-120">AzureRM.Network</span></span>
* <span data-ttu-id="7cc12-121">Aktivera Trafikanalys-parametrar på Network Watcher-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7cc12-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="7cc12-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="7cc12-122">AzureRM.Resources</span></span>
* <span data-ttu-id="7cc12-123">Åtgärda problemet med egenskapen "Properties" för objekt(en) "PSResource" som returneras från "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="7cc12-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="7cc12-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="7cc12-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="7cc12-125">Åtgärda problemet med att nya autentiseringsvärden inte anges vid uppdatering av ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="7cc12-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="7cc12-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7cc12-126">AzureRM.Sql</span></span>
* <span data-ttu-id="7cc12-127">Följande cmdletar har uppdaterats med valfri LicenseType-parameter</span><span class="sxs-lookup"><span data-stu-id="7cc12-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="7cc12-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7cc12-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="7cc12-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7cc12-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="7cc12-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7cc12-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="7cc12-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7cc12-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="7cc12-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7cc12-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="7cc12-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="7cc12-133">AzureRM.Websites</span></span>
* <span data-ttu-id="7cc12-134">New-AzureRMWebApp har uppdaterats för att använda vanliga algoritmer från biblioteket Strategy.</span><span class="sxs-lookup"><span data-stu-id="7cc12-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="7cc12-135">6.1.0 – maj 2018</span><span class="sxs-lookup"><span data-stu-id="7cc12-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7cc12-136">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7cc12-136">AzureRM.Profile</span></span>
* <span data-ttu-id="7cc12-137">Åtgärda problem där en körning av Clear-AzureRmContext skulle bevara en tom kontext med namnet på den föregående standardkontexten som gjorde att användaren inte kunde skapa en ny kontext med det gamla namnet</span><span class="sxs-lookup"><span data-stu-id="7cc12-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="7cc12-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7cc12-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="7cc12-139">Aktivera Gateway associerings- och avassocieringsåtgärder på AS.</span><span class="sxs-lookup"><span data-stu-id="7cc12-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="7cc12-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7cc12-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="7cc12-141">Stöd för ApiVersions, ApiReleases och ApiRevisions har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="7cc12-142">Stöd för serverdelen på ServiceFabric har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="7cc12-143">Stöd för Application Insights-loggare har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="7cc12-144">Stöd för att identifiera SKU:n ”Basic” som en giltig SKU för Api Management-tjänsten har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="7cc12-145">Stöd för att installera certifikat som utfärdats av privata certifikatutfärdare som rot eller certifikatutfärdare har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="7cc12-146">Stöd för att godkänna anpassade SSL-certifikat via KeyVault och flera proxy-värdnamn har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="7cc12-147">Stöd för MSI-identitet har lagts till</span><span class="sxs-lookup"><span data-stu-id="7cc12-147">Added support for MSI identity</span></span>
* <span data-ttu-id="7cc12-148">Stöd för att godkänna principer via URL har lagts till. Obs! Följande cmdletar blir inaktuella i framtida versioner</span><span class="sxs-lookup"><span data-stu-id="7cc12-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="7cc12-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="7cc12-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="7cc12-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cc12-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="7cc12-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="7cc12-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="7cc12-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="7cc12-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="7cc12-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="7cc12-153">AzureRM.Batch</span></span>
* <span data-ttu-id="7cc12-154">Släpp nya cmdleten Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="7cc12-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="7cc12-155">Släpp nya cmdleten Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="7cc12-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="7cc12-156">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="7cc12-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="7cc12-157">Lägg till nya parametrar Expand, ResourceGroup, InstanceName, InstanceId, Tags och Top på cmdleten Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="7cc12-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="7cc12-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cc12-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="7cc12-159">Åtgärda exempel för Export AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="7cc12-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="7cc12-160">Åtgärda undantag för null-parameter för rekursivt ärende i Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7cc12-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="7cc12-161">Åtgärda hjälpfilerna för Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7cc12-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="7cc12-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7cc12-162">AzureRM.Network</span></span>
* <span data-ttu-id="7cc12-163">Öka nätverkets SDK-version från förhandsversionen 18.0.0 till förhandsversionen 19.0.0</span><span class="sxs-lookup"><span data-stu-id="7cc12-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="7cc12-164">Cmdlet har lagts till för att skapa protokollinformation</span><span class="sxs-lookup"><span data-stu-id="7cc12-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="7cc12-165">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cc12-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="7cc12-166">Cmdlet har lagts till för att lägga till en ny kretsanslutning till en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="7cc12-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="7cc12-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7cc12-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="7cc12-168">Cmdlet har lagts till för att ta bort en kretsanslutning från en befintlig expressroute-krets.</span><span class="sxs-lookup"><span data-stu-id="7cc12-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="7cc12-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7cc12-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="7cc12-170">Cmdlet har lagts till för att hämta en kretsanslutning</span><span class="sxs-lookup"><span data-stu-id="7cc12-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="7cc12-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7cc12-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="7cc12-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cc12-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="7cc12-173">Användning med serverautentisering med genererade certifikat (problem #5998) har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="7cc12-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="7cc12-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7cc12-174">AzureRM.Sql</span></span>
* <span data-ttu-id="7cc12-175">Cmdletar för granskning för att ta bort AuditActions eller AuditActionGroups har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="7cc12-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="7cc12-176">Åtgärdade problem med Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy vid konfigurering av en ny flexibel bevarandeprincip där kommandot misslyckas med ett meddelande om att konfigurering av långsiktig bevarandeprincip med Azure Recovery Service-valv och principen inte längre stöds,</span><span class="sxs-lookup"><span data-stu-id="7cc12-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="7cc12-177">och att en begäran med den nya flexibla bevarandeprincipen ska skickas.</span><span class="sxs-lookup"><span data-stu-id="7cc12-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="7cc12-178">Uppdatera alla Azure Sql Database/ElasticPool Creation/Update-relaterade cmdletar för att använda det nya databas-API:et som stöder SKU-egenskaper för skalnings- och nivårelaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7cc12-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="7cc12-179">Cmdletar har uppdaterats, inklusive:</span><span class="sxs-lookup"><span data-stu-id="7cc12-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="7cc12-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7cc12-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="7cc12-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7cc12-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="7cc12-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7cc12-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="7cc12-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7cc12-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="7cc12-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7cc12-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="7cc12-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7cc12-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="7cc12-186">Uppdatera parametrarna för Get-AzureRmTrafficManagerProfile så att ResourceGroupName-parametern blir obligatorisk när du använder Name-parametern.</span><span class="sxs-lookup"><span data-stu-id="7cc12-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>