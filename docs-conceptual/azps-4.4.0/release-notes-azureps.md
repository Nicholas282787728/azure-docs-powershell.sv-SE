---
title: Viktig information om Azure PowerShell
description: Lär dig mer om alla de senaste uppdateringarna för Azure PowerShell-modulerna.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 88e9c622ef3608b17e6cd8d4ce8c193812a97520
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/14/2020
ms.locfileid: "86382352"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="27ffd-103">Viktig information om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="27ffd-103">Azure PowerShell release notes</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="27ffd-104">4.4.0 – juli 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-104">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-105">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-106">En ny cmdlet, ”Invoke-AzRestMethod”, har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-106">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="27ffd-107">Ett problem åtgärdades som kan orsaka autentiseringsfel i scenarier med fler processer, t.ex. när flera Azure PowerShell-cmdletar körs med ”Start-Job” [#9448]</span><span class="sxs-lookup"><span data-stu-id="27ffd-107">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="27ffd-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27ffd-108">Az.Aks</span></span>
* <span data-ttu-id="27ffd-109">Felet som gjorde att ”Get-AzAks” inte hämtade alla kluster har åtgärdats [#12296]</span><span class="sxs-lookup"><span data-stu-id="27ffd-109">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27ffd-110">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-110">Az.AnalysisServices</span></span>
* <span data-ttu-id="27ffd-111">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="27ffd-111">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-112">Az.Automation</span></span>
* <span data-ttu-id="27ffd-113">Problemet som gjorde att strängar med escape-tecken inte kunde konverteras till JSON-objekt har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-113">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-114">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-114">Az.Compute</span></span>
* <span data-ttu-id="27ffd-115">En varning har lats till som visas när ”New-AzVmss” används utan den senaste avbildningsversionen</span><span class="sxs-lookup"><span data-stu-id="27ffd-115">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-116">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-117">Globala parametrar har lagts till för Data Factory.</span><span class="sxs-lookup"><span data-stu-id="27ffd-117">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27ffd-118">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27ffd-118">Az.EventGrid</span></span>
* <span data-ttu-id="27ffd-119">Modulen har uppdaterats så att API-version 2020-06-01 används.</span><span class="sxs-lookup"><span data-stu-id="27ffd-119">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="27ffd-120">Nya funktioner har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-120">Added new features:</span></span>
    - <span data-ttu-id="27ffd-121">Indatamappning</span><span class="sxs-lookup"><span data-stu-id="27ffd-121">Input mapping</span></span>
    - <span data-ttu-id="27ffd-122">Schema för händelseleverans</span><span class="sxs-lookup"><span data-stu-id="27ffd-122">Event Delivery Schema</span></span>
    - <span data-ttu-id="27ffd-123">Private Link</span><span class="sxs-lookup"><span data-stu-id="27ffd-123">Private Link</span></span>
    - <span data-ttu-id="27ffd-124">Cloud Event V10 Schema</span><span class="sxs-lookup"><span data-stu-id="27ffd-124">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="27ffd-125">Service Bus-ämne som mål</span><span class="sxs-lookup"><span data-stu-id="27ffd-125">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="27ffd-126">Azure-funktion som mål</span><span class="sxs-lookup"><span data-stu-id="27ffd-126">Azure Function As Destination</span></span>
    - <span data-ttu-id="27ffd-127">Webhook-batchbearbetning</span><span class="sxs-lookup"><span data-stu-id="27ffd-127">WebHook Batching</span></span>
    - <span data-ttu-id="27ffd-128">Säker webhook (AAD-stöd)</span><span class="sxs-lookup"><span data-stu-id="27ffd-128">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="27ffd-129">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="27ffd-129">IpFiltering</span></span>
* <span data-ttu-id="27ffd-130">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-130">Updated cmdlets:</span></span>
    - <span data-ttu-id="27ffd-131">”New-AzEventGridSubscription”/”Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="27ffd-131">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="27ffd-132">Lägg till nya valfria parametrar för att ge stöd för webhook-batchbearbetning.</span><span class="sxs-lookup"><span data-stu-id="27ffd-132">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="27ffd-133">Lägg till nya valfria parametrar för att ge stöd för skyddad webhook med AAD.</span><span class="sxs-lookup"><span data-stu-id="27ffd-133">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="27ffd-134">Lägg till ny enum (uppräkning) för EndpointType-parametern för att ge stöd för Azure-funktion och Service Bus-ämne som nya mål.</span><span class="sxs-lookup"><span data-stu-id="27ffd-134">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="27ffd-135">Lägg till ny valfri parameter för leveransschema.</span><span class="sxs-lookup"><span data-stu-id="27ffd-135">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="27ffd-136">”New-AzEventGridTopic”/”Update-AzEventGridTopic” och ”New-AzEventGridDomain”/”Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="27ffd-136">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="27ffd-137">Lägg till nya valfria parametrar för att ge stöd för IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="27ffd-137">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="27ffd-138">”New-AzEventGridTopic”/”New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="27ffd-138">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="27ffd-139">Lägg till nya valfria parametrar för att ge stöd för indatamappning.</span><span class="sxs-lookup"><span data-stu-id="27ffd-139">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27ffd-140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-140">Az.FrontDoor</span></span>
* <span data-ttu-id="27ffd-141">Modulen har uppdaterats så att API 2020-05-01 används</span><span class="sxs-lookup"><span data-stu-id="27ffd-141">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="27ffd-142">Stöd för privat länk har lagts till för Storage-, KeyVault- och Web App Service-resurser</span><span class="sxs-lookup"><span data-stu-id="27ffd-142">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-143">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-144">Stöd för att skapa kluster med ADLSGen1/2-lagring i nationella moln.</span><span class="sxs-lookup"><span data-stu-id="27ffd-144">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-145">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-146">Bugg som orsakade fel med ”Get-AzDiagnosticSetting” när mått eller loggar var null har åtgärdats [#12272]</span><span class="sxs-lookup"><span data-stu-id="27ffd-146">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-147">Az.Network</span></span>
* <span data-ttu-id="27ffd-148">Parameterväxlingen i VWan HubVnet-anslutningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-148">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="27ffd-149">Nya cmdletar har lagts till för platser för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="27ffd-149">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="27ffd-150">”Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="27ffd-150">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="27ffd-151">”New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="27ffd-151">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="27ffd-152">”Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="27ffd-152">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="27ffd-153">”Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="27ffd-153">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="27ffd-154">”New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="27ffd-154">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="27ffd-155">Nya cmdletar har lagts till för virtuella installationer i Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="27ffd-155">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="27ffd-156">”Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="27ffd-156">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="27ffd-157">”New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="27ffd-157">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="27ffd-158">”Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="27ffd-158">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="27ffd-159">”Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="27ffd-159">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="27ffd-160">”Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="27ffd-160">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="27ffd-161">”New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="27ffd-161">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="27ffd-162">Application Gateway har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="27ffd-162">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="27ffd-163">StorageSync har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="27ffd-163">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="27ffd-164">SignalR har introducerats i vanliga cmdletar för Private Link</span><span class="sxs-lookup"><span data-stu-id="27ffd-164">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-166">Projektreferensen till autentisering har tagits bort</span><span class="sxs-lookup"><span data-stu-id="27ffd-166">Removed project reference to Authentication</span></span>
* <span data-ttu-id="27ffd-167">Azure Backup-anpassade cmdletar gör text mer korrekt.</span><span class="sxs-lookup"><span data-stu-id="27ffd-167">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="27ffd-168">Stöd har lagts till som gör att Azure Backup kan hämta MAB-agentjobb med cmdleten ”Get-AzRecoveryServicesBackupJob”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-168">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-169">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-169">Az.Resources</span></span>
* <span data-ttu-id="27ffd-170">”Save-AzResourceGroupDeploymentTemplate” har uppdaterats för att använda SDK:n.</span><span class="sxs-lookup"><span data-stu-id="27ffd-170">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="27ffd-171">Cmdleten ”Unregister-AzResourceProvider” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-171">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-172">Az.Sql</span></span>
* <span data-ttu-id="27ffd-173">Stöd har lagts till för SPN och gästanvändare i cmdleten ”Set-AzSqlInstanceActiveDirectoryAdministrator”</span><span class="sxs-lookup"><span data-stu-id="27ffd-173">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="27ffd-174">En bugg har åtgärdats i cmdletar för dataklassificering.</span><span class="sxs-lookup"><span data-stu-id="27ffd-174">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="27ffd-175">Stöd har lagts till för redundansväxling med Azure SQL Managed Instance: ”Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="27ffd-175">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-176">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-176">Az.Storage</span></span>
* <span data-ttu-id="27ffd-177">Problemet som gjorde att UserAgent inte lades till för vissa cmdletar för dataplanet har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-177">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="27ffd-178">Stöd har lagts till för att skapa/uppdatera Storage-konto med MinimumTlsVersion och AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="27ffd-178">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="27ffd-179">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27ffd-179">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="27ffd-180">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27ffd-180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27ffd-181">Stöd har lagts till för att aktivera/inaktivera versionshantering i Blob Service för ett Storage-konto</span><span class="sxs-lookup"><span data-stu-id="27ffd-181">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="27ffd-182">”Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="27ffd-182">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="27ffd-183">Stöd har lagts till för att visa blobar med blobversioner</span><span class="sxs-lookup"><span data-stu-id="27ffd-183">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="27ffd-184">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="27ffd-184">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="27ffd-185">Stöd har lagts till för att hämta/ta bort enskilda ögonblicksbilder av blobar eller blobversioner</span><span class="sxs-lookup"><span data-stu-id="27ffd-185">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="27ffd-186">”Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="27ffd-186">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="27ffd-187">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="27ffd-187">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="27ffd-188">Stöd har lagts till för pipelines från blobobjekt genererade av Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="27ffd-188">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="27ffd-189">”Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="27ffd-189">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="27ffd-190">”New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="27ffd-190">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="27ffd-191">”Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="27ffd-191">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="27ffd-192">”Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="27ffd-192">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="27ffd-193">”Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="27ffd-193">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27ffd-194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27ffd-194">Az.StorageSync</span></span>
* <span data-ttu-id="27ffd-195">En ny version har lagts till för StorageSync SDK som körs mot ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="27ffd-195">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="27ffd-196">En cmdlet för synkroniseringstjänsten för lagringsuppdatering har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-196">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="27ffd-197">”Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="27ffd-197">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="27ffd-198">IncomingTrafficPolicy och PrivateEndpointConnections har lagts till för StorageSyncService-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-198">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-199">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-199">Az.Websites</span></span>
* <span data-ttu-id="27ffd-200">Stöd har lagts till för att utföra åtgärder för platser som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="27ffd-200">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="27ffd-201">4.3.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-201">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-202">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-202">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-203">Stöd för identifiering av miljöinställning som standard och tillägg av miljön via ”Add-AzEnvironment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-203">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="27ffd-204">Uppdatera förinlästa sammansättningar [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="27ffd-204">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="27ffd-205">Uppdaterad Azure.Core-sammansättning</span><span class="sxs-lookup"><span data-stu-id="27ffd-205">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="27ffd-206">Ett problem har åtgärdats som kan orsaka att ”Connect-AzAccount” misslyckas vid körning av flera trådar [#11201]</span><span class="sxs-lookup"><span data-stu-id="27ffd-206">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="27ffd-207">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27ffd-207">Az.Aks</span></span>
* <span data-ttu-id="27ffd-208">Användning av gamla [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) ersattes med anrop till API:erna [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) och [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="27ffd-208">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27ffd-209">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27ffd-209">Az.Batch</span></span>
* <span data-ttu-id="27ffd-210">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Management.Batch” SDK till och med version 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="27ffd-210">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="27ffd-211">Möjligheten att ange BatchAccount-identiteten har lagts till i cmdleten ”New-AzBatchAccount”</span><span class="sxs-lookup"><span data-stu-id="27ffd-211">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-213">Stöd för att visa kontofunktioner.</span><span class="sxs-lookup"><span data-stu-id="27ffd-213">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="27ffd-214">Stöd för att ändra PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="27ffd-214">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-215">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-215">Az.Compute</span></span>
* <span data-ttu-id="27ffd-216">Parametern SimulateEviction har lagts till i cmdletarna set-AzVM och set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="27ffd-216">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="27ffd-217">”Premium_LRS” har lagts till i argumentslutföraren för parametern StorageAccountType för cmdleten New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="27ffd-217">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="27ffd-218">Understatusar har lagts till i VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="27ffd-218">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="27ffd-219">”Delete” har lagts till i argumentslutföraren för parametern EvictionPolicy för cmdletarna New-AzVM och New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="27ffd-219">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="27ffd-220">Åtgärdat namn för nytt VM-tillägg för SAP</span><span class="sxs-lookup"><span data-stu-id="27ffd-220">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-221">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-221">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-222">ADF .Net SDK har uppdaterats till 4.9.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-222">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27ffd-223">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-223">Az.EventHub</span></span>
* <span data-ttu-id="27ffd-224">Parametrar för hanterad identitet har lagts till i cmdletarna ”New-AzEventHubNamespace” och ”set-AzEventHubNamespace”</span><span class="sxs-lookup"><span data-stu-id="27ffd-224">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="27ffd-225">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="27ffd-225">Az.Functions</span></span>
* <span data-ttu-id="27ffd-226">Stöd har lagts till för att skapa PowerShell 7.0- och Java 11-funktionsappar</span><span class="sxs-lookup"><span data-stu-id="27ffd-226">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-227">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-227">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-228">Stöd för listning av värdar och omstart för specifika värdar i HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="27ffd-228">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27ffd-229">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27ffd-229">Az.HealthcareApis</span></span>
* <span data-ttu-id="27ffd-230">Uppdaterade SDK-versionen till 1.1.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-230">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="27ffd-231">Stöd har lagts till för exportinställningar och hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="27ffd-231">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-232">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-232">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-233">Parameter för inmatningsobjekt har åtgärdats för ”Set-AzActivityLogAlert”</span><span class="sxs-lookup"><span data-stu-id="27ffd-233">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="27ffd-234">Parametern ”InputObject” har åtgärdats för ”Set-AzActionGroup” [#10868]</span><span class="sxs-lookup"><span data-stu-id="27ffd-234">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-235">Az.Network</span></span>
* <span data-ttu-id="27ffd-236">Stöd har lagts till för parametern AddressPrefixType i ”Remove-AzExpressRouteCircuitConnectionConfig”</span><span class="sxs-lookup"><span data-stu-id="27ffd-236">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="27ffd-237">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-237">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="27ffd-238">”New-AzFirewallPolicyDnsSetting”</span><span class="sxs-lookup"><span data-stu-id="27ffd-238">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="27ffd-239">Stöd för mål-FQDN i nätverksregler för brandväggsprincip</span><span class="sxs-lookup"><span data-stu-id="27ffd-239">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="27ffd-240">Stöd har lagts till för åtgärder i serverdelsadresspooler</span><span class="sxs-lookup"><span data-stu-id="27ffd-240">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="27ffd-241">”New-AzLoadBalancerBackendAddressConfig”</span><span class="sxs-lookup"><span data-stu-id="27ffd-241">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="27ffd-242">”New-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="27ffd-242">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="27ffd-243">”Set-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="27ffd-243">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="27ffd-244">”Remove-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="27ffd-244">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="27ffd-245">”Get-AzLoadBalancerBackendAddressPool”</span><span class="sxs-lookup"><span data-stu-id="27ffd-245">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="27ffd-246">Namnvalidering har lagts till för ”New-AzIpGroup”</span><span class="sxs-lookup"><span data-stu-id="27ffd-246">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="27ffd-247">Nya cmdletar har lagts till för Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-247">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="27ffd-248">”New-AzFirewallPolicyThreatIntelWhitelist”</span><span class="sxs-lookup"><span data-stu-id="27ffd-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="27ffd-249">Nedanstående kommandon för funktionen har uppdaterats: Konfiguration/borttagning av anpassade DNS-servrar på VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="27ffd-249">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="27ffd-250">New-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="27ffd-250">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="27ffd-251">Update-AzP2sVpnGateway har uppdaterats: Den valfria parametern ”-CustomDnsServer” har lagts till för att kunder ska kunna ange att deras DNS-servrar ska konfigureras på P2SVpnGateway, som kan användas av punkt-till-plats-klienter.</span><span class="sxs-lookup"><span data-stu-id="27ffd-251">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="27ffd-252">”Update-AzVpnGateway” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="27ffd-252">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="27ffd-253">Den valfria parametern ”-BgpPeeringAddress” har lagts till för att kunder ska kunna ange sina anpassade BGP:er som ska konfigurerar på VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="27ffd-253">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="27ffd-254">Ny cmdlet har lagts till för att stödja återställning av en VirtualHub-resurs routningsstatus:</span><span class="sxs-lookup"><span data-stu-id="27ffd-254">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="27ffd-255">”Reset-AzHubRouter”</span><span class="sxs-lookup"><span data-stu-id="27ffd-255">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="27ffd-256">Nedanstående saker har uppdaterats baserat på den senaste Swagger-ändringen för brandväggspolicyn</span><span class="sxs-lookup"><span data-stu-id="27ffd-256">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="27ffd-257">Namn ändras för RuleGroup, RuleCollectionGroup och RuleType</span><span class="sxs-lookup"><span data-stu-id="27ffd-257">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="27ffd-258">Stöd har lagts till för NAT-regelsamlingar för brandväggsprincip så att flera NAT-regelsamlingar stöds</span><span class="sxs-lookup"><span data-stu-id="27ffd-258">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="27ffd-259">[Icke-bakåtkompatibel ändring] Den obligatoriska parametern ”SourceIpGroup” har lagts till för ”New-AzFirewallPolicyApplicationRule” och ”New-AzFirewallPolicyNetworkRule”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-259">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="27ffd-260">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="27ffd-260">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="27ffd-261">[Icke-bakåtkompatibel ändring] ”New-AzFirewallPolicyApplicationRule” har åtgärdats, parametern ”SourceAddress” är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="27ffd-261">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="27ffd-262">[Icke-bakåtkompatibel ändring] Obligatoriska parametrar har tagits bort: ”TranslatedAddress”, ”TranslatedPort” för ”New-AzFirewallPolicyNatRuleCollection”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-262">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="27ffd-263">Nya cmdletar har lagts till för att stödja PrivateLink på Application Gateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-263">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="27ffd-264">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="27ffd-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27ffd-265">”Get-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="27ffd-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27ffd-266">”New-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="27ffd-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27ffd-267">”Set-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="27ffd-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27ffd-268">”Remove-AzApplicationGatewayPrivateLinkConfiguration”</span><span class="sxs-lookup"><span data-stu-id="27ffd-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27ffd-269">”New-AzApplicationGatewayPrivateLinkIpConfiguration”</span><span class="sxs-lookup"><span data-stu-id="27ffd-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="27ffd-270">Nya cmdletar har lagts till för VirtualHubs underordnade resurs HubRouteTables.</span><span class="sxs-lookup"><span data-stu-id="27ffd-270">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="27ffd-271">”New-AzVHubRoute”</span><span class="sxs-lookup"><span data-stu-id="27ffd-271">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="27ffd-272">”New-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="27ffd-272">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="27ffd-273">”Get-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="27ffd-273">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="27ffd-274">”Update-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="27ffd-274">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="27ffd-275">”Remove-AzVHubRouteTable”</span><span class="sxs-lookup"><span data-stu-id="27ffd-275">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="27ffd-276">Befintliga cmdletar har uppdaterats för att stödja valfri RoutingConfiguration-indataparameter för anpassad routning i VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="27ffd-276">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="27ffd-277">”New-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="27ffd-277">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="27ffd-278">”Set-AzExpressRouteConnection”</span><span class="sxs-lookup"><span data-stu-id="27ffd-278">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="27ffd-279">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="27ffd-279">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27ffd-280">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="27ffd-280">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27ffd-281">”New-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="27ffd-281">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="27ffd-282">”Update-AzVpnConnection”</span><span class="sxs-lookup"><span data-stu-id="27ffd-282">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="27ffd-283">”New-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="27ffd-283">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="27ffd-284">”Update-AzP2sVpnGateway”</span><span class="sxs-lookup"><span data-stu-id="27ffd-284">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-285">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-285">Az.OperationalInsights</span></span>
* <span data-ttu-id="27ffd-286">Fast fel PSWorkspace implementerar inte IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="27ffd-286">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="27ffd-287">”pergb2018” har lagts till i uppsättningen med giltiga värden för parametern ”Sku” i ”Set-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="27ffd-287">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="27ffd-288">Alias ”FunctionParameters” lades till för parametern ”FunctionParameter” till</span><span class="sxs-lookup"><span data-stu-id="27ffd-288">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="27ffd-289">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="27ffd-289">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="27ffd-290">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="27ffd-290">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-291">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-291">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-292">Azure Backup har fått stöd för att hämta MAB-objekt.</span><span class="sxs-lookup"><span data-stu-id="27ffd-292">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="27ffd-293">Azure Site Recovery stöder disktypen ”StandardSSD_LRS”</span><span class="sxs-lookup"><span data-stu-id="27ffd-293">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-294">Az.Resources</span></span>
* <span data-ttu-id="27ffd-295">”UsageLocation”, ”GivenName”, ”Surname”, ”AccountEnabled”, ”MailNickname”, ”Mail” på ”PSADUser” lades till [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="27ffd-295">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="27ffd-296">Problem med att ”-Mail” inte fungerar på ”Get-AzADUser” har åtgärdats [#11981]</span><span class="sxs-lookup"><span data-stu-id="27ffd-296">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="27ffd-297">Parametern ”-ExcludeChangeType” har lagts till i ”Get-AzDeploymentWhatIfResult” och ”Get-AzResourceGroupDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="27ffd-297">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="27ffd-298">Parametern ”-WhatIfExcludeChangeType” har lagts till i ”New-AzDeployment” och ”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-298">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="27ffd-299">Cmdletar för ”Test-Az\*Deployment” har uppdaterats för att visa bättre felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="27ffd-299">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="27ffd-300">Hjälpmeddelandet för parametern ”-Name” i distributionsskapande och What If-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-300">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-301">Az.Sql</span></span>
* <span data-ttu-id="27ffd-302">Stöd för tjänsthuvudnamn har lagts till för administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="27ffd-302">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="27ffd-303">Synkroniseringsproblem i Data Classification-cmdletar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-303">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="27ffd-304">Stöd för att söka efter användare via e-postadress på ”Set-AzSqlServerActiveDirectoryAdministrator” [#12192]</span><span class="sxs-lookup"><span data-stu-id="27ffd-304">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-305">Az.Storage</span></span>
* <span data-ttu-id="27ffd-306">Skapa lagringskonto med RequireInfrastructureEncryption stöds</span><span class="sxs-lookup"><span data-stu-id="27ffd-306">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="27ffd-307">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27ffd-307">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="27ffd-308">Logiken för inläsning av Azure.Core flyttades till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-308">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-309">Az.Websites</span></span>
* <span data-ttu-id="27ffd-310">Skydd för att ta bort skapad webapp om återställningen misslyckades har lagts till i ”Restore-AzDeletedWebApp”</span><span class="sxs-lookup"><span data-stu-id="27ffd-310">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="27ffd-311">”SourceWebApp.Location” har lagts till för ”New-AzWebApp” och ”New-AzWebAppSlot”</span><span class="sxs-lookup"><span data-stu-id="27ffd-311">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="27ffd-312">Fel som förhindrade ändring av containerinställningar i ”Set-AzWebApp” och ”Set-AzWebAppSlot” har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-312">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="27ffd-313">Ett fel för att hämta SiteConfig när -Name inte anges för Get-AzWebApp har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-313">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="27ffd-314">Stöd har lagts till för att skapa ASP för Linux-appar</span><span class="sxs-lookup"><span data-stu-id="27ffd-314">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="27ffd-315">Undantag har lagts till för kloning över resursgrupper</span><span class="sxs-lookup"><span data-stu-id="27ffd-315">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="27ffd-316">4.2.0 – juni 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-316">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-317">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-318">Åtgärdade ett problem som kan få Az att hoppa över loggar i Azure Automation- eller PowerShell-jobb [#11492]</span><span class="sxs-lookup"><span data-stu-id="27ffd-318">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27ffd-319">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-319">Az.AnalysisServices</span></span>
* <span data-ttu-id="27ffd-320">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-320">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-321">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-321">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-322">Uppdaterad sammansättningsversion för cmdletar för tjänsthantering</span><span class="sxs-lookup"><span data-stu-id="27ffd-322">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="27ffd-323">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="27ffd-323">Az.Billing</span></span>
* <span data-ttu-id="27ffd-324">Uppdaterad sammansättningsversion för förbrukningscmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-324">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-325">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-325">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-326">Stöd för PrivateEndpoint- och PublicNetworkAccess-kontroll.</span><span class="sxs-lookup"><span data-stu-id="27ffd-326">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-327">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-327">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-328">Uppdaterad sammansättningsversion för datafabrik V2-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-328">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="27ffd-329">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="27ffd-329">Az.DataShare</span></span>
* <span data-ttu-id="27ffd-330">Allmän tillgänglighet för modulen ”Az.DataShare”</span><span class="sxs-lookup"><span data-stu-id="27ffd-330">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="27ffd-331">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="27ffd-331">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="27ffd-332">Allmän tillgänglighet för modulen ”Az.DesktopVirtualization”</span><span class="sxs-lookup"><span data-stu-id="27ffd-332">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-333">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-333">Az.OperationalInsights</span></span>
* <span data-ttu-id="27ffd-334">Uppgraderad SDK till 0.21.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-334">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="27ffd-335">Lade till valfria parametrar till</span><span class="sxs-lookup"><span data-stu-id="27ffd-335">Added optional parameters to</span></span> 
    - <span data-ttu-id="27ffd-336">”New-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="27ffd-336">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="27ffd-337">”Set-AzOperationalInsightsSavedSearch”</span><span class="sxs-lookup"><span data-stu-id="27ffd-337">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27ffd-338">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-338">Az.PolicyInsights</span></span>
* <span data-ttu-id="27ffd-339">Korrigerade exempel 3 för ”Start-AzPolicyComplianceScan”</span><span class="sxs-lookup"><span data-stu-id="27ffd-339">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="27ffd-340">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="27ffd-340">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="27ffd-341">Uppdaterad sammansättningsversion för PowerBI-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-341">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="27ffd-342">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="27ffd-342">Az.PrivateDns</span></span>
* <span data-ttu-id="27ffd-343">Korrigerade formatering av utförlig utdatasträng för Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-343">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-344">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-345">Azure Site Recovery-stöd för att skapa en återställningsplan för replikering mellan zoner från xml-indata.</span><span class="sxs-lookup"><span data-stu-id="27ffd-345">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="27ffd-346">Uppdaterad sammansättningsversion för cmdletar för SiteRecovery och Backup</span><span class="sxs-lookup"><span data-stu-id="27ffd-346">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-347">Az.Resources</span></span>
* <span data-ttu-id="27ffd-348">Lade till slutparameter för cmdletarna Get-AzDeploymentScriptLog och Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="27ffd-348">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="27ffd-349">Formaterad utdataegenskap så att den kan visas i cmdlet-utdata för Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="27ffd-349">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="27ffd-350">Bytte namn på parametern -DeploymentScriptInputObject till -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="27ffd-350">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="27ffd-351">Åtgärdade saknade fil/målnamn i cmdlet-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="27ffd-351">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="27ffd-352">Uppdaterad sammansättningsversion för cmdletar för resurshanterare och taggar</span><span class="sxs-lookup"><span data-stu-id="27ffd-352">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-353">Az.Sql</span></span>
* <span data-ttu-id="27ffd-354">Lade till UsePrivateLinkConnection till ”New-AzSqlSyncGroup”, ”Update-AzSqlSyncGroup”, ”New-AzSqlSyncMember” och ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="27ffd-354">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="27ffd-355">Lade till SyncMemberAzureDatabaseResourceId till ”New-AzSqlSyncMember” and ”Update-AzSqlSyncMember”</span><span class="sxs-lookup"><span data-stu-id="27ffd-355">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="27ffd-356">Lade till stöd för att söka efter gästanvändare för att ange administratörs-cmdlet för SQL Server Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="27ffd-356">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-357">Az.Storage</span></span>
* <span data-ttu-id="27ffd-358">Uppdaterad sammansättningsversion för dataplan-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-358">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="27ffd-359">4.1.0 – maj 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-359">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="27ffd-360">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="27ffd-360">Highlights since the last release</span></span>
* <span data-ttu-id="27ffd-361">PowerShell-versioner som stöds: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="27ffd-361">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="27ffd-362">Allmän tillgänglighet för Az.Functions</span><span class="sxs-lookup"><span data-stu-id="27ffd-362">General availability of Az.Functions</span></span> 
* <span data-ttu-id="27ffd-363">Nya stora uppdateringar har gjorts för Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources och Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-363">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-364">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-365">”Add-AzEnvironment” och ”Set-AzEnvironment” har uppdaterats med stöd för parametrarna ”AzureSynapseAnalyticsEndpointResourceId” och ”AzureSynapseAnalyticsEndpointSuffix”</span><span class="sxs-lookup"><span data-stu-id="27ffd-365">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="27ffd-366">Azure.Core-relaterade sammansättningar har lagts till i Az.Accounts; PowerShell-plattformar som stöds är Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="27ffd-366">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="27ffd-367">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27ffd-367">Az.Aks</span></span>
* <span data-ttu-id="27ffd-368">API-versionen har uppgraderats till 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="27ffd-368">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="27ffd-369">Stöds för att skapa AKS med hjälp av Windows-container</span><span class="sxs-lookup"><span data-stu-id="27ffd-369">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="27ffd-370">Nya cmdletar är tillgängliga: ”New-AzAksNodePool”, ”Update-AzAksNodePool”, ”Remove-AzAksNodePool”,        ”Get-AzAksNodePool”, ”Install-AzAksKubectl”, ”Get-AzAksVersion”</span><span class="sxs-lookup"><span data-stu-id="27ffd-370">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-371">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-372">Parametrarna ”New-AzApiManagement” och ”Set-AzApiManagement”: [-AssignIdentity] har bytt namn till [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="27ffd-372">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="27ffd-373">”New-AzApiManagement” och ”Set-AzApiManagement”: En ny parameter har lagts till: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="27ffd-373">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="27ffd-374">”Get-AzApiManagementProperty” har bytt namn till ”Get-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-374">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27ffd-375">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="27ffd-375">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="27ffd-376">”New-AzApiManagementProperty” har bytt namn till ”New-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-376">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27ffd-377">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="27ffd-377">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="27ffd-378">”Set-AzApiManagementProperty” har bytt namn till ”Set-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-378">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27ffd-379">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="27ffd-379">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="27ffd-380">”Remove-AzApiManagementProperty” har bytt namn till ”Remove-AzApiManagementNamedValue”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-380">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27ffd-381">PropertyId-parametern har bytt namn till NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="27ffd-381">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="27ffd-382">Den nya cmdleten Get-AzApiManagementAuthorizationServerClientSecret gör att ”Get-AzApiManagementAuthorizationServer” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="27ffd-382">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="27ffd-383">Den nya cmdleten ”Get-AzApiManagementNamedValueSecretValue” gör att ”Get-AzApiManagementNamedValue” inte returnerar värdet för en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-383">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="27ffd-384">Den nya cmdleten ”Get-AzApiManagementOpenIdConnectProviderClientSecret” gör att ”Get-AzApiManagementOpenIdConnectProvider” inte längre returnerar klienthemligheter.</span><span class="sxs-lookup"><span data-stu-id="27ffd-384">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="27ffd-385">Den nya cmdleten ”Get-AzApiManagementSubscriptionKey” gör att ”Get-AzApiManagementSubscription” inte längre returnerar prenumerationsnycklar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-385">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="27ffd-386">Den nya cmdleten ”Get-AzApiManagementTenantAccessSecret” gör att ”Get-AzApiManagementTenantAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-386">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="27ffd-387">Den nya cmdleten ”Get-AzApiManagementTenantGitAccessSecret” gör att ”Get-AzApiManagementTenantGitAccess” inte längre returnerar nycklar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-387">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="27ffd-388">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-388">Az.ApplicationInsights</span></span>
* <span data-ttu-id="27ffd-389">Tillagda parametrar: ”RetentionInDays” ”PublicNetworkAccessForIngestion” ”PublicNetworkAccessForQuery” för ”New-AzApplicationInsights”</span><span class="sxs-lookup"><span data-stu-id="27ffd-389">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="27ffd-390">Cmdleten ”Update-AzApplicationInsights” har skapats</span><span class="sxs-lookup"><span data-stu-id="27ffd-390">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="27ffd-391">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-391">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27ffd-392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27ffd-392">Az.Batch</span></span>
* <span data-ttu-id="27ffd-393">Az.Batch har uppdaterats att använda ”Microsoft.Azure.Batch” SDK version 13.0.0 och ”Microsoft.Azure.Management.Batch” SDK version 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="27ffd-393">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="27ffd-394">Nu kan du välja vilken typ av certifikat du lägger till genom att använda den nya parametern ”-CertificateKind” med ”New-AzBatchCertificate”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-394">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="27ffd-395">Egenskapen ”ApplicationPackages” har tagits bort från ”PSApplication”, som tidigare alltid var ''.</span><span class="sxs-lookup"><span data-stu-id="27ffd-395">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="27ffd-396">Specifika paket i ett program kan nu hämtas med hjälp av ”Get-AzBatchApplicationPackage”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-396">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="27ffd-397">Ett exempel: ”Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-397">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="27ffd-398">Nu när du skapar en pool med hjälp av ”New-AzBatchPool” kan egenskapen ”VirtualMachineImageId” för ”PSImageReference” endast referera till en Shared Image Gallery-avbildning.</span><span class="sxs-lookup"><span data-stu-id="27ffd-398">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="27ffd-399">När du skapar en pool med hjälp av ”New-AzBatchPool” kan poolen etableras utan en offentlig IP-adress med hjälp av den nya egenskapen ”PublicIPAddressConfiguration” för ”PSNetworkConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-399">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="27ffd-400">Egenskapen ”PublicIPs” för ”PSNetworkConfiguration” har också flyttats till ”PSPublicIPAddressConfiguration”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-400">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="27ffd-401">Den här egenskapen kan bara anges om ”IPAddressProvisioningType” är ”UserManaged”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-401">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-402">Az.Compute</span></span>
* <span data-ttu-id="27ffd-403">Parametern HostId har lagts till för cmdleten ”Update-AzVM”t</span><span class="sxs-lookup"><span data-stu-id="27ffd-403">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="27ffd-404">Hjälpdokumenten har uppdaterats för cmdletarna ”New-AzVMConfig”, ”New-AzVmssConfig”, ”Update-AzVmss”, ”Set-AzVMOperatingSystem” och ”Set-AzVmssOsProfile”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-404">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="27ffd-405">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="27ffd-405">Breaking changes</span></span>
    - <span data-ttu-id="27ffd-406">Parametern FilterExpression tas bort från cmdleten ”Get-AzVMImage”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-406">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="27ffd-407">Parametern AssignIdentity tas bort från cmdletarna ”New-AzVmssConfig”, ”New-AzVMConfig” och ”Update-AzVM”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-407">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="27ffd-408">AutomaticRepairMaxInstanceRepairsPercent tas bort från cmdletarna ”New-AzVmssConfig” och ”Update-AzVmss”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-408">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="27ffd-409">Egenskaperna AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus och VirtualMachineScaleSetsColocationStatus tas bort från ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="27ffd-409">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="27ffd-410">Egenskapen MaxInstanceRepairsPercent tas bort från AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="27ffd-410">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="27ffd-411">Typerna AvailabilitySets, VirtualMachines och VirtualMachineScaleSets ändras från IList<SubResource> till IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="27ffd-411">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="27ffd-412">Beskrivningen för cmdleten ”Get-AzVM” har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-412">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-413">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-414">CRUD-stöd för egenskaper för dataflödeskörning  i hanterad IR.</span><span class="sxs-lookup"><span data-stu-id="27ffd-414">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27ffd-415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-415">Az.FrontDoor</span></span>
* <span data-ttu-id="27ffd-416">Nya cmdletar har lagts till för att skapa, uppdatera, hämta och ta bort (CRUD) Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="27ffd-416">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="27ffd-417">Hjälp-cmdletar har lagts till för konstruktion av Front Door-regelmotorobjekt</span><span class="sxs-lookup"><span data-stu-id="27ffd-417">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="27ffd-418">Regelmotorreferens har lagts till för Front Door-hanteringsregelobjekt.</span><span class="sxs-lookup"><span data-stu-id="27ffd-418">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="27ffd-419">Parametrar för Private Link har lagts till för Front Door-serverdelsobjekt</span><span class="sxs-lookup"><span data-stu-id="27ffd-419">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="27ffd-420">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="27ffd-420">Az.Functions</span></span>
* <span data-ttu-id="27ffd-421">Allmän tillgänglighet för ”Az.Functions”-modulen</span><span class="sxs-lookup"><span data-stu-id="27ffd-421">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-422">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-422">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-423">Stöd för diskkryptering med kundhanterad nyckel.</span><span class="sxs-lookup"><span data-stu-id="27ffd-423">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27ffd-424">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27ffd-424">Az.HealthcareApis</span></span>
* <span data-ttu-id="27ffd-425">Åtkomstprinciper använder inte längre det aktiva huvudkontot som standard</span><span class="sxs-lookup"><span data-stu-id="27ffd-425">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-426">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-426">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-427">En cmdlet har lagts till som anropar en fråga i en IoT-hubb för att hämta information med ett SQL-liknande språk.</span><span class="sxs-lookup"><span data-stu-id="27ffd-427">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="27ffd-428">Problemet som gjorde att ”Add-AzIotHubDevice” inte skapade en Edge-aktiverad enhet utan underordnade enheter har åtgärdats [#11597]</span><span class="sxs-lookup"><span data-stu-id="27ffd-428">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="27ffd-429">En cmdlet har lagts till för att generera SAS-token för en Iot-hubb, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="27ffd-429">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="27ffd-430">En cmdlet har lagts till för att anropa en måttfråga om konfiguration.</span><span class="sxs-lookup"><span data-stu-id="27ffd-430">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="27ffd-431">Hantera automatisk distribution av IoT Edge i stor skala.</span><span class="sxs-lookup"><span data-stu-id="27ffd-431">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="27ffd-432">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="27ffd-432">New cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-433">”Add-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-433">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="27ffd-434">”Get-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-434">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="27ffd-435">”Remove-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-435">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="27ffd-436">”Set-AzIotHubDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-436">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="27ffd-437">En cmdlet har lagts till för att anropa en måttfråga om IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="27ffd-437">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="27ffd-438">En cmdlet har lagts till för att tillämpa konfigurationsinnehåll på den angivna gränsenheten.</span><span class="sxs-lookup"><span data-stu-id="27ffd-438">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-439">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-440">Två alias har tagits bort: ”New-AzKeyVaultCertificateAdministratorDetails” och ”New-AzKeyVaultCertificateOrganizationDetails”</span><span class="sxs-lookup"><span data-stu-id="27ffd-440">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="27ffd-441">Nu är mjuk borttagning aktiverat som standard när ett nyckelvalv skapas</span><span class="sxs-lookup"><span data-stu-id="27ffd-441">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="27ffd-442">Nätverksregler kan ställas in för att styra åtkomsten från särskilda nätverksplatser när du skapar ett nyckelvalv</span><span class="sxs-lookup"><span data-stu-id="27ffd-442">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="27ffd-443">Stöd för BYOK (Bring Your Own Key) har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-443">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="27ffd-444">”Add-AzKeyVaultKey” stöder generering av en KeyExchange-nyckel</span><span class="sxs-lookup"><span data-stu-id="27ffd-444">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="27ffd-445">”Get-AzKeyVaultKey” stöder nedladdning av en offentlig nyckel i PEM-format</span><span class="sxs-lookup"><span data-stu-id="27ffd-445">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="27ffd-446">”KeyOps”-delen av hjälpdokumentet för ”Add-AzKeyVaultKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="27ffd-446">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-447">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-448">Bugg för ”Set-AzDiagnosticSettings” har åtgärdats; kvarhållningsprincipen tillämpas inte på alla kategorier [#11589]</span><span class="sxs-lookup"><span data-stu-id="27ffd-448">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="27ffd-449">Stöd för WebTest-tillgänglighetskriterier för måttavisering V2</span><span class="sxs-lookup"><span data-stu-id="27ffd-449">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="27ffd-450">”New-AzMetricAlertRuleV2Criteria”: ett alternativ för att skapa tillgänglighetskriterier för webbtest har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-450">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="27ffd-451">”Add-AzMetricAlertRuleV2”: stöd för de nya tillgänglighetskriterierna för webbtest</span><span class="sxs-lookup"><span data-stu-id="27ffd-451">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="27ffd-452">Redundant definition har tagits bort för RetentionPolicy i PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="27ffd-452">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="27ffd-453">Redundanta egenskaper som definierats i PSEventData har tagits bort [#11353]</span><span class="sxs-lookup"><span data-stu-id="27ffd-453">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="27ffd-454">”Get-AzLog” har bytt namn till ”Get-AzActivityLog”</span><span class="sxs-lookup"><span data-stu-id="27ffd-454">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-455">Az.Network</span></span>
* <span data-ttu-id="27ffd-456">Attribut för icke-bakåtkompatibel ändring har lagts till för att meddela att standardbeteendet för zoner kommer att ändras</span><span class="sxs-lookup"><span data-stu-id="27ffd-456">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="27ffd-457">”New-AzPublicIpAddress”</span><span class="sxs-lookup"><span data-stu-id="27ffd-457">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="27ffd-458">”New-AzPublicIpPrefix”</span><span class="sxs-lookup"><span data-stu-id="27ffd-458">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="27ffd-459">”New-AzLoadBalancerFrontendIpConfig”</span><span class="sxs-lookup"><span data-stu-id="27ffd-459">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="27ffd-460">Stöd har lagts till för en ny resurs på den översta nivån, SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="27ffd-460">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="27ffd-461">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-461">New cmdlets added:</span></span>
        - <span data-ttu-id="27ffd-462">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="27ffd-462">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="27ffd-463">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="27ffd-463">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="27ffd-464">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="27ffd-464">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="27ffd-465">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="27ffd-465">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="27ffd-466">”RequiredZoneNames” har lagts till för ”PSPrivateLinkResource” och ”GroupId” för ”PSPrivateEndpointConnection”</span><span class="sxs-lookup"><span data-stu-id="27ffd-466">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="27ffd-467">Fel parametertyp för SuccessThresholdRoundTripTimeMs-parametern för New-AzNetworkWatcherConnectionMonitorTestConfigurationObject har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-467">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="27ffd-468">VirtualWan-cmdletar har uppdaterats för att ange AllowVnetToVnetTraffic-argumentets standardvärde till True.</span><span class="sxs-lookup"><span data-stu-id="27ffd-468">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="27ffd-469">”New-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="27ffd-469">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="27ffd-470">”Update-AzVirtualWan”</span><span class="sxs-lookup"><span data-stu-id="27ffd-470">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="27ffd-471">Nya cmdletar har lagts till för att stödja DNS-zongrupp för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="27ffd-471">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="27ffd-472">”New-AzPrivateDnsZoneConfig”</span><span class="sxs-lookup"><span data-stu-id="27ffd-472">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="27ffd-473">”Get-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="27ffd-473">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="27ffd-474">”New-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="27ffd-474">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="27ffd-475">”Set-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="27ffd-475">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="27ffd-476">”Remove-AzPrivateDnsZoneGroup”</span><span class="sxs-lookup"><span data-stu-id="27ffd-476">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="27ffd-477">Parametrarna ”DNSEnableProxy”, ”DNSRequireProxyForNetworkRules” och ”DNSServers” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="27ffd-477">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="27ffd-478">Parametrarna ”EnableDnsProxy”, ”DnsProxyNotRequiredForNetworkRule” och ”DnsServer” har lagts till för ”AzureFirewall”</span><span class="sxs-lookup"><span data-stu-id="27ffd-478">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="27ffd-479">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27ffd-479">Updated cmdlet:</span></span>
        - <span data-ttu-id="27ffd-480">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="27ffd-480">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-481">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-481">Az.OperationalInsights</span></span>
* <span data-ttu-id="27ffd-482">Äldre kod har uppdaterats för att tillämpa ny genererad SDK</span><span class="sxs-lookup"><span data-stu-id="27ffd-482">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="27ffd-483">Cmdletar har tagits bort på grund av föråldrade API:er</span><span class="sxs-lookup"><span data-stu-id="27ffd-483">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="27ffd-484">”Get-AzOperationalInsightsSavedSearchResult” (alias ”Get-AzOperationalInsightsSavedSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="27ffd-484">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="27ffd-485">”Get-AzOperationalInsightsSearchResult” (alias ”Get-AzOperationalInsightsSearchResults”)</span><span class="sxs-lookup"><span data-stu-id="27ffd-485">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="27ffd-486">”Get-AzOperationalInsightsLinkTarget” (alias ”Get-AzOperationalInsightsLinkTargets”)</span><span class="sxs-lookup"><span data-stu-id="27ffd-486">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="27ffd-487">Parametrar har lagts till för ”Set-AzOperationalInsightsWorkspace” och ”New-AzOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="27ffd-487">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="27ffd-488">Cmdletar har skapats för länkat lagringskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-488">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="27ffd-489">Cmdletar har skapats för kluster och länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="27ffd-489">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-491">Azure Site Recovery: Stöd har lagts till för att skydda VM-närhetsplaceringsgrupper för Azure till Azure-provider.</span><span class="sxs-lookup"><span data-stu-id="27ffd-491">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="27ffd-492">Azure Site Recovery: Stöd har lagts till för replikering mellan zoner.</span><span class="sxs-lookup"><span data-stu-id="27ffd-492">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="27ffd-493">Azure Backup: Stöd har lagts till för långsiktig kvarhållning för Azure FileShare-återställningspunkter.</span><span class="sxs-lookup"><span data-stu-id="27ffd-493">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="27ffd-494">Azure Backup: Egenskaper för diskexkludering har lagts till för cmdlet-utdata från ”Get-AzRecoveryServicesBackupItem”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-494">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="27ffd-495">En privat slutpunkt har lagts till för filen med valvets autentiseringsuppgifter för Site Recovery-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="27ffd-495">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-496">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-496">Az.Resources</span></span>
* <span data-ttu-id="27ffd-497">En varning har lagts till om visningsfördröjning när en ny rolldefinition skapas</span><span class="sxs-lookup"><span data-stu-id="27ffd-497">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="27ffd-498">Princip-cmdletar har ändrats för utmatning av starkt typifierade objekt</span><span class="sxs-lookup"><span data-stu-id="27ffd-498">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="27ffd-499">Parametern ”-TenantLevel” har tagits bort för användning med ”Get-AzResourceLock” [#11335]</span><span class="sxs-lookup"><span data-stu-id="27ffd-499">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="27ffd-500">”Remove-AzResourceGroup -Id ResourceId” har åtgärdats [#9882]</span><span class="sxs-lookup"><span data-stu-id="27ffd-500">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="27ffd-501">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i omfånget för resursgrupper: ”Get-AzDeploymentResourceGroupWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="27ffd-501">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="27ffd-502">En ny cmdlet har lagts till för att hämta What-If-resultat för ARM-mallar i prenumerationsomfånget: ”Get-AzDeploymentWhatIfResult”</span><span class="sxs-lookup"><span data-stu-id="27ffd-502">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="27ffd-503">Alias: ”Get-AzSubscriptionDeploymentWhatIf”</span><span class="sxs-lookup"><span data-stu-id="27ffd-503">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="27ffd-504">Parametrarna ”-WhatIf” och ”-Confirm” har åsidosatts för ”New-AzDeployment” och ”New-AzResourceGroupDeployment” för att använda What-If-resultat för ARM-mallar</span><span class="sxs-lookup"><span data-stu-id="27ffd-504">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="27ffd-505">Ett utfasningsmeddelande har lagts till för parametern ”ApiVersion” i distributions-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-505">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="27ffd-506">En funktion har lagts till för att visa förbättrade felmeddelanden för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="27ffd-506">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="27ffd-507">CorrelationId-loggning har lagts till för distributionsfel</span><span class="sxs-lookup"><span data-stu-id="27ffd-507">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="27ffd-508">Egenskapen ”error” har lagts till i utdata från distributionsskript</span><span class="sxs-lookup"><span data-stu-id="27ffd-508">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="27ffd-509">Nuget Microsoft.Azure.Management.ResourceManager har uppdaterats till ”3.7.1-preview”</span><span class="sxs-lookup"><span data-stu-id="27ffd-509">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="27ffd-510">Specifika testfall har tagits bort då egenskapen Error i DeploymentValidateResult har ändrats till lässkyddad från nuget 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="27ffd-510">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="27ffd-511">GenericResourceExpanded har flyttats från SDK ResourceManager 3.7.1-preview</span><span class="sxs-lookup"><span data-stu-id="27ffd-511">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="27ffd-512">Stöd för taggar har lagts till för alla Get-cmdletar för distribution, samt</span><span class="sxs-lookup"><span data-stu-id="27ffd-512">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="27ffd-513">”New-AzDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-513">'New-AzDeployment'</span></span>
    - <span data-ttu-id="27ffd-514">”New-AzManagementGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-514">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="27ffd-515">”New-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-515">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="27ffd-516">”New-AzTenantDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-516">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27ffd-517">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-517">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-518">En bugg har åtgärdats som gjorde att --SecretIdentifier fick fel tumavtryck för certifikat när ett certifikat lades till</span><span class="sxs-lookup"><span data-stu-id="27ffd-518">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-519">Az.Sql</span></span>
* <span data-ttu-id="27ffd-520">Förbättrade prestanda för:</span><span class="sxs-lookup"><span data-stu-id="27ffd-520">Enhance performance of:</span></span>
    - <span data-ttu-id="27ffd-521">”Set-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="27ffd-521">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27ffd-522">”Set-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="27ffd-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27ffd-523">”Remove-AzSqlDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="27ffd-523">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27ffd-524">”Remove-AzSqlInstanceDatabaseSensitivityClassification”</span><span class="sxs-lookup"><span data-stu-id="27ffd-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27ffd-525">”Enable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="27ffd-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="27ffd-526">”Enable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="27ffd-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="27ffd-527">”Disable-AzSqlDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="27ffd-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="27ffd-528">”Disable-AzSqlInstanceDatabaseSensitivityRecommendation”</span><span class="sxs-lookup"><span data-stu-id="27ffd-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="27ffd-529">Validering på klientsidan har tagits bort för parametern ”RetentionDays” från cmdleten ”Set-AzSqlDatabaseBackupShortTermRetentionPolicy”</span><span class="sxs-lookup"><span data-stu-id="27ffd-529">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="27ffd-530">Granskning av ett lagringskonto i Vnet; en bugg har åtgärdats som orsakade fel när en Storage Blob Data-deltagarroll skapades.</span><span class="sxs-lookup"><span data-stu-id="27ffd-530">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-531">Az.Storage</span></span>
* <span data-ttu-id="27ffd-532">”-AsJob” har lagts till för att hämta/lista konto med cmdleten ”Get-AzStorageAccount”</span><span class="sxs-lookup"><span data-stu-id="27ffd-532">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="27ffd-533">Gör KeyVersion valfri när lagringskontot uppdateras med KeyvaultEncryption, för att ge stöd för automatisk nyckelrotation</span><span class="sxs-lookup"><span data-stu-id="27ffd-533">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="27ffd-534">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27ffd-534">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27ffd-535">Problemet med borttagning av Azure-filkatalog i pipeline har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-535">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="27ffd-536">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="27ffd-536">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="27ffd-537">Åtgärdat [#9880]: Definitionen av DefaultAction-värdet för NetWorkRule har ändrats för konsekvens med Swagger.</span><span class="sxs-lookup"><span data-stu-id="27ffd-537">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="27ffd-538">”Update-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="27ffd-538">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="27ffd-539">”Get-AzStorageAccountNetworkRuleSet”</span><span class="sxs-lookup"><span data-stu-id="27ffd-539">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="27ffd-540">Åtgärdat [#11624]: Hoppa över dubblettregler när NetworkRules läggs till, för att undvika serverfel</span><span class="sxs-lookup"><span data-stu-id="27ffd-540">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="27ffd-541">”Add-AzStorageAccountNetworkRule”</span><span class="sxs-lookup"><span data-stu-id="27ffd-541">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="27ffd-542">Microsoft.Azure.Cosmos.Table SDK har uppgraderats till 1.0.7</span><span class="sxs-lookup"><span data-stu-id="27ffd-542">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="27ffd-543">Ett varningsmeddelande har lagts till för att påminna användaren om att lista igen med ContinuationToken när endast delobjekt returneras i listan med DataLake Gen2-objekt,</span><span class="sxs-lookup"><span data-stu-id="27ffd-543">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="27ffd-544">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="27ffd-544">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="27ffd-545">Stöd för att skapa eller uppdatera lagringskonto med Azure Files Active Directory Domain Service-autentisering</span><span class="sxs-lookup"><span data-stu-id="27ffd-545">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="27ffd-546">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27ffd-546">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="27ffd-547">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27ffd-547">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27ffd-548">Stöd för nya eller listade Kerberos-nycklar för lagringskontot</span><span class="sxs-lookup"><span data-stu-id="27ffd-548">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="27ffd-549">”New-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="27ffd-549">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="27ffd-550">”Get-AzStorageAccountKey”</span><span class="sxs-lookup"><span data-stu-id="27ffd-550">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="27ffd-551">Stöd för redundans med lagringskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-551">Supported failover Storage account</span></span>
    - <span data-ttu-id="27ffd-552">”Invoke-AzStorageAccountFailover”</span><span class="sxs-lookup"><span data-stu-id="27ffd-552">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="27ffd-553">Hjälpen för ”Get-AzStorageBlobCopyState” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="27ffd-553">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="27ffd-554">Hjälpen för ”Get-AzStorageFileCopyState” och ”Start-AzStorageBlobCopy” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="27ffd-554">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="27ffd-555">Lagringsklientbibliotek v12 har integrerats med Queue- och File-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-555">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="27ffd-556">Utdatatypen har ändrats från CloudFile till AzureStorageFile; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="27ffd-556">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="27ffd-557">”Get-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="27ffd-557">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="27ffd-558">”Remove-AzStorageFile”</span><span class="sxs-lookup"><span data-stu-id="27ffd-558">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="27ffd-559">”Get-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="27ffd-559">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="27ffd-560">”Set-AzStorageFileContent”</span><span class="sxs-lookup"><span data-stu-id="27ffd-560">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="27ffd-561">”Start-AzStorageFileCopy”</span><span class="sxs-lookup"><span data-stu-id="27ffd-561">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="27ffd-562">Utdatatypen har ändrats från CloudFileDirectory till AzureStorageFileDirectory; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="27ffd-562">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="27ffd-563">”New-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="27ffd-563">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="27ffd-564">”Remove-AzStorageDirectory”</span><span class="sxs-lookup"><span data-stu-id="27ffd-564">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="27ffd-565">Utdatatypen har ändrats från CloudFileShare till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="27ffd-565">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="27ffd-566">”Get-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="27ffd-566">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="27ffd-567">”New-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="27ffd-567">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="27ffd-568">”Remove-AzStorageShare”</span><span class="sxs-lookup"><span data-stu-id="27ffd-568">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="27ffd-569">Utdatatypen har ändrats från FileShareProperties till AzureStorageFileShare; ursprungliga utdata blir en underordnad egenskap i den nya utmatningen</span><span class="sxs-lookup"><span data-stu-id="27ffd-569">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="27ffd-570">”Set-AzStorageShareQuota”</span><span class="sxs-lookup"><span data-stu-id="27ffd-570">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="27ffd-571">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="27ffd-571">Az.TrafficManager</span></span>
* <span data-ttu-id="27ffd-572">Felaktigt profilnamn har åtgärdats i utförliga utdata för ”DisableAzureTrafficManagerEndpoint”</span><span class="sxs-lookup"><span data-stu-id="27ffd-572">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-573">Az.Websites</span></span>
* <span data-ttu-id="27ffd-574">Stavfel har åtgärdats i hjälpen för ”Update-AzWebAppAccessRestrictionConfig”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-574">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="27ffd-575">3.8.0 – April 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-575">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="27ffd-576">Höjdpunkter sedan den senaste uppdateringen</span><span class="sxs-lookup"><span data-stu-id="27ffd-576">Highlights since the last release</span></span>
* <span data-ttu-id="27ffd-577">PowerShell-versioner som Az.Storage stöder: Windows PowerShell 5.1, PowerShell Core 6.2.4+ och PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="27ffd-577">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-578">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-579">Uppdaterade URL:en för Azure PowerShell-enkäten i ”Resolve-AzError” [#11507]</span><span class="sxs-lookup"><span data-stu-id="27ffd-579">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-580">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-581">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="27ffd-581">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="27ffd-582">"Set-AzApiManagementGroup" Uppdaterad dokumentation för att ange GroupId-parametern</span><span class="sxs-lookup"><span data-stu-id="27ffd-582">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27ffd-583">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27ffd-583">Az.Cdn</span></span>
* <span data-ttu-id="27ffd-584">Fast ChinaCDN-relaterad prissättning för SKU-visning</span><span class="sxs-lookup"><span data-stu-id="27ffd-584">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-585">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-585">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-586">Identitet som stöds, kryptering, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="27ffd-586">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-587">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-587">Az.Compute</span></span>
* <span data-ttu-id="27ffd-588">Cmdleten ”Set-AzVmssOrchestrationServiceState” har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-588">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="27ffd-589">”Get-AzVmss” med -InstanceView visar OrchestrationService-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="27ffd-589">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-590">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-590">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-591">Hantera den dubbla konfigurationen för IoT-enheter, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="27ffd-591">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-592">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="27ffd-592">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="27ffd-593">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="27ffd-593">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="27ffd-594">En cmdlet har lagts till för att anropa direkt metod på en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27ffd-594">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="27ffd-595">Hantera dubbel konfiguration för IoT-enhetsmodul, nya cmdletar är:</span><span class="sxs-lookup"><span data-stu-id="27ffd-595">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-596">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="27ffd-596">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="27ffd-597">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="27ffd-597">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="27ffd-598">Hantera IoT-automatisk konfiguration av enhetshantering i stor skala.</span><span class="sxs-lookup"><span data-stu-id="27ffd-598">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="27ffd-599">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="27ffd-599">New cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-600">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27ffd-600">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="27ffd-601">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27ffd-601">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="27ffd-602">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27ffd-602">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="27ffd-603">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27ffd-603">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="27ffd-604">En cmdlet har lagts till för att anropa en edge-modulmetod i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27ffd-604">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-605">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-605">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-606">Har lagt till en ny cmdlet, "Update-AzKeyVault", som kan aktivera mjuk borttagning och rensning av skydd i ett valv</span><span class="sxs-lookup"><span data-stu-id="27ffd-606">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="27ffd-607">Har lagt till stöd i Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="27ffd-607">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="27ffd-608">Åtgärdat fel i exemplen i 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="27ffd-608">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="27ffd-609">Har lagt till stöd för privat slutpunkt</span><span class="sxs-lookup"><span data-stu-id="27ffd-609">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="27ffd-610">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="27ffd-610">Az.Maintenance</span></span>
* <span data-ttu-id="27ffd-611">Publicerar slutversion av underhålls-cmdletar för GA</span><span class="sxs-lookup"><span data-stu-id="27ffd-611">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-612">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-612">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-613">Har lagt till cmdletar för privat länkomfång</span><span class="sxs-lookup"><span data-stu-id="27ffd-613">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="27ffd-614">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="27ffd-614">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27ffd-615">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="27ffd-615">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27ffd-616">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="27ffd-616">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27ffd-617">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="27ffd-617">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27ffd-618">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="27ffd-618">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="27ffd-619">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="27ffd-619">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="27ffd-620">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="27ffd-620">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-621">Az.Network</span></span>
* <span data-ttu-id="27ffd-622">Uppdaterade cmdletar för att aktivera anslutning på privat IP för Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="27ffd-622">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="27ffd-623">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="27ffd-623">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="27ffd-624">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="27ffd-624">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="27ffd-625">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="27ffd-625">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="27ffd-626">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="27ffd-626">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="27ffd-627">Uppdaterade cmdletar för att aktivera FQDN-baserade LocalNetworkGateways och VpnSites</span><span class="sxs-lookup"><span data-stu-id="27ffd-627">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="27ffd-628">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="27ffd-628">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="27ffd-629">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="27ffd-629">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="27ffd-630">Stöd har lagts till för IPv6-adresstypen i ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="27ffd-630">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="27ffd-631">Lade till 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="27ffd-631">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="27ffd-632">tillåter inställning av alla befintliga egenskaper inklusive IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="27ffd-632">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="27ffd-633">Uppdaterade 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="27ffd-633">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="27ffd-634">Lade till en ytterligare valfri parameter, AddressPrefixType, för att specificera adresstypen för adressprefix</span><span class="sxs-lookup"><span data-stu-id="27ffd-634">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="27ffd-635">Uppdaterade cmdletar för att aktivera inställningen för DPD-timeout på Virtual Network Gateway-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-635">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="27ffd-636">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-636">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="27ffd-637">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-637">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27ffd-638">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-638">Az.PolicyInsights</span></span>
* <span data-ttu-id="27ffd-639">Cmdleten "Start-AzPolicyComplianceScan" har lagts till för att utlösa genomsökningar av principefterlevnad</span><span class="sxs-lookup"><span data-stu-id="27ffd-639">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="27ffd-640">Principdefinition, uppsättningsdefinition och tilldelningsversioner har lagts till i "Get-AzPolicyState"-utdata</span><span class="sxs-lookup"><span data-stu-id="27ffd-640">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27ffd-641">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-641">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-642">Förbättrad kodformatering och användbarhet för "New-AzServiceFabricCluster"-exempel</span><span class="sxs-lookup"><span data-stu-id="27ffd-642">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-643">Az.Sql</span></span>
* <span data-ttu-id="27ffd-644">Lade till cmdletarna "Get-AzSqlInstanceOperation" och "Stop-AzSqlInstanceOperation"</span><span class="sxs-lookup"><span data-stu-id="27ffd-644">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="27ffd-645">Stöd för granskning för ett lagringskonto i VNet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-645">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-646">Az.Storage</span></span>
* <span data-ttu-id="27ffd-647">Lade till meddelande om icke-bakåtkompatibel ändring vid ändring i utdata för Azure File-cmdletar i en framtida version</span><span class="sxs-lookup"><span data-stu-id="27ffd-647">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="27ffd-648">Stöd för nya SkuName StandardGZRS, StandardRAGZRS när ett lagringskonto skapas/uppdateras</span><span class="sxs-lookup"><span data-stu-id="27ffd-648">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="27ffd-649">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27ffd-649">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="27ffd-650">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27ffd-650">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27ffd-651">Stöd för DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="27ffd-651">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="27ffd-652">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27ffd-652">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27ffd-653">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27ffd-653">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27ffd-654">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="27ffd-654">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="27ffd-655">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27ffd-655">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27ffd-656">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="27ffd-656">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="27ffd-657">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27ffd-657">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27ffd-658">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="27ffd-658">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="27ffd-659">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27ffd-659">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="27ffd-660">0.10.0-förhandsversion – April 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-660">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="27ffd-661">Allmänt</span><span class="sxs-lookup"><span data-stu-id="27ffd-661">General</span></span>
* <span data-ttu-id="27ffd-662">Az-moduler är nu tillgängliga i förhandsversion på Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="27ffd-662">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="27ffd-663">Därmed möjliggörs kompatibilitet för flera plattformar med Linux och macOs.</span><span class="sxs-lookup"><span data-stu-id="27ffd-663">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="27ffd-664">Azure Stack Hub stöder nu PowerShell Core med AZ-moduler. Mer information finns [här](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="27ffd-664">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="27ffd-665">Supportprofil för AZ-moduler 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="27ffd-665">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="27ffd-666">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="27ffd-666">Az.Billing</span></span>
  - <span data-ttu-id="27ffd-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-667">Az.Compute</span></span>
  - <span data-ttu-id="27ffd-668">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="27ffd-668">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="27ffd-669">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-669">Az.EventHub</span></span>
  - <span data-ttu-id="27ffd-670">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-670">Az.IotHub</span></span>
  - <span data-ttu-id="27ffd-671">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-671">Az.KeyVault</span></span>
  - <span data-ttu-id="27ffd-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-672">Az.Monitor</span></span>
  - <span data-ttu-id="27ffd-673">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-673">Az.Network</span></span>
  - <span data-ttu-id="27ffd-674">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-674">Az.Resources</span></span>
  - <span data-ttu-id="27ffd-675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-675">Az.Storage</span></span>
  - <span data-ttu-id="27ffd-676">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-676">Az.Websites</span></span>
* <span data-ttu-id="27ffd-677">Tre nya PowerShell-moduler för AZ har introducerats som fungerar med Azure Stack Hub, och de är Az.Databox, Az.IotHub och Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-677">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="27ffd-678">Kommandona är i princip oförändrade, med endast mindre ändringar som att AzureRM ändras till AZ</span><span class="sxs-lookup"><span data-stu-id="27ffd-678">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="27ffd-679">En uppdaterad länk till PowerShell-dokumentationen för Azure Stack Hub finns [här](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="27ffd-679">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="27ffd-680">3.7.0 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-680">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-681">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-682">Åtgärdade ”Get-AzTenant”/”Get-AzDefault”/”Set-AzDefault”-utlösning av NullReferenceException när du inte är inloggad [#10292]</span><span class="sxs-lookup"><span data-stu-id="27ffd-682">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-683">Az.Compute</span></span>
* <span data-ttu-id="27ffd-684">Följande parametrar har lagts till i cmdleten ”New-AzDiskConfig”:</span><span class="sxs-lookup"><span data-stu-id="27ffd-684">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="27ffd-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="27ffd-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="27ffd-686">Tillåten krypteringsegenskap till målparametern för cmdleten ”New-AzGalleryImageVersion”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-686">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="27ffd-687">Åtgärdade tempDisk-problem för cmdletarna ”Set-AzVmss”-Reimage och ”Invoke-AzVMReimage”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-687">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="27ffd-688">[#11354]</span><span class="sxs-lookup"><span data-stu-id="27ffd-688">[#11354]</span></span>
* <span data-ttu-id="27ffd-689">Stöd har lagts till i nedanstående cmdletar för nytt SAP-tillägg</span><span class="sxs-lookup"><span data-stu-id="27ffd-689">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="27ffd-690">”Set-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="27ffd-690">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="27ffd-691">”Get-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="27ffd-691">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="27ffd-692">”Remove-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="27ffd-692">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="27ffd-693">”Update-AzVMAEMExtension”</span><span class="sxs-lookup"><span data-stu-id="27ffd-693">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="27ffd-694">Åtgärdade fel i exempel på hjälpdokument</span><span class="sxs-lookup"><span data-stu-id="27ffd-694">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="27ffd-695">Visade det exakta strängvärdet för VM PowerState i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="27ffd-695">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="27ffd-696">”New-AzVmssConfig”: den fasta serialiseringen av egenskapen AutomaticRepairs när SinglePlacementGroup är inaktiverad.</span><span class="sxs-lookup"><span data-stu-id="27ffd-696">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="27ffd-697">[#11257]</span><span class="sxs-lookup"><span data-stu-id="27ffd-697">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-698">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-699">ADF .Net SDK har uppdaterats till 4.8.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-699">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="27ffd-700">Valfria parametrar har lagts till i kommandot ”Invoke-AzDataFactoryV2Pipeline” för att stödja omkörning</span><span class="sxs-lookup"><span data-stu-id="27ffd-700">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-701">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-701">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-702">Lade till beskrivning för icke-bakåtkompatibel ändring för ”Export-AzDataLakeStoreItem” och ”Import-AzDataLakeStoreItem”</span><span class="sxs-lookup"><span data-stu-id="27ffd-702">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="27ffd-703">Lade till alternativ för bytekodning för ”New-AzDataLakeStoreItem”, ”Add-AzDAtaLakeStoreItemContent” och ”Get-AzDAtaLakeStoreItemContent”</span><span class="sxs-lookup"><span data-stu-id="27ffd-703">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-704">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-704">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-705">Stöd för att ange en minimal TLS-version som stöds när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="27ffd-705">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-706">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-706">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-707">Stöd har lagts till för att hantera distribuerade inställningar per enhet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-707">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="27ffd-708">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-708">New Cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-709">”Get-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="27ffd-709">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="27ffd-710">”Set-AzIotHubDistributedTracing”</span><span class="sxs-lookup"><span data-stu-id="27ffd-710">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-711">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-711">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-712">Ändrade attribut för icke-bakåtkompatibel ändring lades till för ”New-AzKeyVault”</span><span class="sxs-lookup"><span data-stu-id="27ffd-712">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-713">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-713">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-714">Uppdaterad dokumentation för ”New-AzScheduledQueryRuleLogMetricTrigger”</span><span class="sxs-lookup"><span data-stu-id="27ffd-714">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-715">Az.Network</span></span>
* <span data-ttu-id="27ffd-716">Uppdaterade cmdletar för att tillåta VirtualHubVnetConnections mellan klienter</span><span class="sxs-lookup"><span data-stu-id="27ffd-716">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="27ffd-717">”New-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="27ffd-717">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27ffd-718">”Update-AzVirtualHubVnetConnection”</span><span class="sxs-lookup"><span data-stu-id="27ffd-718">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27ffd-719">”New-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="27ffd-719">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="27ffd-720">”Update-AzVirtualHub”</span><span class="sxs-lookup"><span data-stu-id="27ffd-720">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="27ffd-721">SQL Management SDK-beroende har tagits bort</span><span class="sxs-lookup"><span data-stu-id="27ffd-721">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27ffd-722">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-722">Az.PolicyInsights</span></span>
* <span data-ttu-id="27ffd-723">Förbättrade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="27ffd-723">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-724">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-724">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-725">Azure Site Recovery har lagt till stöd för återaktivering av skydd och uppdaterade VM-egenskaper för virtuella Azure-datorer med krypterad disk.</span><span class="sxs-lookup"><span data-stu-id="27ffd-725">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="27ffd-726">Lade till Azure Site Recovery VmwareToAzure-egenskaper för DR-övervakning</span><span class="sxs-lookup"><span data-stu-id="27ffd-726">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="27ffd-727">Azure Backup har lagt till stöd för att försöka uppdatera principuppdateringen för misslyckade objekt på nytt.</span><span class="sxs-lookup"><span data-stu-id="27ffd-727">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="27ffd-728">Azure Backup lagt till stöd för diskundantagsinställningar under säkerhetskopiering och återställning.</span><span class="sxs-lookup"><span data-stu-id="27ffd-728">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="27ffd-729">Azure Backup lagt till stöd för att återställa flera filer/mappar i AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="27ffd-729">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="27ffd-730">Azure Backup lade till support för användardefinierad Resourcegroup-support vid uppdatering av IaasVM-princip</span><span class="sxs-lookup"><span data-stu-id="27ffd-730">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-731">Az.Resources</span></span>
* <span data-ttu-id="27ffd-732">Åtgärdade ”Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType” så att den använder den faktisk apiVersion av resurser i stället för standard-apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="27ffd-732">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="27ffd-733">Lade till correlationId-loggning för felscenarier</span><span class="sxs-lookup"><span data-stu-id="27ffd-733">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="27ffd-734">Liten dokumentationsändring för ”Get-AzResourceLock”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-734">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="27ffd-735">Lade till exempel.</span><span class="sxs-lookup"><span data-stu-id="27ffd-735">Added example.</span></span>
* <span data-ttu-id="27ffd-736">Undantaget enkelt citattecken i parametervärde för ”Get-AzADUser” [#11317]</span><span class="sxs-lookup"><span data-stu-id="27ffd-736">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="27ffd-737">Nya cmdletar har lagts till för distributionsskript (”Get-AzDeploymentScript”, ”Get-AzDeploymentScriptLog”, ”Save-AzDeploymentScriptLog”, ”Remove-AzDeploymentScript”)</span><span class="sxs-lookup"><span data-stu-id="27ffd-737">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-738">Az.Sql</span></span>
* <span data-ttu-id="27ffd-739">En läsbar sekundär parameter har lagts till i Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="27ffd-739">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="27ffd-740">Cmdleten Disable-AzSqlServerActiveDirectoryOnlyAuthentication har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-740">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="27ffd-741">Den sparade känslighet rangordningen när kolumner klassificeras i databasen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-741">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="27ffd-742">Az.Support</span><span class="sxs-lookup"><span data-stu-id="27ffd-742">Az.Support</span></span>
* <span data-ttu-id="27ffd-743">Allmän tillgänglighet för ”Az.Support”-modulen</span><span class="sxs-lookup"><span data-stu-id="27ffd-743">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-744">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-744">Az.Websites</span></span>
* <span data-ttu-id="27ffd-745">Stöd har lagts till för att arbeta med trafikdirigeringsregler för webbappar under nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-745">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="27ffd-746">”Get-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="27ffd-746">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="27ffd-747">”Update-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="27ffd-747">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="27ffd-748">”Add-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="27ffd-748">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="27ffd-749">”Remove-AzWebAppTrafficRouting”</span><span class="sxs-lookup"><span data-stu-id="27ffd-749">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="27ffd-750">3.6.1 – mars 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-750">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-751">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-752">Öppna sidan med Azure PowerShell-enkäten i ”Send-Feedback” [#11020]</span><span class="sxs-lookup"><span data-stu-id="27ffd-752">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="27ffd-753">Visa URL:en för Azure PowerShell-enkäten i ”Resolve-Error” [#11021]</span><span class="sxs-lookup"><span data-stu-id="27ffd-753">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="27ffd-754">Az-version har lagts till i UserAgent</span><span class="sxs-lookup"><span data-stu-id="27ffd-754">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-755">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-755">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-756">Stöd har lagts till för att hämta och konfigurera en anpassad domän på DeveloperPortal-slutpunkten [#11007]</span><span class="sxs-lookup"><span data-stu-id="27ffd-756">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="27ffd-757">”Export-AzApiManagementApi” Stöd har lagts till för att ladda ned API-definition i Json-format [#9987]</span><span class="sxs-lookup"><span data-stu-id="27ffd-757">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="27ffd-758">”Import-AzApiManagementApi” Stöd har lagts till för att importera OpenApi 3.0-definition från Json-dokument</span><span class="sxs-lookup"><span data-stu-id="27ffd-758">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="27ffd-759">”New-AzApiManagementIdentityProvider” och ”Set-AzApiManagementIdentityProvider” Stöd har lagts till för att konfigurera ”Signin Tenant” för AAD B2C-provider [#9784]</span><span class="sxs-lookup"><span data-stu-id="27ffd-759">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-760">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-760">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-761">En referens har uttryckligen lagts till för System.Buffers i csproj och psd1.</span><span class="sxs-lookup"><span data-stu-id="27ffd-761">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-762">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-762">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-763">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27ffd-763">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="27ffd-764">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-764">New Cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-765">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27ffd-765">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27ffd-766">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27ffd-766">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27ffd-767">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27ffd-767">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27ffd-768">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27ffd-768">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="27ffd-769">Stöd har lagts till för att hantera moduler på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27ffd-769">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="27ffd-770">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-770">New Cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-771">”Add-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="27ffd-771">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="27ffd-772">”Get-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="27ffd-772">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="27ffd-773">”Remove-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="27ffd-773">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="27ffd-774">”Set-AzIotHubModule”</span><span class="sxs-lookup"><span data-stu-id="27ffd-774">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="27ffd-775">Cmdlet har lagts till för att hämta anslutningssträngen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27ffd-775">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="27ffd-776">Cmdlet har lagts till för att hämta anslutningssträngen för en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27ffd-776">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="27ffd-777">Stöd har lagts till för att hämta/ange en överordnad enhet för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-777">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="27ffd-778">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-778">New Cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-779">”Get-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="27ffd-779">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="27ffd-780">”Set-AzIotHubDeviceParent”</span><span class="sxs-lookup"><span data-stu-id="27ffd-780">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="27ffd-781">Stöd har lagts till för att hantera en enhets överordnade och underordnade relationer.</span><span class="sxs-lookup"><span data-stu-id="27ffd-781">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-782">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-782">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-783">Utdatavärdet har åtgärdats för ”Get-AzMetricDefinition” [#9714]</span><span class="sxs-lookup"><span data-stu-id="27ffd-783">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-784">Az.Network</span></span>
* <span data-ttu-id="27ffd-785">SQL Management SDK har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-785">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="27ffd-786">Ett problem har åtgärdats med namngivningsskillnader i klassen PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="27ffd-786">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="27ffd-787">Fältet ActionsRequired mappar till ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="27ffd-787">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="27ffd-788">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="27ffd-788">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-789">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-789">Az.Resources</span></span>
* <span data-ttu-id="27ffd-790">Null-referensfel har åtgärdats i ”Get-AzRoleAssignment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-790">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="27ffd-791">Växlarna ”-Force” och ”-PassThru” är valfria i ”Remove-AzADGroup” [#10849]</span><span class="sxs-lookup"><span data-stu-id="27ffd-791">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="27ffd-792">Ett problem har åtgärdats som gjorde att ”MailNickname” inte returnerades i ”Remove-AzADGroup” [#11167]</span><span class="sxs-lookup"><span data-stu-id="27ffd-792">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="27ffd-793">Ett problem har åtgärdats som gjorde att pipe-åtgärden ”Remove-AzADGroup” inte fungerar [#11171]</span><span class="sxs-lookup"><span data-stu-id="27ffd-793">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="27ffd-794">Ett null-referensfel har åtgärdats i GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="27ffd-794">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="27ffd-795">Attribut för icke-bakåtkompatibla ändringar har lagts till för kommande ändringar i cmdlets för principer</span><span class="sxs-lookup"><span data-stu-id="27ffd-795">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="27ffd-796">”Get-AzResourceGroup” har uppdaterats för att utföra taggfiltrering för resursgrupper på serversidan</span><span class="sxs-lookup"><span data-stu-id="27ffd-796">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="27ffd-797">Utökade Tag-cmdlets stöder -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ffd-797">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="27ffd-798">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ffd-798">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="27ffd-799">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ffd-799">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="27ffd-800">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ffd-800">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="27ffd-801">Ny Tag-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-801">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="27ffd-802">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ffd-802">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="27ffd-803">Flyttade ScopedDeployment från SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-803">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-804">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-804">Az.Sql</span></span>
* <span data-ttu-id="27ffd-805">PublicNetworkAccess har lagts till i ”New-AzSqlServer” och ”Set-AzSqlServer”</span><span class="sxs-lookup"><span data-stu-id="27ffd-805">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="27ffd-806">Stöd har lagts till för konfiguration av säkerhetskopiering för långsiktig kvarhållning för hanterade databaser</span><span class="sxs-lookup"><span data-stu-id="27ffd-806">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="27ffd-807">Hämta/ange LTR-princip på en hanterad databas</span><span class="sxs-lookup"><span data-stu-id="27ffd-807">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="27ffd-808">Hämta LTR-säkerhetskopior efter hanterad databas, hanterad instans eller plats</span><span class="sxs-lookup"><span data-stu-id="27ffd-808">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="27ffd-809">Ta bort en LTR-säkerhetskopia</span><span class="sxs-lookup"><span data-stu-id="27ffd-809">Remove an LTR backup</span></span>
    - <span data-ttu-id="27ffd-810">Återställa en LTR-säkerhetskopia för att skapa en ny hanterad databas</span><span class="sxs-lookup"><span data-stu-id="27ffd-810">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="27ffd-811">MinimalTlsVersion har lagts till för New-AzSqlServer och Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="27ffd-811">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="27ffd-812">MinimalTlsVersion har lagts till för New-AzSqlInstance och Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27ffd-812">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="27ffd-813">SQL SDK-versionen för Az.Network har ändrats</span><span class="sxs-lookup"><span data-stu-id="27ffd-813">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-814">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-814">Az.Storage</span></span>
* <span data-ttu-id="27ffd-815">AllowProtectedAppendWrite stöds i ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-815">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="27ffd-816">”Set-AzRmStorageContainerImmutabilityPolicy”</span><span class="sxs-lookup"><span data-stu-id="27ffd-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="27ffd-817">Varningsmeddelande har lagts till om icke-bakåtkompatibel ändring för ändring av typen AzureStorageTable i en senare version</span><span class="sxs-lookup"><span data-stu-id="27ffd-817">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="27ffd-818">”New-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="27ffd-818">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="27ffd-819">”Get-AzStorageTable”</span><span class="sxs-lookup"><span data-stu-id="27ffd-819">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-820">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-820">Az.Websites</span></span>
* <span data-ttu-id="27ffd-821">Tag-parametern har lagts till för ”New-AzAppServicePlan” och ”Set-AzAppServicePlan”</span><span class="sxs-lookup"><span data-stu-id="27ffd-821">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="27ffd-822">Stoppa cmdlet-körning om ett undantag uppstår när en anpassad domän läggs till på en webbplats</span><span class="sxs-lookup"><span data-stu-id="27ffd-822">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="27ffd-823">Stöd har lagts till för att utföra åtgärder för App Services som inte tillhör samma resursgrupp som App Services-planen</span><span class="sxs-lookup"><span data-stu-id="27ffd-823">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="27ffd-824">Åtkomstbegränsning har tillämpats på WebApp/Function i olika resursgrupper</span><span class="sxs-lookup"><span data-stu-id="27ffd-824">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="27ffd-825">Ett problem har åtgärdats för att ange anpassade värdnamn för WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="27ffd-825">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="27ffd-826">3.5.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-826">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27ffd-827">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="27ffd-827">Highlights since the last major release</span></span>
* <span data-ttu-id="27ffd-828">Uppdaterade telemetri på klientsidan.</span><span class="sxs-lookup"><span data-stu-id="27ffd-828">Updated client side telemetry.</span></span>
* <span data-ttu-id="27ffd-829">Az.IotHub lade till cmdletar som stöd för att hantera enheter.</span><span class="sxs-lookup"><span data-stu-id="27ffd-829">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="27ffd-830">Az.SqlVirtualMachine lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="27ffd-830">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-831">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-832">Lade till SubscriptionId, TenantId och körningstid i data för telemetri på klientsidan</span><span class="sxs-lookup"><span data-stu-id="27ffd-832">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-833">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-833">Az.Automation</span></span>
* <span data-ttu-id="27ffd-834">Åtgärdade skrivfel i exempel 1 i referensdokumentation för ”New-AzAutomationSoftwareUpdateConfiguration”</span><span class="sxs-lookup"><span data-stu-id="27ffd-834">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-835">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-835">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-836">Uppdaterade SDK till 7.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-836">Updated SDK to 7.0</span></span>
* <span data-ttu-id="27ffd-837">Förbättrade felmeddelande vid serversvar om tom brödtext</span><span class="sxs-lookup"><span data-stu-id="27ffd-837">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-838">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-838">Az.Compute</span></span>
* <span data-ttu-id="27ffd-839">Tillät tomt värde för ProximityPlacementGroupId under uppdatering</span><span class="sxs-lookup"><span data-stu-id="27ffd-839">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27ffd-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-840">Az.FrontDoor</span></span>
* <span data-ttu-id="27ffd-841">Lade till cmdlet för att hämta hanterade regeldefinitioner som kan användas i WAF</span><span class="sxs-lookup"><span data-stu-id="27ffd-841">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-842">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-842">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-843">Lade till stöd för att hantera enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27ffd-843">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="27ffd-844">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-844">New Cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-845">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27ffd-845">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27ffd-846">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27ffd-846">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27ffd-847">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27ffd-847">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27ffd-848">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="27ffd-848">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-849">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-849">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-850">Åtgärdade duplicerad text för Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-850">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-851">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-851">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-852">Åtgärdade beskrivning av cmdleten Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="27ffd-852">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="27ffd-853">En ny parameter med namnet ActionGroupId har lagts till i kommandot ”New-AzMetricAlertRuleV2”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-853">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="27ffd-854">Användaren kan ange ActionGroupId(string) eller ActionGroup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="27ffd-854">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-855">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-855">Az.Network</span></span>
* <span data-ttu-id="27ffd-856">Lade till en extra parameteranteckning för parametern ”-EnableProxyProtocol” för cmdleten ”New-AzPrivateLinkService”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-856">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="27ffd-857">Åtgärdade FilterData-exempel i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="27ffd-857">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="27ffd-858">Lade till paketinsamlingsexempel för att samla in alla inre och yttre paket i Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="27ffd-858">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="27ffd-859">Lade till stöd för Azure-brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="27ffd-859">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="27ffd-860">Inga nya cmdletar har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-860">No new cmdlets are added.</span></span> <span data-ttu-id="27ffd-861">Lättar begränsningen för brandväggsprincip på VNet-brandväggar</span><span class="sxs-lookup"><span data-stu-id="27ffd-861">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-862">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-862">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-863">Lade till stöd för Restore-as-files för SQL-databaser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-863">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-864">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-864">Az.Resources</span></span>
* <span data-ttu-id="27ffd-865">Omstrukturerade cmdletar för malldistribution</span><span class="sxs-lookup"><span data-stu-id="27ffd-865">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="27ffd-866">Lade till nya cmdletar för att hantera distributioner i hanteringsgruppen: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="27ffd-866">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="27ffd-867">Lade till nya cmdletar för att hantera distributioner i klientorganisationsområdet: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="27ffd-867">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="27ffd-868">Omstrukturerade \*-AzDeployment-cmdletar för att fungera specifikt i prenumerationsomfattningen</span><span class="sxs-lookup"><span data-stu-id="27ffd-868">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="27ffd-869">Skapade alias \*-AzSubscriptionDeployment för \*-AzDeployment-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-869">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="27ffd-870">Åtgärdade ”Update-AzADApplication” när parametern ”AvailableToOtherTenants” inte har angetts</span><span class="sxs-lookup"><span data-stu-id="27ffd-870">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="27ffd-871">Tog bort ApplicationObjectWithoutCredentialParameterSet för att undvika AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="27ffd-871">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="27ffd-872">Återskapade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="27ffd-872">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-873">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-873">Az.Sql</span></span>
* <span data-ttu-id="27ffd-874">Lade till stöd för återställning till tidpunkt mellan prenumerationer på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-874">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="27ffd-875">Lade till stöd för att ändra befintlig SQL Managed Instance-maskinvarugenerering</span><span class="sxs-lookup"><span data-stu-id="27ffd-875">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="27ffd-876">Åtgärdade ”Update-AzSqlServerVulnerabilityAssessmentSetting”-hjälpexempel: parameter/egenskapsutdata - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="27ffd-876">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="27ffd-877">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="27ffd-877">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="27ffd-878">Lade till cmdletar för lyssningsfunktion för tillgänglighetsgrupp</span><span class="sxs-lookup"><span data-stu-id="27ffd-878">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27ffd-879">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27ffd-879">Az.StorageSync</span></span>
* <span data-ttu-id="27ffd-880">Uppdaterade teckenuppsättningar som stöds i ”Invoke-AzStorageSyncCompatibilityCheck”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-880">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="27ffd-881">3.4.0 – februari 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-881">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27ffd-882">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="27ffd-882">Highlights since the last major release</span></span>
* <span data-ttu-id="27ffd-883">Första Az.CosmosDB-versionen 0.1.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="27ffd-883">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="27ffd-884">Stöd för Az.Network ConnectionMonitor V2 har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-884">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-885">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-885">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-886">Inaktivera automatisk sparande av kontext när AzureRmContext.json inte är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="27ffd-886">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="27ffd-887">Uppdatera referensen till Azure Powershell Common till 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="27ffd-887">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-888">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-888">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-889">**Get-AzApiManagementApiSchema** Hämtning av Open-Api-schema som är associerat med ett API har åtgärdats   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="27ffd-889">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="27ffd-890">**New-AzApiManagementProduct**\* och **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="27ffd-890">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="27ffd-891">Åtgärda dokumentation för https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="27ffd-891">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="27ffd-892">**Set-AzApiManagementApi** Exempel för att visa hur ServiceUrl uppdateras med hjälp av cmdleten har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-892">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-893">Az.Compute</span></span>
* <span data-ttu-id="27ffd-894">Begränsa antalet VM-status till 100 för att undvika begränsning när Get-AzVM -Status utförs utan VM-namn.</span><span class="sxs-lookup"><span data-stu-id="27ffd-894">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="27ffd-895">Lägg till cmdleten Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-895">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="27ffd-896">Lägg till parametrarna EncryptionType och DiskEncryptionSetId i följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-896">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="27ffd-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="27ffd-898">Lägg till parametern ColocationStatus för cmdleten Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="27ffd-898">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-899">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-899">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-900">Uppdatera ADF .Net SDK-versionen till 4.7.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-900">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="27ffd-901">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="27ffd-901">Az.DeploymentManager</span></span>
* <span data-ttu-id="27ffd-902">Lägger till LIST-åtgärder för resurser</span><span class="sxs-lookup"><span data-stu-id="27ffd-902">Adds LIST operations for resources</span></span>
* <span data-ttu-id="27ffd-903">Lägger till funktion för att utföra åtgärder för hälsokontrollsteg</span><span class="sxs-lookup"><span data-stu-id="27ffd-903">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-904">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-904">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-905">Åtgärda dokumentfel för New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="27ffd-905">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-906">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-907">Lägg till Name-alias för attributet VaultName så att Remove-AzureKeyVault stämmer överens med New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="27ffd-907">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-908">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-908">Az.Network</span></span>
* <span data-ttu-id="27ffd-909">Nytt exempel har lagts till i Set-AzNetworkWatcherConfigFlowLog.md för att demonstrera ett inaktiveringsscenario för Trafikanalys.</span><span class="sxs-lookup"><span data-stu-id="27ffd-909">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="27ffd-910">Lägg till stöd för att tilldela konfiguration av hanterings-IP till Azure Firewall – ett dedikerat undernät och en offentlig IP som brandväggen använder för dess hanteringstrafik</span><span class="sxs-lookup"><span data-stu-id="27ffd-910">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="27ffd-911">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="27ffd-911">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="27ffd-912">Parametern -ManagementPublicIpAddress (inte obligatorisk) som accepterar ett offentligt IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-912">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="27ffd-913">Metoden SetManagementIpConfiguration har lagts till för brandväggsobjekt – kräver ett undernät och en offentlig IP-adress som indata – undernätets namn måste vara ”AzureFirewallManagementSubnet”</span><span class="sxs-lookup"><span data-stu-id="27ffd-913">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="27ffd-914">Exempel för Get-AzNetworkSecurityGroup har korrigerats så att exempel visas för NSG:er i stället för nätverksgränssnitt.</span><span class="sxs-lookup"><span data-stu-id="27ffd-914">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="27ffd-915">Ett skrivfel har åtgärdats i kommandot New-AzVpnSite som hindrade kompletteraren för resurs-ID från att fylla i en parameter.</span><span class="sxs-lookup"><span data-stu-id="27ffd-915">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="27ffd-916">Stöd för Url-konfiguration i åtgärdsuppsättningen för omskrivningsregler i Application Gateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-916">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="27ffd-917">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-917">New cmdlets added:</span></span>
        - <span data-ttu-id="27ffd-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="27ffd-919">Cmdletar har uppdaterats med den valfria parametern -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-919">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="27ffd-920">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-920">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="27ffd-921">Lägg till stöd för resurser för NetworkWatcher ConnectionMonitor version 2</span><span class="sxs-lookup"><span data-stu-id="27ffd-921">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27ffd-922">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-922">Az.PolicyInsights</span></span>
* <span data-ttu-id="27ffd-923">Stöd för utvärdering av efterlevnad innan fastställande av vilken resurs som ska åtgärdas</span><span class="sxs-lookup"><span data-stu-id="27ffd-923">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="27ffd-924">Lägg till parametern ”-ResourceDiscoverMode” för Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="27ffd-924">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="27ffd-925">Lägg till cmdleten Get-AzPolicyMetadata för att hämta resurser för principmetadata</span><span class="sxs-lookup"><span data-stu-id="27ffd-925">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="27ffd-926">Get-AzPolicyState och Get-AzPolicyStateSummary för API-versionen 2019-10-01 har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="27ffd-926">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-927">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-928">Azure Site Recovery-stöd för att ta bort en replikerad disk.</span><span class="sxs-lookup"><span data-stu-id="27ffd-928">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="27ffd-929">Tillagt Azure Backup-stöd för att lägga till taggar när ett Recovery Services-valv skapas.</span><span class="sxs-lookup"><span data-stu-id="27ffd-929">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-930">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-930">Az.Resources</span></span>
* <span data-ttu-id="27ffd-931">Gör -Scope valfritt i cmdletarna \*-AzPolicyAssignment med standardinställning till kontextprenumeration</span><span class="sxs-lookup"><span data-stu-id="27ffd-931">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="27ffd-932">Lägg till exempel på att skapa ADServicePrincipal med lösenord och nyckelautentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="27ffd-932">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-933">Az.Sql</span></span>
<span data-ttu-id="27ffd-934">Åtgärda cmdleten New-AzSqlDatabaseSecondary så att existensen PartnerDatabaseName kontrolleras i stället för existensen DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="27ffd-934">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-935">Az.Storage</span></span>
* <span data-ttu-id="27ffd-936">Stöd för angivning av krypteringsnyckeltyp för Tabell/kö i Skapa lagringskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-936">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="27ffd-937">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-937">New-AzStorageAccount</span></span>
* <span data-ttu-id="27ffd-938">Visa RequestId när StorageException inte har ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="27ffd-938">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="27ffd-939">Åtgärda exempel 6 för cmdleten Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27ffd-939">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-940">Az.Websites</span></span>
* <span data-ttu-id="27ffd-941">Set-AzWebapp och Set-AzWebappSlot stöder egenskaperna AlwaysOn, MinTls och FtpsState</span><span class="sxs-lookup"><span data-stu-id="27ffd-941">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="27ffd-942">Åtgärdar problemet där inställning av HttpsOnly samtidigt som AppservicePlan ändrades med det enskilda kommandot Set-AzWebApp återställde HttpsOnly till standardvärdet</span><span class="sxs-lookup"><span data-stu-id="27ffd-942">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="27ffd-943">3.3.0 – januari 2020</span><span class="sxs-lookup"><span data-stu-id="27ffd-943">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-944">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-944">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-945">Nu stöder Add-AzEnvironment och Set-AzEnvironment parametrarna AzureAttestationServiceEndpointResourceId och AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="27ffd-945">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27ffd-946">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27ffd-946">Az.Cdn</span></span>
* <span data-ttu-id="27ffd-947">Information om felsvar visas i New-AzCdnEndpoint-cmdleten</span><span class="sxs-lookup"><span data-stu-id="27ffd-947">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-948">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-948">Az.Compute</span></span>
* <span data-ttu-id="27ffd-949">Set-AzVMCustomScriptExtension-cmdleten har åtgärdats för en virtuell dator med hanterad OD-disk som inte har någon operativsystemprofil.</span><span class="sxs-lookup"><span data-stu-id="27ffd-949">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="27ffd-950">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27ffd-950">Az.ContainerInstance</span></span>
* <span data-ttu-id="27ffd-951">Parameternamn som används med New-AzContainerGroup-exempel har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-951">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="27ffd-952">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="27ffd-952">Az.DataBoxEdge</span></span>
* <span data-ttu-id="27ffd-953">Cmdleten ”Get-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-953">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27ffd-954">Hämta gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="27ffd-954">Get the Edge Storage Container</span></span>
* <span data-ttu-id="27ffd-955">Cmdleten ”New-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-955">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27ffd-956">Skapa en ny gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="27ffd-956">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="27ffd-957">Cmdleten ”Remove-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-957">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27ffd-958">Ta bort gränslagringscontainern</span><span class="sxs-lookup"><span data-stu-id="27ffd-958">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="27ffd-959">Cmdleten ”Invoke-AzDataBoxEdgeStorageContainer” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-959">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27ffd-960">Anropa åtgärd för att uppdatera data i gränslagringscontainer</span><span class="sxs-lookup"><span data-stu-id="27ffd-960">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="27ffd-961">Cmdleten ”Get-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-961">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="27ffd-962">Hämta gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="27ffd-962">Get the Edge Storage Account</span></span>
* <span data-ttu-id="27ffd-963">Cmdleten ”New-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-963">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="27ffd-964">Skapa ett nytt gränslagringskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-964">Create new Edge Storage Account</span></span>
* <span data-ttu-id="27ffd-965">Cmdleten ”Remove-AzDataBoxEdgeStorageAccount” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-965">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="27ffd-966">Ta bort gränslagringskontot</span><span class="sxs-lookup"><span data-stu-id="27ffd-966">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="27ffd-967">Anropa cmdleten ”Invoke-AzDataBoxEdgeShare”</span><span class="sxs-lookup"><span data-stu-id="27ffd-967">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="27ffd-968">Anropa åtgärd för att uppdatera resursdata</span><span class="sxs-lookup"><span data-stu-id="27ffd-968">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="27ffd-969">Cmdleten ”Set-AzDataBoxEdgeStorageAccountCredential” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-969">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="27ffd-970">Ange autentiseringsuppgifter för az databoxedge-lagringskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-970">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-971">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-971">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-972">Lägg till AutoUpdateETA-, LatestVersion-, PushedVersion-, TaskQueueId- och VersionStatus-egenskaper för Get-AzDataFactoryV2IntegrationRuntime-cmd</span><span class="sxs-lookup"><span data-stu-id="27ffd-972">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="27ffd-973">Uppdatera ADF .Net SDK-versionen till 4.6.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-973">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="27ffd-974">Lägg till parametern ”PublicIPs” för ”Set-AzureRmDataFactoryV2IntegrationRuntime”-cmd så att Azure-SSIS IR kan skapas med statiska offentliga IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-974">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="27ffd-975">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="27ffd-975">Az.DevTestLabs</span></span>
* <span data-ttu-id="27ffd-976">Ta bort den brutna länken i Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-976">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27ffd-977">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-977">Az.EventHub</span></span>
* <span data-ttu-id="27ffd-978">Korrigering av problem 10634: Åtgärda referensen till null-objekt för eventhubnamespace-borttagning</span><span class="sxs-lookup"><span data-stu-id="27ffd-978">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-979">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-979">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-980">Åtgärda Invoke-AzHDInsightHiveJob.md-fel.</span><span class="sxs-lookup"><span data-stu-id="27ffd-980">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="27ffd-981">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="27ffd-981">Az.MachineLearning</span></span>
* <span data-ttu-id="27ffd-982">Nedanstående cmdletar har tagits bort eftersom MachineLearningCompute inte längre är tillgängligt</span><span class="sxs-lookup"><span data-stu-id="27ffd-982">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="27ffd-983">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="27ffd-983">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="27ffd-984">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="27ffd-984">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="27ffd-985">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="27ffd-985">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="27ffd-986">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="27ffd-986">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="27ffd-987">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="27ffd-987">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="27ffd-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="27ffd-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="27ffd-989">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="27ffd-989">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-990">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-990">Az.Network</span></span>
* <span data-ttu-id="27ffd-991">Uppgradera beroende av Microsoft.Azure.Management.Sql från 1.36-preview till 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="27ffd-991">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-992">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-993">Ändrat Azure Site Recovery-stöd för krypterade vilande data på virtuella datorer med hanterade diskar med kundhanterade nycklar för Azure till Azure-providern.</span><span class="sxs-lookup"><span data-stu-id="27ffd-993">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="27ffd-994">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-994">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="27ffd-995">Azure Site Recovery-stöd för att ange ID för diskkrypteringsuppsättning som valfri inmatning på disknivå för aktivering av skydd för VMware till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-995">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="27ffd-996">Azure Site Recovery-stöd för att uppdatera replikeringsskyddade objekt med mappning för diskkrypteringsuppsättning för HyperV till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-996">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-997">Az.Resources</span></span>
* <span data-ttu-id="27ffd-998">Åtgärda ett fel i hjälpdokument för ”Remove-AzTag”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-998">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-999">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1000">Åtgärda funktioner i cmdletar för att ange baslinjen för sårbarhetsbedömning för arbete med huvuddatabasen för Azure-databasen och begränsa den för systemdatabaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1000">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="27ffd-1001">Åtgärda ett fel när en redundansgrupp för en SQL-instans skapas</span><span class="sxs-lookup"><span data-stu-id="27ffd-1001">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="27ffd-1002">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="27ffd-1002">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="27ffd-1003">Lägg till DR som en ny giltig licenstyp</span><span class="sxs-lookup"><span data-stu-id="27ffd-1003">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-1004">Az.Storage</span></span>
* <span data-ttu-id="27ffd-1005">Lägg till varningsmeddelande om icke-bakåtkompatibel ändring för DefaultAction-värdeändring i en framtida version</span><span class="sxs-lookup"><span data-stu-id="27ffd-1005">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="27ffd-1006">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1006">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="27ffd-1007">Stöd för att hämta lagringskontots senaste synkroniseringstid genom att köra get-AzureRMStorageAccount med parametern -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1007">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="27ffd-1008">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-1008">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="27ffd-1009">3.2.0 – December 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1009">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="27ffd-1010">Allmänt</span><span class="sxs-lookup"><span data-stu-id="27ffd-1010">General</span></span>
* <span data-ttu-id="27ffd-1011">Uppdatera referenser i .psd1 för att använda relativa sökvägar för alla moduler</span><span class="sxs-lookup"><span data-stu-id="27ffd-1011">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-1012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1012">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-1013">Ange rätt UserAgent för telemetri på klientsidan för Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="27ffd-1013">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="27ffd-1014">Visa användarvänligt felmeddelande när kontexten är null i Az 4.0 preview</span><span class="sxs-lookup"><span data-stu-id="27ffd-1014">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27ffd-1015">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27ffd-1015">Az.Batch</span></span>
* <span data-ttu-id="27ffd-1016">Korrigera problem [#10602](https://github.com/Azure/azure-powershell/issues/10602), där **New-AzBatchPool** skickade VirtualMachineConfiguration.ContainerConfiguration eller VirtualMachineConfiguration.DataDisks på ett felaktigt sätt till servern.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1016">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-1017">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-1017">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-1018">Uppdatera ADF .Net SDK-versionen till 4.5.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1018">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27ffd-1019">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1019">Az.FrontDoor</span></span>
* <span data-ttu-id="27ffd-1020">Stöd har lagts till för undantag för hanterade regler för brandväggen för webbaserade program</span><span class="sxs-lookup"><span data-stu-id="27ffd-1020">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="27ffd-1021">Lägg till SocketAddr för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="27ffd-1021">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27ffd-1022">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27ffd-1022">Az.HealthcareApis</span></span>
* <span data-ttu-id="27ffd-1023">Undantagshantering</span><span class="sxs-lookup"><span data-stu-id="27ffd-1023">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-1024">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-1025">Åtgärdat fel vid åtkomst av värde som kanske inte har angetts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1025">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="27ffd-1026">Hantering av ECC-certifikat (Elliptic Curve Cryptography)</span><span class="sxs-lookup"><span data-stu-id="27ffd-1026">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="27ffd-1027">Stöd har lagts till för att ange kurvan för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="27ffd-1027">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-1028">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1028">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-1029">Lägger till valfritt argument i kommandot Lägg till diagnostikinställningar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1029">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="27ffd-1030">Ett växelargument som om det finns visar att exporten till Log Analytics måste ske till ett fast schema (kallas även</span><span class="sxs-lookup"><span data-stu-id="27ffd-1030">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="27ffd-1031">dedikerad, datatyp)</span><span class="sxs-lookup"><span data-stu-id="27ffd-1031">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1032">Az.Network</span></span>
* <span data-ttu-id="27ffd-1033">Stöd för IpGroups i program-, NAT- och nätverksregler för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1033">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-1034">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-1034">Az.Resources</span></span>
* <span data-ttu-id="27ffd-1035">Åtgärda ett problem där malldistributionen inte kan läsa en mallparameter om dess namn står i konflikt med ett inbyggt parameternamn.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1035">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="27ffd-1036">Uppdaterade princip-cmdletar för att använda den nya API-versionen 2019-09-01 som introducerar grupperingsstöd inom principuppsättningsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1036">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1037">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1037">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1038">Uppgraderad funktion för att skapa lagring i automatisk aktivering av sårbarhetsbedömning till StorageV2</span><span class="sxs-lookup"><span data-stu-id="27ffd-1038">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-1039">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-1039">Az.Storage</span></span>
* <span data-ttu-id="27ffd-1040">Stöd för generering av blob/container-identitetsbaserad SAS-token med lagringskontextbaserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="27ffd-1040">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="27ffd-1041">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="27ffd-1041">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="27ffd-1042">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="27ffd-1042">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="27ffd-1043">Stöd för återkallning av användardelegeringsnycklar för lagringskonto för att återkalla alla SAS-token</span><span class="sxs-lookup"><span data-stu-id="27ffd-1043">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="27ffd-1044">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="27ffd-1044">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="27ffd-1045">Uppgradera till Microsoft.Azure.Management.Storage 14.2.0 för att stödja den nya API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1045">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="27ffd-1046">Stöd för QuotaGiB (resurskvot i Gibibye) för värden över 5120 i hanteringsplanet för cmdletar för filresurser och parameteraliaset. Quota har också lagts till för parametern ”QuotaGiB”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1046">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="27ffd-1047">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1047">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="27ffd-1048">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1048">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="27ffd-1049">Lägg till parameteraliaset QuotaGiB i parametern Quota</span><span class="sxs-lookup"><span data-stu-id="27ffd-1049">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="27ffd-1050">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="27ffd-1050">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="27ffd-1051">Åtgärda problemet att Set-AzStorageContainerAcl kan rensa den lagrade åtkomstprincipen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1051">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="27ffd-1052">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="27ffd-1052">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="27ffd-1053">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1053">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27ffd-1054">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1054">Highlights since the last major release</span></span>
* <span data-ttu-id="27ffd-1055">Az.DataBoxEdge 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1055">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="27ffd-1056">Az.SqlVirtualMachine 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1056">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1057">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1058">Funktion för att använda en virtuell dator igen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1058">VM Reapply feature</span></span>
    - <span data-ttu-id="27ffd-1059">Lägg till parameter för att använda igen till cmdleten Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="27ffd-1059">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="27ffd-1060">Funktionen AutomaticRepairs i VM-skalningsuppsättningar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1060">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="27ffd-1061">Lägg till parametrarna EnableAutomaticRepair, AutomaticRepairGracePeriod och AutomaticRepairMaxInstanceRepairsPercent till följande cmdletar:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27ffd-1061">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="27ffd-1062">Stöd för galleriavbildningar i flera klientorganisationer för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="27ffd-1062">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="27ffd-1063">Lägg till "Spot" till argumentslutföraren i prioritetsparametern i cmdletarna New-AzVM, New-AzVMConfig och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27ffd-1063">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="27ffd-1064">Lägg till parametrarna DiskIOPSReadWrite och DiskMBpsReadWrite till cmdleten Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="27ffd-1064">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="27ffd-1065">Ändra parametern SourceImageId för cmdleten New-AzGalleryImageVersion till valfri</span><span class="sxs-lookup"><span data-stu-id="27ffd-1065">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="27ffd-1066">Lägg till parametrarna OSDiskImage och DataDiskImage till cmdleten New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="27ffd-1066">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="27ffd-1067">Lägg till parametern HyperVGeneration till cmdleten New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="27ffd-1067">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="27ffd-1068">Lägg till parametern SkipExtensionsOnOverprovisionedVMs till cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27ffd-1068">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="27ffd-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="27ffd-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="27ffd-1070">Cmdleten `Get-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1070">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="27ffd-1071">Hämta ordning</span><span class="sxs-lookup"><span data-stu-id="27ffd-1071">Get the Order</span></span>
* <span data-ttu-id="27ffd-1072">Cmdleten `New-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1072">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="27ffd-1073">Skapa ny ordning</span><span class="sxs-lookup"><span data-stu-id="27ffd-1073">Create new Order</span></span>
* <span data-ttu-id="27ffd-1074">Cmdleten `Remove-AzDataBoxEdgeOrder` har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1074">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="27ffd-1075">Ta bort ordning</span><span class="sxs-lookup"><span data-stu-id="27ffd-1075">Remove the Order</span></span>
* <span data-ttu-id="27ffd-1076">Cmdleten `New-AzDataBoxEdgeShare` har ändrats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1076">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="27ffd-1077">Nu skapas lokal filresurs</span><span class="sxs-lookup"><span data-stu-id="27ffd-1077">Now creates Local Share</span></span>
* <span data-ttu-id="27ffd-1078">Cmdleten `Set-AzDataBoxEdgeRole` har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1078">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="27ffd-1079">Nu kan IotRole mappas till filresursen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1079">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="27ffd-1080">Cmdleten `Invoke-AzDataBoxEdgeDevice` har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1080">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="27ffd-1081">Anropa genomsökningsuppdatering, ladda ned uppdatering, installera uppdateringar på enheten</span><span class="sxs-lookup"><span data-stu-id="27ffd-1081">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="27ffd-1082">Cmdleten `Get-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1082">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="27ffd-1083">Hämtar information om utlösare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1083">Gets the information about Triggers</span></span>
* <span data-ttu-id="27ffd-1084">Cmdleten `New-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1084">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="27ffd-1085">Skapa nya utlösare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1085">Create new Triggers</span></span>
* <span data-ttu-id="27ffd-1086">Cmdleten `Remove-AzDataBoxEdgeTrigger` har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1086">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="27ffd-1087">Ta bort utlösare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1087">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-1088">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-1089">Uppdatera ADF .Net SDK-versionen till 4.4.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1089">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="27ffd-1090">Lägg till parametern ExpressCustomSetup för kommandot Set-AzureRmDataFactoryV2IntegrationRuntime för att aktivera installationskonfigurationer och komponenter från tredje part utan anpassat konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1090">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-1091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-1091">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-1092">Uppdatera dokumentation för Get-AzDataLakeStoreDeletedItem och Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="27ffd-1092">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27ffd-1093">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1093">Az.EventHub</span></span>
* <span data-ttu-id="27ffd-1094">Korrigering av problem #10301: Korrigera datumformat för SAS-token</span><span class="sxs-lookup"><span data-stu-id="27ffd-1094">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27ffd-1095">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1095">Az.FrontDoor</span></span>
* <span data-ttu-id="27ffd-1096">Lägg till parametern MinimumTlsVersion till Enable-AzFrontDoorCustomDomainHttps och New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="27ffd-1096">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="27ffd-1097">Lägg till parametrarna HealthProbeMethod och EnabledState till New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="27ffd-1097">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="27ffd-1098">Lägg till en ny cmdlet för att skapa BackendPoolsSettings-objekt som passar i skapande/uppdatering av Front Door</span><span class="sxs-lookup"><span data-stu-id="27ffd-1098">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="27ffd-1099">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="27ffd-1099">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1100">Az.Network</span></span>
* <span data-ttu-id="27ffd-1101">Ändra alternativexemplen Start-AzVirtualNetworkGatewayConnectionPacketCapture.md och Start-AzVirtualnetworkGatewayPacketCapture.md för FilterData.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1101">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="27ffd-1102">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="27ffd-1102">Az.PrivateDns</span></span>
* <span data-ttu-id="27ffd-1103">Uppdaterade PrivateDns .NET SDK till version 1.0.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1103">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-1104">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-1104">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-1105">Stöd för att välja disktyp vid aktivering av skydd i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1105">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="27ffd-1106">Korrigering av bugg för åtgärdsredigering av återställningsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1106">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="27ffd-1107">Återställningsstöd för att godkänna filestream-databaser i Azure Backup SQL.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1107">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27ffd-1108">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27ffd-1108">Az.RedisCache</span></span>
* <span data-ttu-id="27ffd-1109">Parametern MinimumTlsVersion har lagts till i cmdletarna New-AzRedisCache och Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1109">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="27ffd-1110">Dessutom har MinimumTlsVersion lagts till i utdata för cmdleten Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1110">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="27ffd-1111">Verifiering har lagts till på parametern -Size i cmdletarna Set-AzRedisCache och New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="27ffd-1111">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-1112">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-1112">Az.Resources</span></span>
- <span data-ttu-id="27ffd-1113">Uppdaterade policy-cmdletar för att använda den nya API-versionen 2019-06-01 som har en ny EnforcementMode-egenskap i policytilldelningen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1113">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="27ffd-1114">Uppdaterade hjälpexempel för skapandet av policydefinition</span><span class="sxs-lookup"><span data-stu-id="27ffd-1114">Updated create policy definition help example</span></span>
- <span data-ttu-id="27ffd-1115">Åtgärda bugg i Remove-AZADServicePrincipal -ServicePrincipalName, utlös null-referens när tjänstens huvudnamn inte hittas.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1115">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="27ffd-1116">Åtgärda bugg i New-AZADServicePrincipal, utlös null-referens när klientorganisationen inte har någon prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1116">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="27ffd-1117">Ändra New-AzAdServicePrincipal för att endast lägga till autentiseringsuppgifter för det associerade programmet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1117">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1118">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1118">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1119">Stöd har lagts till för databasen ReadReplicaCount.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1119">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="27ffd-1120">Korrigerade Set-AzSqlDatabase när zonredundans inte har angetts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1120">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="27ffd-1121">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1121">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="27ffd-1122">Allmänt</span><span class="sxs-lookup"><span data-stu-id="27ffd-1122">General</span></span>
* <span data-ttu-id="27ffd-1123">Az. PrivateDns 1.0.0 har släppts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1123">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1124">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-1125">Lägg till ett utfasningsmeddelande för aliaset Resolve-error.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1125">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="27ffd-1126">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1126">Az.Advisor</span></span>
* <span data-ttu-id="27ffd-1127">Den nya kategorin Operational Excellence har lagts till i cmdleten Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1127">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27ffd-1128">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27ffd-1128">Az.Batch</span></span>
* <span data-ttu-id="27ffd-1129">`CoreQuota` på `BatchAccountContext` har bytt namn till `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1129">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="27ffd-1130">Det finns även en ny `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1130">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="27ffd-1131">Detta påverkar **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1131">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="27ffd-1132">**New-AzBatchTask** `-ResourceFile`-parametern tar nu en samling `PSResourceFile`-objekt som kan skapas med hjälp av den nya cmdleten **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1132">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="27ffd-1133">Ny **New-AzBatchResourceFile**-cmdlet för att skapa `PSResourceFile`-objekt.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1133">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="27ffd-1134">Dessa kan tillhandahållas till **New-AzBatchTask** på `-ResourceFile`-parametern.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1134">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="27ffd-1135">Detta stöder två nya typer av resursfiler förutom det befintliga sättet med `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1135">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="27ffd-1136">`AutoStorageContainerName`-baserade resursfiler laddar ned en hel container för automatisk lagring till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1136">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="27ffd-1137">`StorageContainerUrl`-baserade resursfiler laddar ned containern som anges i webbadressen till Batch-noden.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1137">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="27ffd-1138">Tog bort egenskapen `ApplicationPackages` för `PSApplication` som returnerades av **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1138">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="27ffd-1139">Specifika paket i ett program kan nu hämtas med hjälp av **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1139">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="27ffd-1140">Till exempel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1140">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="27ffd-1141">Bytt namn på `ApplicationId` till `ApplicationName` på **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** och **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1141">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="27ffd-1142">`ApplicationId` är nu ett alias för `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1142">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="27ffd-1143">Ny `PSWindowsUserConfiguration`-egenskap till `PSUserAccount` lades till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1143">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="27ffd-1144">Bytte namn på `Version` till `Name` på `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1144">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="27ffd-1145">Bytte namn på `BlobSource` till `HttpUrl` på `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1145">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="27ffd-1146">Tog bort egenskapen `OSDisk` från `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1146">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="27ffd-1147">Tog bort **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1147">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="27ffd-1148">Den här åtgärden stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1148">This operation is no longer supported.</span></span>
* <span data-ttu-id="27ffd-1149">`TargetOSVersion` har tagits bort från `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1149">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="27ffd-1150">Bytte namn på `CurrentOSVersion` till `OSVersion` på `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1150">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="27ffd-1151">`DataEgressGiB` och `DataIngressGiB` har tagits bort från `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1151">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="27ffd-1152">Tog bort **Get-AzBatchNodeAgentSku** och ersatte det med **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1152">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="27ffd-1153">**Get-AzBatchSupportedImage** returnerar samma data som **Get-AzBatchNodeAgentSku** men i ett mer användarvänligt format.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1153">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="27ffd-1154">Nya icke-verifierade avbildningar returneras nu också.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1154">New non-verified images are also now returned.</span></span> <span data-ttu-id="27ffd-1155">Ytterligare information om `Capabilities` och `BatchSupportEndOfLife` för varje avbildning inkluderas också.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1155">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="27ffd-1156">Lade till möjlighet att montera fjärrfilsystem på varje nod i en pool via den nya parametern `MountConfiguration` för **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1156">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="27ffd-1157">Har nu stöd för nätverkssäkerhetsregler som blockerar nätverksåtkomst till en pool baserat på källportens trafik.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1157">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="27ffd-1158">Detta görs via egenskapen `SourcePortRanges` på `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1158">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="27ffd-1159">När du kör en container stöder nu Batch körningen av uppgiften i arbetskatalogen för containern eller i arbetskatalogen för Batch-uppgiften.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1159">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="27ffd-1160">Detta styrs av egenskapen `WorkingDirectory` på `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1160">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="27ffd-1161">Lade till en funktion för att ange en samling av offentliga IP-adresser på `PSNetworkConfiguration` via den nya egenskapen `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1161">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="27ffd-1162">Detta garanterar att noderna i poolen har en IP-adress från listan över IP-adresser som tillhandahållits av användare.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1162">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="27ffd-1163">Om inget värde anges är standardvärdet för `WaitForSuccess` på `PSSTartTask` nu `$True` (var tidigare `$False`).</span><span class="sxs-lookup"><span data-stu-id="27ffd-1163">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="27ffd-1164">Om inget värde anges är standardvärdet för `Scope` på `PSAutoUserSpecification` nu `Pool` (var tidigare `Task` på Windows och `Pool` på Linux).</span><span class="sxs-lookup"><span data-stu-id="27ffd-1164">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27ffd-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27ffd-1165">Az.Cdn</span></span>
* <span data-ttu-id="27ffd-1166">Introducerade UrlRewriteAction och CacheKeyQueryStringAction till RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1166">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="27ffd-1167">Åtgärdade flera buggar, som saknade indata för ”väljare” i cmdleten New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1167">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1168">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1169">Funktion för diskkrypteringsuppsättning</span><span class="sxs-lookup"><span data-stu-id="27ffd-1169">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="27ffd-1170">Nya cmdletar:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1170">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="27ffd-1171">Parametern DiskEncryptionSetId har lagts till i följande cmdletar:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="27ffd-1171">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="27ffd-1172">Parametrarna DiskEncryptionSetId och EncryptionType har lagts till i följande cmdletar:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1172">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="27ffd-1173">Lägg till parametern PublicIPAddressVersion i New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1173">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="27ffd-1174">Flytta FileUris för anpassat skripttillägg från offentlig inställning till skyddad inställning</span><span class="sxs-lookup"><span data-stu-id="27ffd-1174">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="27ffd-1175">Lägg till ScaleInPolicy i cmdletarna New-AzVmss, New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27ffd-1175">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="27ffd-1176">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1176">Breaking changes</span></span>
    - <span data-ttu-id="27ffd-1177">Parametern UploadSizeInBytes används istället för DiskSizeGB för New-AzDiskConfig när CreateOption är Uppladdning</span><span class="sxs-lookup"><span data-stu-id="27ffd-1177">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="27ffd-1178">PublishingProfile.Source.ManagedImage.Id ersätts med StorageProfile.Source.Id i objektet GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="27ffd-1178">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-1179">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-1179">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-1180">Uppdatera ADF .Net SDK-versionen till 4.3.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1180">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-1181">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-1181">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-1182">Uppdatera ADLS SDK-version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) innehåller följande korrigeringar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1182">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="27ffd-1183">Undvik att utlösa undantag när det inte går att deserialisera creationtime för inmatning av papperskorg eller katalog.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1183">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="27ffd-1184">Gör inställning tillgänglig per tidsgräns för förfrågan i adlsclient</span><span class="sxs-lookup"><span data-stu-id="27ffd-1184">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="27ffd-1185">Korrigera överföringen av ursprunglig syncflag för badoffset-återställning</span><span class="sxs-lookup"><span data-stu-id="27ffd-1185">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="27ffd-1186">Korrigera EnumerateDirectory för att hämta fortsättningstoken när svar har kontrollerats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1186">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="27ffd-1187">Korrigera bugg i Concat</span><span class="sxs-lookup"><span data-stu-id="27ffd-1187">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27ffd-1188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1188">Az.FrontDoor</span></span>
* <span data-ttu-id="27ffd-1189">Åtgärdade diverse stavfel i modul</span><span class="sxs-lookup"><span data-stu-id="27ffd-1189">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-1190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-1190">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-1191">Korrigerade buggen att kunder får felet ”inte en giltig Base-64-sträng” vid användning av Get-AzHDInsightCluster för att hämta klustret med ADLSGen1-lagring.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1191">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="27ffd-1192">Lägg till en parameter med namnet ”ApplicationId” i de tre cmdletarna Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig och New-AzHDInsightCluster så att kunden kan tillhandahålla tjänstens huvudnamn för program-ID för åtkomst till Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1192">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="27ffd-1193">Ändrade Microsoft.Azure.Management.HDInsight från 2.1.0 till 5.1.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1193">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="27ffd-1194">Fem cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1194">Removed five cmdlets:</span></span>
    - <span data-ttu-id="27ffd-1195">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="27ffd-1195">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="27ffd-1196">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="27ffd-1196">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="27ffd-1197">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="27ffd-1197">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="27ffd-1198">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27ffd-1198">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="27ffd-1199">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27ffd-1199">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="27ffd-1200">Tre cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1200">Added three cmdlets:</span></span>
    - <span data-ttu-id="27ffd-1201">Get-AzHDInsightMonitoring som ersätter Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1201">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="27ffd-1202">Enable-AzHDInsightMonitoring som ersätter Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1202">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="27ffd-1203">Disable-AzHDInsightMonitoring som ersätter Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1203">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="27ffd-1204">Korrigerade cmdleten Get-AzHDInsightProperties för att stödja hämtning av funktionsinformation från en viss plats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1204">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="27ffd-1205">Parameteruppsättningarna (Spark1 och Spark2) har tagits bort från Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1205">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="27ffd-1206">Lägg till exempel för cmdleten Add-AzHDInsightSecurityProfile till hjälpdokumenten.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1206">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="27ffd-1207">Ändrade utdatatyp för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1207">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="27ffd-1208">Ändrade utdatatyp för Get-AzHDInsightProperties från CapabilitiesResponse till AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1208">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="27ffd-1209">Ändrade utdatatyp för Remove-AzHDInsightCluster från ClusterGetResponse till bool.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1209">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="27ffd-1210">Ändrade utdatatyp för Set-AzHDInsightGatewaySettings HttpConnectivitySettings till GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1210">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="27ffd-1211">Lade till testfall för vissa scenarier.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1211">Added some scenario test cases.</span></span>
* <span data-ttu-id="27ffd-1212">Ta bort vissa alias: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1212">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-1213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1213">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-1214">Icke-bakåtkompatibla ändringar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1214">Breaking changes:</span></span>
    - <span data-ttu-id="27ffd-1215">Cmdleten Add-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1215">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27ffd-1216">Parameteruppsättningen __AllParameterSets för cmdleten Add-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1216">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="27ffd-1217">Cmdleten Get-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1217">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27ffd-1218">Parameteruppsättningen __AllParameterSets för cmdleten Get-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1218">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="27ffd-1219">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1219">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="27ffd-1220">Egenskapen OperationsMonitoringProperties av typen Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1220">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="27ffd-1221">Cmdleten New-AzIotHubExportDevice stöder inte längre aliaset New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1221">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="27ffd-1222">Cmdleten New-AzIotHubImportDevice stöder inte längre aliaset New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1222">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="27ffd-1223">Cmdleten Remove-AzIotHubEventHubConsumerGroup har inte längre stöd för parametern EventHubEndpointName och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1223">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27ffd-1224">Parameteruppsättningen __AllParameterSets för cmdleten Remove-AzIotHubEventHubConsumerGroup har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1224">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="27ffd-1225">Cmdleten Set-AzIotHub har inte längre stöd för parametern OperationsMonitoringProperties och inget alias hittades för det ursprungliga parameternamnet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1225">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27ffd-1226">Parameteruppsättningen UpdateOperationsMonitoringProperties för cmdleten Set-AzIotHub har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1226">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-1227">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-1227">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-1228">Azure Site Recovery-stöd för att konfigurera nätverksresurser som NSG, offentliga IP-adresser och interna lastbalanserare för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1228">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="27ffd-1229">Azure Site Recovery-stöd för att skriva till hanterad disk för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1229">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="27ffd-1230">Azure Site Recovery-stöd för NIC-reduktion för vMWare till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1230">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="27ffd-1231">Azure Site Recovery-stöd för accelererat nätverk för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1231">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="27ffd-1232">Azure Site Recovery-stöd för automatisk uppdatering av agent för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1232">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="27ffd-1233">Azure Site Recovery-stöd för Standard SSD för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1233">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="27ffd-1234">Azure Site Recovery-stöd för tvåstegskryptering i Azure Disk Encryption för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1234">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="27ffd-1235">Azure Site Recovery-stöd för att skydda nyligen tillagda diskar för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1235">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="27ffd-1236">En funktion för mjuk borttagning av virtuella datorer samt tester för mjuk borttagning har tagits bort</span><span class="sxs-lookup"><span data-stu-id="27ffd-1236">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-1237">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-1237">Az.Resources</span></span>
* <span data-ttu-id="27ffd-1238">Uppdatera beroendesammansättning för Microsoft.Extensions.Caching.Memory från 1.1.1 till 2.2</span><span class="sxs-lookup"><span data-stu-id="27ffd-1238">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1239">Az.Network</span></span>
* <span data-ttu-id="27ffd-1240">Ändra alla cmdletar för PrivateEndpointConnection så att de stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1240">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="27ffd-1241">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1241">Updated cmdlet:</span></span>
        - <span data-ttu-id="27ffd-1242">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1242">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27ffd-1243">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1243">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27ffd-1244">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1244">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27ffd-1245">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1245">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27ffd-1246">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1246">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="27ffd-1247">Lägg till ny cmdlet för PrivateLinkResource så att det också stöder generiska tjänstleverantörer.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1247">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="27ffd-1248">Ny cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1248">New cmdlet:</span></span>
        - <span data-ttu-id="27ffd-1249">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="27ffd-1249">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="27ffd-1250">Lägg till nya fält och parametrar för funktionen Proxy Protocol V2.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1250">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="27ffd-1251">Lägg till egenskapen EnableProxyProtocol i PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27ffd-1251">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="27ffd-1252">Lägg till egenskapen LinkIdentifier i PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1252">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="27ffd-1253">Uppdaterade New-AzPrivateLinkService för att lägga till den nya valfria parametern EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1253">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="27ffd-1254">Korrigera felaktig beskrivning av parameter i referensdokumentationen för New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="27ffd-1254">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="27ffd-1255">Nya cmdletar som stöder Azure-brandväggsprincipen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1255">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="27ffd-1256">Lägg till stöd för den underordnade resursen RouteTables för VirtualHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1256">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="27ffd-1257">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1257">New cmdlets added:</span></span>
        - <span data-ttu-id="27ffd-1258">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1258">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="27ffd-1259">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="27ffd-1259">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="27ffd-1260">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="27ffd-1260">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="27ffd-1261">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="27ffd-1261">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="27ffd-1262">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1262">Set-AzVirtualHub</span></span>
* <span data-ttu-id="27ffd-1263">Lägg till stöd för ny egenskaps-SKU för VirtualHub och VirtualWANType för VirtualWan</span><span class="sxs-lookup"><span data-stu-id="27ffd-1263">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="27ffd-1264">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1264">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27ffd-1265">New-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="27ffd-1265">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="27ffd-1266">Update-AzVirtualHub: lade till parameter-SKU</span><span class="sxs-lookup"><span data-stu-id="27ffd-1266">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="27ffd-1267">New-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="27ffd-1267">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="27ffd-1268">Update-AzVirtualWan: lade till parametern VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="27ffd-1268">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="27ffd-1269">Lägg till stöd för egenskapen EnableInternetSecurity för HubVnetConnection, VpnConnection och ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1269">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="27ffd-1270">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1270">New cmdlets added:</span></span>
        - <span data-ttu-id="27ffd-1271">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1271">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="27ffd-1272">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1272">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27ffd-1273">New-AzureRmVirtualHubVnetConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1273">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27ffd-1274">New-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1274">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27ffd-1275">Update-AzureRmVpnConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1275">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27ffd-1276">New-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1276">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27ffd-1277">Set-AzureRmExpressRouteConnection: parametern EnableInternetSecurity har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1277">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="27ffd-1278">Lägg till stöd för att konfigurera TopLevel WebApplicationFirewall-princip</span><span class="sxs-lookup"><span data-stu-id="27ffd-1278">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="27ffd-1279">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1279">New cmdlets added:</span></span>
        - <span data-ttu-id="27ffd-1280">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="27ffd-1280">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="27ffd-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="27ffd-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="27ffd-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="27ffd-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="27ffd-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="27ffd-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="27ffd-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="27ffd-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="27ffd-1286">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1286">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27ffd-1287">New-AzApplicationGatewayFirewallPolicy: parametrarna PolicySetting, ManagedRule har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1287">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="27ffd-1288">Stöd för operator för geomatchning har lagts till på CustomRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-1288">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="27ffd-1289">Geomatchning har lagts till i operatorn på FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="27ffd-1289">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="27ffd-1290">Stöd har lagts till för brandväggsprinciperna perListener och perSite</span><span class="sxs-lookup"><span data-stu-id="27ffd-1290">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="27ffd-1291">Cmdletar har uppdaterats med valfria parametrar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1291">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27ffd-1292">New-AzApplicationGatewayHttpListener: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1292">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="27ffd-1293">New-AzApplicationGatewayPathRuleConfig: parametrarna FirewallPolicy, FirewallPolicyId har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1293">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="27ffd-1294">Åtgärdat så att nödvändigt undernät med namnet AzureBastionSubnet i PSBastion kan vara skiftlägesokänsligt</span><span class="sxs-lookup"><span data-stu-id="27ffd-1294">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="27ffd-1295">Stöd för mål-FQDN:er i nätverksregler och översatt FQDN i NAT-regler för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="27ffd-1295">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="27ffd-1296">Lägg till stöd för resursen RouteTables för IpGroup på den högsta nivån</span><span class="sxs-lookup"><span data-stu-id="27ffd-1296">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="27ffd-1297">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1297">New cmdlets added:</span></span>
        - <span data-ttu-id="27ffd-1298">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-1298">New-AzIpGroup</span></span>
        - <span data-ttu-id="27ffd-1299">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-1299">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="27ffd-1300">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-1300">Get-AzIpGroup</span></span>
        - <span data-ttu-id="27ffd-1301">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-1301">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27ffd-1302">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-1302">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-1303">Ta bort cmdleten Add-AzServiceFabricApplicationCertificate eftersom det här scenariot omfattas av Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1303">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1304">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1305">Stöd har lagts till för återställning av utelämnade databaser på hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1305">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="27ffd-1306">Inaktuella gamla cmdletar för granskning från kod.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1306">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="27ffd-1307">Tog bort inaktuella alias:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1307">Removed deprecated aliases:</span></span>
* <span data-ttu-id="27ffd-1308">Get-AzSqlDatabaseIndexRecommendations (använd Get-AzSqlDatabaseIndexRecommendation istället)</span><span class="sxs-lookup"><span data-stu-id="27ffd-1308">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="27ffd-1309">Get-AzSqlDatabaseRestorePoints (använd Get-AzSqlDatabaseRestorePoint istället)</span><span class="sxs-lookup"><span data-stu-id="27ffd-1309">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="27ffd-1310">Ta bort cmdleten Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-1310">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="27ffd-1311">Ta bort alias för inaktuella cmdletar för inställningar för utvärdering av säkerhetsrisk</span><span class="sxs-lookup"><span data-stu-id="27ffd-1311">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="27ffd-1312">Inaktualisera cmdletar för inställningar för avancerad hotidentifiering</span><span class="sxs-lookup"><span data-stu-id="27ffd-1312">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="27ffd-1313">Lägga till cmdletar för att inaktivera och aktivera känslighetsrekommendationer på kolumner i en databas.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1313">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-1314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-1314">Az.Storage</span></span>
* <span data-ttu-id="27ffd-1315">Stöd för att aktivera stora filresurser vid skapande eller uppdatering av lagringskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-1315">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="27ffd-1316">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-1316">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="27ffd-1317">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-1317">Set-AzStorageAccount</span></span>
* <span data-ttu-id="27ffd-1318">När du stänger/hämtar en filreferens kan du hoppa över kontrollen av huruvida indatasökvägen är en filkatalog eller en fil för att undvika problem med objekt som har status DeletePending</span><span class="sxs-lookup"><span data-stu-id="27ffd-1318">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="27ffd-1319">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27ffd-1319">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="27ffd-1320">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27ffd-1320">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="27ffd-1321">2.8.0 – oktober 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1321">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="27ffd-1322">Allmänt</span><span class="sxs-lookup"><span data-stu-id="27ffd-1322">General</span></span>
* <span data-ttu-id="27ffd-1323">AZ. HealthcareApis 1.0.0-version</span><span class="sxs-lookup"><span data-stu-id="27ffd-1323">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-1324">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1324">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-1325">Uppdatera telemetri och URL-omskrivning för genererade moduler, korrigera Windows-enhetstester.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1325">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-1326">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-1326">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-1327">**Set-AzApiManagementApi** – Tillagt stöd för att uppdatera Api till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1327">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="27ffd-1328">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="27ffd-1328">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-1329">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-1329">Az.Automation</span></span>
* <span data-ttu-id="27ffd-1330">Åtgärdade cmdleten New-AzureAutomationSoftwareUpdateConfiguration för parametern för inställning av Linux-omstart.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1330">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27ffd-1331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27ffd-1331">Az.Batch</span></span>
* <span data-ttu-id="27ffd-1332">**Get-AzBatchNodeAgentSku** är inaktuell och ersätts av **Get-AzBatchSupportImage** i version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1332">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1333">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1333">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1334">Lägg till parametrarna Priority, EvictionPolicy och MaxPrice till cmdletarna New-AzVM och New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27ffd-1334">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="27ffd-1335">Korrigera varningsmeddelande och hjälpdokument för cmdletarna Add-AzVMAdditionalUnattendContent och Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="27ffd-1335">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="27ffd-1336">Åtgärda – skipVmBackup-undantag för virtuella Linux-datorer med hanterade diskar för Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1336">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="27ffd-1337">Åtgärda fel i uppdatera krypteringsinställningarna i set-AzVMDiskEncryptionExtension, scenario i två steg.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1337">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-1338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-1338">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-1339">Lägga till CRUD-kommandon för ADF V2-dataflödet: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow och Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1339">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="27ffd-1340">Lägger till åtgärdskommandon för ADF V2-dataflödesfelsökningssession: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand och Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1340">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="27ffd-1341">Uppdatera ADF .Net SDK-versionen till 4.2.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1341">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-1343">Korrigera kontovalidering så att konton med ”-” kan skickas utan domän</span><span class="sxs-lookup"><span data-stu-id="27ffd-1343">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27ffd-1344">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27ffd-1344">Az.HealthcareApis</span></span>
* <span data-ttu-id="27ffd-1345">PowerShell-versionen har uppdaterats till 1.0.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1345">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="27ffd-1346">Uppdaterade SDK-versionen till 1.0.2</span><span class="sxs-lookup"><span data-stu-id="27ffd-1346">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="27ffd-1347">Uppdatera i tester för att referera till en ny SDK-version</span><span class="sxs-lookup"><span data-stu-id="27ffd-1347">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="27ffd-1348">Utdatastrukturen har uppdaterats från kapslad till förenklad.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1348">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-1349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1349">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-1350">Lägg till ny routningskälla: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="27ffd-1350">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="27ffd-1351">Mindre felkorrigering: Get-AzIothub returnerar inte subscriptionId</span><span class="sxs-lookup"><span data-stu-id="27ffd-1351">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-1352">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1352">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-1353">Nya åtgärdsgruppsmottagare har lagts till för åtgärdsgrupp   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="27ffd-1353">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="27ffd-1354">Använd vanligt aviseringsschema som är aktiverat för mottagarna.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1354">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="27ffd-1355">Detta gäller inte för SMS, push för Azure-app, ITSM och röstmottagare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1355">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="27ffd-1356">Webhooks har nu stöd för Azure Active Directory-autentisering.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1356">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1357">Az.Network</span></span>
* <span data-ttu-id="27ffd-1358">Lägg till ny cmdlet Get-AzAvailableServiceAlias som kan anropas för att hämta de alias som kan användas för tjänstslutpunktsprinciper.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1358">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="27ffd-1359">Stöd för tillägg av trafikväljare har lagts till i gatewayanslutningar för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="27ffd-1359">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="27ffd-1360">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1360">New cmdlets added:</span></span>
        - <span data-ttu-id="27ffd-1361">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-1361">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="27ffd-1362">Cmdletar har uppdaterats med valfri parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1362">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="27ffd-1363">Lägg till stöd för ESP- och AH-protokoll i konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="27ffd-1363">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="27ffd-1364">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1364">Updated cmdlets:</span></span>
        - <span data-ttu-id="27ffd-1365">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1365">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27ffd-1366">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1366">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27ffd-1367">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1367">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="27ffd-1368">Förbättra hanteringen av undantag i Cortex-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1368">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="27ffd-1369">Nya generationer och SKU:er för VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="27ffd-1369">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="27ffd-1370">Introducera nya generationer för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1370">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="27ffd-1371">Introducera nya SKU:er med högt dataflöde för VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1371">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27ffd-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27ffd-1372">Az.RedisCache</span></span>
* <span data-ttu-id="27ffd-1373">Uppdaterad referensdokumentation för ”set-AzRedisCache” för att inkludera saknade värden för parametern ”size”</span><span class="sxs-lookup"><span data-stu-id="27ffd-1373">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1374">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1375">Lägg till stöd för inställningen Active Directory administratör på den hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1375">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-1376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-1376">Az.Storage</span></span>
* <span data-ttu-id="27ffd-1377">Uppdatera Lagringsklientbibliotek till 11.1.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1377">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="27ffd-1378">Lista containrar med hanteringsplans-API, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="27ffd-1378">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="27ffd-1379">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="27ffd-1379">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="27ffd-1380">Lista lagringskonton från prenumerationen, kommer att listas med NextPageLink</span><span class="sxs-lookup"><span data-stu-id="27ffd-1380">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="27ffd-1381">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-1381">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27ffd-1382">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27ffd-1382">Az.StorageSync</span></span>
* <span data-ttu-id="27ffd-1383">Åtgärda problemet 9810 i Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1383">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-1384">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-1384">Az.Websites</span></span>
* <span data-ttu-id="27ffd-1385">Set-AzWebApp – uppdatering av ASP för en app misslyckades</span><span class="sxs-lookup"><span data-stu-id="27ffd-1385">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="27ffd-1386">2.7.0 – september 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1386">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-1387">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-1387">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-1388">Uppdatera ”-Format”-parameterbeskrivningen i ”Set-AzApiManagementPolicy”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1388">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="27ffd-1389">Referenser för den föråldrade cmdleten ”Update-AzApiManagementDeployment” har tagits bort från referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1389">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="27ffd-1390">Använd ”Set-AzApiManagement” i stället.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1390">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-1391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-1391">Az.Automation</span></span>
* <span data-ttu-id="27ffd-1392">Stavfel har korrigerats i exempel i referensdokumentationen för ”Register-AzAutomationDscNode”</span><span class="sxs-lookup"><span data-stu-id="27ffd-1392">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="27ffd-1393">Klargörande har lagts till om OS-begränsningar för Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="27ffd-1393">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="27ffd-1394">Null-referensundantag har korrigerats för -Wait-alternativet i Start-AzAutomationRunbook-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1394">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1395">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1396">Lägg till UploadSizeInBytes-parameter till New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1396">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="27ffd-1397">Lägg till Incremental-parameter till New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1397">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="27ffd-1398">Lägg till en funktion för virtuella datorer med låg prioritet:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1398">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="27ffd-1399">MaxPrice-, EvictionPolicy- och Priority-parametrar har lagts till i New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1399">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="27ffd-1400">MaxPrice-parametern har lagts till i New-AzVmssConfig-, Update-AzVM- och Update-AzVmss-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1400">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="27ffd-1401">Åtgärda problem med VM-referenser för Get-AzAvailabilitySet-cmdleten när alla tillgänglighetsuppsättningar i prenumerationen visas.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1401">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="27ffd-1402">Korrigera null-undantaget för Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1402">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="27ffd-1403">Korrigera VHD-metoden för sökning relativt till slut.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1403">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="27ffd-1404">Åtgärda UltraSSD-problem för New-AzVM och Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1404">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-1405">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-1405">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-1406">Lägger till 3 nya kommandon för ADF V2 – Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription och Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="27ffd-1406">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="27ffd-1407">ADF .Net SDK har uppdaterats till 4.1.3</span><span class="sxs-lookup"><span data-stu-id="27ffd-1407">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-1408">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-1408">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-1409">Anrop för icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1409">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-1410">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1410">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-1411">Lägg till stöd för att anropa redundans för en IotHub till den geo-länkade katastrofåterställningsregionen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1411">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="27ffd-1412">Lägg till stöd för att hantera meddelandeberikning för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1412">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="27ffd-1413">Nya cmdlet:ar är:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1413">New cmdlets are:</span></span>
    - <span data-ttu-id="27ffd-1414">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="27ffd-1414">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="27ffd-1415">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="27ffd-1415">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="27ffd-1416">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="27ffd-1416">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="27ffd-1417">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="27ffd-1417">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-1418">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1418">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-1419">Pekar på den senaste Monitor SDK:n, dvs. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="27ffd-1419">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="27ffd-1420">Lägger till bakåtkompatibla ändringar i Metrics-cmdletarna, dvs. enhetsuppräkningen stöder flera nya värden.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1420">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="27ffd-1421">Detta är skrivskyddade cmdletar, så det förekommer inga ändringar i inmatningen för cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1421">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="27ffd-1422">API-versionen för **ActionGroups**-begäranden är nu **2019-06-01**. Tidigare var den **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1422">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="27ffd-1423">Test av scenarier har uppdaterats för att anpassas till den här ändringen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1423">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="27ffd-1424">Ett nytt obligatoriskt argument har lagts till för konstruktorerna för klasserna **EmailReceiver** och **WebhookReceiver** – ett booleskt värde med namnet **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1424">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="27ffd-1425">Värdet är för närvarande fast till **false** så att den här icke-bakåtkompatibla ändringen är dold från cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1425">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="27ffd-1426">**Obs!** Det här är en tillfällig ändring som måste verifieras av Alerts-teamet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1426">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="27ffd-1427">Ordningen på argumenten för konstruktorn för klassen **Source** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1427">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="27ffd-1428">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1428">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="27ffd-1429">Ordningen på argumenten för konstruktorn för klassen **AlertingAction** (relaterad till klassen **ScheduledQueryRuleSource**) har ändrats från den tidigare SDK:n.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1429">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="27ffd-1430">Den här ändringen krävde korrigering av två enhetstest: de kompilerades, men testerna skickades inte.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1430">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="27ffd-1431">Stöd för kriterier för dynamiskt tröskelvärde för måttavisering v2</span><span class="sxs-lookup"><span data-stu-id="27ffd-1431">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="27ffd-1432">New-AzMetricAlertRuleV2Criteria: skapar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="27ffd-1432">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="27ffd-1433">Add-AzMetricAlertRuleV2: accepterar nu även kriterier för dynamiskt tröskelvärde</span><span class="sxs-lookup"><span data-stu-id="27ffd-1433">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="27ffd-1434">Förbättringar i schemalagd frågeregel (SQR)</span><span class="sxs-lookup"><span data-stu-id="27ffd-1434">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="27ffd-1435">Cmdletar accepterar ”Location”-parameter i båda formaten, antingen platsen (t.ex. eastus) eller platsens visningsnamn (t.ex. USA, östra)</span><span class="sxs-lookup"><span data-stu-id="27ffd-1435">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="27ffd-1436">”Enabled”-parametern illustreras korrekt i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="27ffd-1436">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="27ffd-1437">Exempel för den valfria parametern ”ActionGroup” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1437">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="27ffd-1438">Förbättrade hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="27ffd-1438">Overall improved help files</span></span>
* <span data-ttu-id="27ffd-1439">Åtgärda bugg då omfattningstypen fastställs för ”Set-AzActionRule”</span><span class="sxs-lookup"><span data-stu-id="27ffd-1439">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1440">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1440">Az.Network</span></span>
* <span data-ttu-id="27ffd-1441">Korrigera felaktigt exempel i referensdokumentationen för ”New-AzApplicationGateway”</span><span class="sxs-lookup"><span data-stu-id="27ffd-1441">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="27ffd-1442">Lägg till anmärkning i ”Get-AzNetworkWatcherPacketCapture”-referensdokumentationen om hämtning av alla egenskaper för en paketinsamling</span><span class="sxs-lookup"><span data-stu-id="27ffd-1442">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="27ffd-1443">Exempel har korrigerats i ”Test-AzNetworkWatcherIPFlow”-referensdokumentationen för korrekt uppräkning av nätverkskort</span><span class="sxs-lookup"><span data-stu-id="27ffd-1443">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="27ffd-1444">Förbättrad tolkning av molnundantag för att visa eventuell ytterligare information</span><span class="sxs-lookup"><span data-stu-id="27ffd-1444">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="27ffd-1445">Förbättrad tolkning av molnundantag för att hantera ytterligare en typ av SDK-undantag</span><span class="sxs-lookup"><span data-stu-id="27ffd-1445">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="27ffd-1446">Felaktig mappning av säkerhetsregelmodeller har korrigerats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1446">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="27ffd-1447">Egenskaper har lagts till för nätverksgränssnittet för funktionen Privat IP</span><span class="sxs-lookup"><span data-stu-id="27ffd-1447">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="27ffd-1448">Egenskapen ”PrivateEndpoint” har lagts till som en typ av PSResourceId till PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="27ffd-1448">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="27ffd-1449">Egenskapen ”PrivateLinkConnectionProperties” har lagts till som en typ av PSIpConfigurationConnectivityInformation till PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-1449">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="27ffd-1450">Modellklassen PSIpConfigurationConnectivityInformation har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1450">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="27ffd-1451">ApplicationRuleProtocolType ”mssql” har lagts till för Azure Firewall-resurs</span><span class="sxs-lookup"><span data-stu-id="27ffd-1451">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="27ffd-1452">MultiLink-stöd i virtuellt WAN</span><span class="sxs-lookup"><span data-stu-id="27ffd-1452">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="27ffd-1453">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1453">New cmdlets</span></span>
        - <span data-ttu-id="27ffd-1454">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="27ffd-1454">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="27ffd-1455">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1455">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="27ffd-1456">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1456">Updated cmdlet:</span></span>
        - <span data-ttu-id="27ffd-1457">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="27ffd-1457">New-VpnSite</span></span>
        - <span data-ttu-id="27ffd-1458">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="27ffd-1458">Update-VpnSite</span></span>
        - <span data-ttu-id="27ffd-1459">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1459">New-VpnConnection</span></span>
        - <span data-ttu-id="27ffd-1460">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1460">Update-VpnConnection</span></span>
* <span data-ttu-id="27ffd-1461">Dokument för vissa PowerShell-exempel har korrigerats så att Az-cmdletar används i stället för AzureRM-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1461">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-1463">Uppdatera AzureVMpolicy-objekt med ProtectedItemsCount-attribut</span><span class="sxs-lookup"><span data-stu-id="27ffd-1463">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="27ffd-1464">Ytterligare tester har lagts till för VM-princip och återställning av ursprungligt lagringskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-1464">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-1465">Az.Resources</span></span>
* <span data-ttu-id="27ffd-1466">Åtgärda fel där det inte gick att anropa New-AzRoleAssignment utan parametern Scope.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1466">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27ffd-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-1468">Stavfel har korrigerats i exempel för ”Update-AzServiceFabricReliability”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1468">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="27ffd-1469">Lägger till nya cmdletar för att hantera program och tjänster:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1469">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="27ffd-1470">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="27ffd-1470">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27ffd-1471">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="27ffd-1471">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="27ffd-1472">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="27ffd-1472">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="27ffd-1473">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="27ffd-1473">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="27ffd-1474">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="27ffd-1474">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27ffd-1475">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="27ffd-1475">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27ffd-1476">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="27ffd-1476">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="27ffd-1477">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="27ffd-1477">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="27ffd-1478">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="27ffd-1478">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="27ffd-1479">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="27ffd-1479">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27ffd-1480">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="27ffd-1480">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="27ffd-1481">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="27ffd-1481">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="27ffd-1482">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="27ffd-1482">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="27ffd-1483">Service Fabric SDK har uppgraderats till version 1.2.0 som använder Service Fabric-resursprovidern med API-version 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1483">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="27ffd-1484">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="27ffd-1484">Az.SignalR</span></span>
* <span data-ttu-id="27ffd-1485">Lägg till Update-, Restart-, CheckNameAvailability- och GetUsage-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1485">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1486">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1487">Uppdatera exempel i referensdokumentationen för ”Get-AzSqlElasticPool”</span><span class="sxs-lookup"><span data-stu-id="27ffd-1487">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="27ffd-1488">vCore-exempel för att skapa en elastisk pool (New-AzSqlElasticPool) har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1488">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="27ffd-1489">Ta bort verifieringen av EmailAddresses och kontrollen som bekräftar att EmailAdmins inte är falskt när EmailAddresses är tomt i Set-AzSqlServerAdvancedThreatProtectionPolicy och Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-1489">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="27ffd-1490">Server-/databasgranskningsinställningar kan tas bort när det finns flera diagnostikinställningar som aktiverar granskningskategorin.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1490">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="27ffd-1491">Åtgärda verifiering av e-postadresser i flera Sql Vulnerability Assessment-cmdletar (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting och Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="27ffd-1491">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-1492">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-1492">Az.Storage</span></span>
* <span data-ttu-id="27ffd-1493">Exempel i referensdokumentationen för ”Get-AzStorageAccountKey” har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1493">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="27ffd-1494">Vid upp- och nedladdning av en Azure-fil kan SMB-egenskaperna för källfilen (t.ex. filattribut, tidpunkten då filen skapades och tidpunkten för den senaste skrivningen) sparas i målfilen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1494">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="27ffd-1495">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27ffd-1495">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="27ffd-1496">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27ffd-1496">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="27ffd-1497">Korrigera problem med uppladdningen av blockblob med egenskaper/metadata för ImmutabilityPolicy i containrar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1497">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="27ffd-1498">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27ffd-1498">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="27ffd-1499">Stöd för hantering av Azure-filresurser med API för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="27ffd-1499">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="27ffd-1500">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1500">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="27ffd-1501">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1501">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="27ffd-1502">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1502">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="27ffd-1503">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27ffd-1503">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-1504">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-1504">Az.Websites</span></span>
* <span data-ttu-id="27ffd-1505">Åtgärdar problemet där webapp-taggar togs bort när appen migrerades till nya ASP</span><span class="sxs-lookup"><span data-stu-id="27ffd-1505">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="27ffd-1506">Åtgärda Publish-AzureWebapp så att det fungerar i Linux och Windows</span><span class="sxs-lookup"><span data-stu-id="27ffd-1506">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="27ffd-1507">Uppdatera exempel i ”Get-AzWebAppPublishingProfile”-referensdokumentationen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1507">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="27ffd-1508">2.6.0 – augusti 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1508">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="27ffd-1509">Allmänt</span><span class="sxs-lookup"><span data-stu-id="27ffd-1509">General</span></span>
* <span data-ttu-id="27ffd-1510">Åtgärdade diverse skrivfel i flera moduler</span><span class="sxs-lookup"><span data-stu-id="27ffd-1510">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-1511">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1511">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-1512">Stöd för användartilldelat MSI i Azure Functions-autentisering (#9479)</span><span class="sxs-lookup"><span data-stu-id="27ffd-1512">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="27ffd-1513">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27ffd-1513">Az.Aks</span></span>
* <span data-ttu-id="27ffd-1514">Åtgärda problem med utdata för "Get-AzAks"</span><span class="sxs-lookup"><span data-stu-id="27ffd-1514">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="27ffd-1515">Mer information här: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="27ffd-1515">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-1516">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-1516">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-1517">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="27ffd-1517">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="27ffd-1518">Uppdatera .net-NuGet-versionen, som inte tillämpar begränsningar för productId, apiId och userId</span><span class="sxs-lookup"><span data-stu-id="27ffd-1518">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="27ffd-1519">**Get-AzApiManagementProduct** – Lade till stöd för frågekörning mot produkter via API.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1519">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="27ffd-1520">**New-AzApiManagementApiRevision** – Korrigering för problem där ApiRevisionDescription inte angavs vid skapande av ny API-revision https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="27ffd-1520">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="27ffd-1521">Åtgärdade skrivfel i modellen "PsApiManagementOAuth2AuthrozationServer" till "PsApiManagementOAuth2AuthorizationServer"</span><span class="sxs-lookup"><span data-stu-id="27ffd-1521">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27ffd-1522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27ffd-1522">Az.Batch</span></span>
* <span data-ttu-id="27ffd-1523">Åtgärdade skrivfel i hjälpmeddelande och dokumentation till att skriva Windows med versaler</span><span class="sxs-lookup"><span data-stu-id="27ffd-1523">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27ffd-1524">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27ffd-1524">Az.Cdn</span></span>
* <span data-ttu-id="27ffd-1525">Åtgärdade skrivfel i CDN-modulens konverteringshjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-1525">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1526">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1527">Lägg till VmssId i New-AzVMConfig-cmdleten</span><span class="sxs-lookup"><span data-stu-id="27ffd-1527">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="27ffd-1528">Lägg till parametrarna TerminateScheduledEvents och TerminateScheduledEventNotBeforeTimeoutInMinutes i New-AzVmssConfig och Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27ffd-1528">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="27ffd-1529">Lägg till egenskapen HyperVGeneration till avbildningsobjekt för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="27ffd-1529">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="27ffd-1530">Lägg till funktioner för Host och HostGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-1530">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="27ffd-1531">Nya cmdletar:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="27ffd-1531">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="27ffd-1532">HostId-parametern läggs till i New-AzVMConfig och New-AzVM</span><span class="sxs-lookup"><span data-stu-id="27ffd-1532">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="27ffd-1533">Uppdatera exempel i "Invoke-AzVMRunCommand"-dokumentationen till att använda rätt parameternamn</span><span class="sxs-lookup"><span data-stu-id="27ffd-1533">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="27ffd-1534">Uppdatera "-VolumeType"-beskrivningen i referensdokumentationen för "set-AzVMDiskEncryptionExtension" och "set-AzVmssDiskEncryptionExtension"</span><span class="sxs-lookup"><span data-stu-id="27ffd-1534">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-1535">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-1535">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-1536">Åtgärda skrivfel till att använda versaler för "Windows" i "New-AzDataFactoryEncryptValue"-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1536">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="27ffd-1537">Uppdaterade ADF .Net SDK-versionen till 4.1.2</span><span class="sxs-lookup"><span data-stu-id="27ffd-1537">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="27ffd-1538">Lägg till parametrarna "DataProxyIntegrationRuntimeName", "DataProxyStagingLinkedServiceName" och "DataProxyStagingPath" för "Set-AzureRmDataFactoryV2IntegrationRuntime"-cmd för att aktivera konfiguration av lokalt installerad integrationskörning som en proxy för SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="27ffd-1538">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="27ffd-1539">Uppdaterade PSTriggerRun till att visa utlöst pipeline, meddelande och egenskaper samt PSActivityRun till att visa aktivitetstypen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1539">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-1540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-1540">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-1541">Korrigering av frysning av Get-DataLakeStoreDeletedItem för fel eller fjärrundantag.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1541">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27ffd-1542">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1542">Az.EventHub</span></span>
* <span data-ttu-id="27ffd-1543">Korrigering av problem #9658 : Skrivfel i parametern VirtualNteworkRule i Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1543">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="27ffd-1544">Korrigering av problem #9558 : Set-AzEventHubNamespace använder PATCH i stället för PUT</span><span class="sxs-lookup"><span data-stu-id="27ffd-1544">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="27ffd-1545">lade till parametern EnableKafka i Set-AzEventHubNamespace-cmdleten</span><span class="sxs-lookup"><span data-stu-id="27ffd-1545">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="27ffd-1546">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1546">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="27ffd-1547">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="27ffd-1547">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="27ffd-1548">Åtgärdade skrivfel i dokumentation där "Azure" skrevs helt med gemener</span><span class="sxs-lookup"><span data-stu-id="27ffd-1548">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1549">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-1550">Åtgärdade felaktigt parameternamn i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1550">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1551">Az.Network</span></span>
* <span data-ttu-id="27ffd-1552">Uppdaterade New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1552">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="27ffd-1553">Gjorde parametern "PublicIpAddress" inaktuell eftersom den aldrig används på serversidan.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1553">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="27ffd-1554">Lade till den valfria parametern "Primary", som anger huruvida den aktuella IP-konfigurationen är den primära.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1554">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="27ffd-1555">Förbättrade hanteringen av felundantag för begärande från SDK – åtgärdar problemet att tidigare SDK-undantag inte hanteras på rätt sätt, vilket leder till att viktig felinformation inte visas</span><span class="sxs-lookup"><span data-stu-id="27ffd-1555">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="27ffd-1556">Justerade valideringslogiken för IPv6-IP-prefix till att kontrollera korrekt IPv6-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1556">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="27ffd-1557">Uppdaterade Get-AzVirtualNetworkSubnetConfig: Lade till parameter som anges till get av undernätets resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1557">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="27ffd-1558">Uppdaterade beskrivningen av parametern Location för AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="27ffd-1558">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-1559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-1559">Az.OperationalInsights</span></span>
* <span data-ttu-id="27ffd-1560">Uppdaterade dokumentation för "New-AzOperationalInsightsLinuxSyslogDataSource"</span><span class="sxs-lookup"><span data-stu-id="27ffd-1560">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="27ffd-1561">Lade till exempel</span><span class="sxs-lookup"><span data-stu-id="27ffd-1561">Added example</span></span>
    - <span data-ttu-id="27ffd-1562">Uppdaterade beskrivningen av parametern "-Name"</span><span class="sxs-lookup"><span data-stu-id="27ffd-1562">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="27ffd-1563">Lade till ett exempel för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="27ffd-1563">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="27ffd-1564">Ändrade beskrivningen av parametern -Name för New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="27ffd-1564">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-1565">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-1565">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-1566">Uppdatera "Get-AzRecoveryServicesBackupJobDetail.md"</span><span class="sxs-lookup"><span data-stu-id="27ffd-1566">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-1567">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-1567">Az.Resources</span></span>
* <span data-ttu-id="27ffd-1568">Lägg till stöd för den nya API-versionen från 2019-05-10 för Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="27ffd-1568">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="27ffd-1569">Lägg till stöd för "copy.count = 0" för variabler, resurser och egenskaper</span><span class="sxs-lookup"><span data-stu-id="27ffd-1569">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="27ffd-1570">Resurser med "condition = false" eller "copy.count = 0" tas bort i complete-läget</span><span class="sxs-lookup"><span data-stu-id="27ffd-1570">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="27ffd-1571">Lägg till ett exempel på tilldelning av princip på prenumerationsnivå i hjälpdokumentationen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1571">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27ffd-1572">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27ffd-1572">Az.ServiceBus</span></span>
* <span data-ttu-id="27ffd-1573">Korrigering av problem #9658 : Skrivfel i parametern VirtualNetworkRule i set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1573">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="27ffd-1574">Korrigering av problem #9786 : kan inte skapa en regel med Endast lyssna-behörighet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1574">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="27ffd-1575">Lade till det nya kommandot "Test-AzServiceBusNameAvailability" för att kontrollera namntillgängligheten för kö och ämne</span><span class="sxs-lookup"><span data-stu-id="27ffd-1575">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27ffd-1576">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-1576">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-1577">Åtgärda buggar med tillägg av nodtyps-cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1577">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="27ffd-1578">NullReferenceException-bugg när resursgrupp hade annan vmss som inte är relaterad till Service Fabric-klustret.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1578">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="27ffd-1579">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="27ffd-1579">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="27ffd-1580">Åtgärda bugg där cmdleten misslyckades om virtualNetwork var i en annan resursgrupp än klustret.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1580">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="27ffd-1581">Åtgärdar problemet: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="27ffd-1581">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="27ffd-1582">AzServiceFabricApplicationCertificate-cmdleten görs inaktuell</span><span class="sxs-lookup"><span data-stu-id="27ffd-1582">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1583">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1584">Uppdatera dokumentation om gamla gransknings-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1584">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-1585">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-1585">Az.Storage</span></span>
* <span data-ttu-id="27ffd-1586">Uppdatera hjälpen för Get/Close-AzStorageFileHandle genom att lägga till fler scenarier i cmdlet-exempel och uppdatera parameterbeskrivningar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1586">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="27ffd-1587">Stöd för StandardBlobTier i uppladdningsblob och kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="27ffd-1587">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="27ffd-1588">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27ffd-1588">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="27ffd-1589">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27ffd-1589">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="27ffd-1590">Stöd för rehydratiseringsprioritet i kopieringsblob</span><span class="sxs-lookup"><span data-stu-id="27ffd-1590">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="27ffd-1591">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27ffd-1591">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-1592">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-1592">Az.Websites</span></span>
* <span data-ttu-id="27ffd-1593">Lägg till klargöranden gällande parametern -AppSettings i Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="27ffd-1593">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="27ffd-1594">2.5.0 – July 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1594">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1595">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-1596">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="27ffd-1596">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="27ffd-1597">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-1597">Az.ApplicationInsights</span></span>
* <span data-ttu-id="27ffd-1598">Korrigera skrivfel i exempel i dokumentationen för Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="27ffd-1598">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-1599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-1599">Az.Automation</span></span>
* <span data-ttu-id="27ffd-1600">Korrigera skrivfel i resurssträng</span><span class="sxs-lookup"><span data-stu-id="27ffd-1600">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-1601">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-1601">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-1602">Stöd för NetworkRuleSet har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1602">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1603">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1604">Lägg till saknade egenskaper (ComputerName, OsName, OsVersion och HyperVGeneration) för visningsobjekt i den virtuella datorinstansen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1604">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="27ffd-1605">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27ffd-1605">Az.ContainerRegistry</span></span>
* <span data-ttu-id="27ffd-1606">Åtgärda skrivfel i Remove-AzContainerRegistryReplication för parametern Replication</span><span class="sxs-lookup"><span data-stu-id="27ffd-1606">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="27ffd-1607">Mer information finns här: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="27ffd-1607">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-1608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-1608">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-1609">ADF .Net SDK-versionen har uppdaterats till 4.1.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1609">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="27ffd-1610">Korrigera skrivfel i dokumentationen för Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="27ffd-1610">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27ffd-1611">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1611">Az.EventHub</span></span>
* <span data-ttu-id="27ffd-1612">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="27ffd-1612">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="27ffd-1613">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1613">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-1614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-1614">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-1615">Stöd har lagts till för att ange KeySize för certifikatprinciper</span><span class="sxs-lookup"><span data-stu-id="27ffd-1615">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27ffd-1616">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27ffd-1616">Az.LogicApp</span></span>
* <span data-ttu-id="27ffd-1617">Korrigering för Get-AzIntegrationAccountMap för att lista alla mappningstyper</span><span class="sxs-lookup"><span data-stu-id="27ffd-1617">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="27ffd-1618">Ny MapType-parameter har lagts till för filtrering</span><span class="sxs-lookup"><span data-stu-id="27ffd-1618">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="27ffd-1619">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-1619">Az.ManagedServices</span></span>
* <span data-ttu-id="27ffd-1620">Stöd för API-versionen 2019-06-01 (GA) har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1620">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1621">Az.Network</span></span>
* <span data-ttu-id="27ffd-1622">Lägg till stöd för privat slutpunkt och privat länktjänst</span><span class="sxs-lookup"><span data-stu-id="27ffd-1622">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="27ffd-1623">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1623">New cmdlets</span></span>
        - <span data-ttu-id="27ffd-1624">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ffd-1624">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27ffd-1625">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27ffd-1625">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27ffd-1626">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1626">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27ffd-1627">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1627">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27ffd-1628">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1628">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27ffd-1629">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1629">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27ffd-1630">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="27ffd-1630">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="27ffd-1631">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27ffd-1631">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="27ffd-1632">Nedanstående kommandon för funktionen har uppdaterats: Flaggan PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies på undernätet i VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="27ffd-1632">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="27ffd-1633">Uppdaterade New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1633">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="27ffd-1634">Valfri parameter har lagts till – PrivateEndpointNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat slutpunkt i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1634">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="27ffd-1635">Valfri parameter har lagts till – PrivateLinkServiceNetworkPoliciesFlag som konfigurerar huruvida nätverksprinciper ska tillämpas på en privat länktjänst i det här undernätet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1635">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="27ffd-1636">AzPrivateLinkService för cmdlet-parametern ServiceName har bytt namn till Name med aliaset ServiceName för bakåtkompatibilitet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1636">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="27ffd-1637">Aktivera ICMP-protokoll för konfiguration av nätverkssäkerhetsregler</span><span class="sxs-lookup"><span data-stu-id="27ffd-1637">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="27ffd-1638">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1638">Updated cmdlets</span></span>
        - <span data-ttu-id="27ffd-1639">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1639">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27ffd-1640">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1640">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27ffd-1641">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1641">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="27ffd-1642">Lägg till ConnectionProtocolType (Ikev1/Ikev2) som en konfigurerbar parameter för New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1642">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="27ffd-1643">Lägg till PrivateIpAddressVersion i LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-1643">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="27ffd-1644">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1644">Updated cmdlet:</span></span>
        - <span data-ttu-id="27ffd-1645">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1645">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="27ffd-1646">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1646">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="27ffd-1647">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1647">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="27ffd-1648">Uppdatering av Application Gateway-kommandot New-AzApplicationGatewayProbeConfig för stöd av anpassad port i Probe</span><span class="sxs-lookup"><span data-stu-id="27ffd-1648">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="27ffd-1649">Uppdaterade New-AzApplicationGatewayProbeConfig: Den valfria parametern Port som används för avsökning i serverdelen har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1649">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="27ffd-1650">Denna parameter gäller för SKU:erna Standard_V2 och WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1650">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-1651">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-1651">Az.OperationalInsights</span></span>
* <span data-ttu-id="27ffd-1652">Uppdaterade standardversionen för sparade sökningar till 1.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1652">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="27ffd-1653">Åtgärdade hantering av anpassad log null regex</span><span class="sxs-lookup"><span data-stu-id="27ffd-1653">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-1654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-1654">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-1655">Uppdatera Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-1655">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="27ffd-1656">Uppdatera Get-AzRecoveryServicesBackupContainer.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-1656">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="27ffd-1657">Uppdatera Get-AzRecoveryServicesVault.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-1657">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="27ffd-1658">Uppdatera Wait-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-1658">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="27ffd-1659">Uppdatera Set-AzRecoveryServicesVaultContext.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-1659">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="27ffd-1660">Uppdatera Get-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-1660">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="27ffd-1661">Uppdatera Get-AzRecoveryServicesBackupRecoveryPoint.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-1661">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="27ffd-1662">Uppdatera Restore-AzRecoveryServicesBackupItem.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-1662">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="27ffd-1663">Uppdaterat tjänstanrop för avregistrering av container för Azure-filresurs</span><span class="sxs-lookup"><span data-stu-id="27ffd-1663">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="27ffd-1664">Uppdatera Set-AzRecoveryServicesAsrAlertSetting.md</span><span class="sxs-lookup"><span data-stu-id="27ffd-1664">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-1665">Az.Resources</span></span>
- <span data-ttu-id="27ffd-1666">Ta bort den cmdlet som saknas och som refereras i dokumentationen till New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="27ffd-1666">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="27ffd-1667">Princip-cmdletar har uppdaterats så att de använder den nya API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="27ffd-1667">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27ffd-1668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27ffd-1668">Az.ServiceBus</span></span>
* <span data-ttu-id="27ffd-1669">Ny cmmdlet har lagts till för att skapa SAS-token: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="27ffd-1669">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="27ffd-1670">verifierings- och felmeddelande har lagts till för authorizationrules-rättigheter om endast "hantera" har tilldelats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1670">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1671">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1672">Åtgärda saknade exempel för Set-AzSqlDatabaseSecondary cmdlet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1672">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="27ffd-1673">Åtgärda angivna återkommande genomsökningar för bedömning av säkerhetsrisk utan angivna e-postadresser</span><span class="sxs-lookup"><span data-stu-id="27ffd-1673">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="27ffd-1674">Korrigera ett skrivfel i ett varningsmeddelande.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1674">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-1675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-1675">Az.Storage</span></span>
* <span data-ttu-id="27ffd-1676">Uppdatera exempel i referensdokumentationen för Get-AzStorageAccount så att rätt parameternamn används</span><span class="sxs-lookup"><span data-stu-id="27ffd-1676">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27ffd-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27ffd-1677">Az.StorageSync</span></span>
* <span data-ttu-id="27ffd-1678">Lägger till cmdleten Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1678">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="27ffd-1679">Åtgärda problem 9551 så att TierFilesOlderThanDays föredras</span><span class="sxs-lookup"><span data-stu-id="27ffd-1679">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-1680">Az.Websites</span></span>
* <span data-ttu-id="27ffd-1681">Åtgärdar ett fel där vissa SiteConfig-egenskaper inte returnerades av Get-AzWebApp och Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="27ffd-1681">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="27ffd-1682">Lägger till en ny platsparameter för Get-AzDeletedWebApp och Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="27ffd-1682">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="27ffd-1683">Åtgärdar ett fel i kloning av webbapp-platser som använder New-AzWebApp-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="27ffd-1683">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="27ffd-1684">2.4.0 – juli 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1684">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-1685">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1685">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-1686">Lägg till stöd för profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1686">Add support for profile cmdlets</span></span>
* <span data-ttu-id="27ffd-1687">Lägg till stöd för miljöer och dataplaner i genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1687">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="27ffd-1688">Åtgärda bugg där fel slutpunkt i vissa fall användes för cmdletar för dataplaner i Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="27ffd-1688">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="27ffd-1689">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1689">Az.Advisor</span></span>
* <span data-ttu-id="27ffd-1690">GA-version av Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1690">GA release of Az.Advisor</span></span>
* <span data-ttu-id="27ffd-1691">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1691">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-1692">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-1692">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-1693">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="27ffd-1693">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="27ffd-1694">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="27ffd-1694">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="27ffd-1695">Stöd för att fråga prenumerationer efter användare och produkt har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1695">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="27ffd-1696">Stöd för att fråga med hjälp av omfång ”/”, ”/apis”, ”/apis/echo-api” har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1696">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="27ffd-1697">Korrigering av problem https://github.com/Azure/azure-powershell/issues/9307 och https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="27ffd-1697">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="27ffd-1698">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="27ffd-1698">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="27ffd-1699">Stöd för att ange ”ApiVersion” och ”ApiVersionSetId” när API:er importeras har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1699">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-1700">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-1700">Az.Automation</span></span>
* <span data-ttu-id="27ffd-1701">Bugg med cmdleten Set-AzAutomationConnectionFieldValue för att hantera strängvärde har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1701">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1702">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1703">Lägg till parametern HyperVGeneration i New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1703">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-1704">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-1704">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-1705">Uppdaterar utdata från ADF-cmdletar som hämtar aktivitetskörningar, hämtar pipelinekörningar och hämtar utlösarkörningar för stöd för Select-Object-pipe.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1705">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27ffd-1706">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27ffd-1706">Az.EventGrid</span></span>
* <span data-ttu-id="27ffd-1707">Korrigera stavfel i dokumentation om ”New-AzEventGridSubscription”</span><span class="sxs-lookup"><span data-stu-id="27ffd-1707">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-1708">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1708">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-1709">Lägg till stöd för att återskapa principnycklar för auktorisering.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1709">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1710">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1710">Az.Network</span></span>
* <span data-ttu-id="27ffd-1711">”RoutingPreference” har lagts till i offentliga IP-taggar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1711">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="27ffd-1712">Förbättra exempel för referensdokumentation om ”Get-AzNetworkServiceTag”</span><span class="sxs-lookup"><span data-stu-id="27ffd-1712">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27ffd-1713">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-1713">Az.PolicyInsights</span></span>
* <span data-ttu-id="27ffd-1714">Åtgärda problem med null-referens i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="27ffd-1714">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="27ffd-1715">Mer information här: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="27ffd-1715">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-1716">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-1716">Az.OperationalInsights</span></span>
* <span data-ttu-id="27ffd-1717">Modellen för CustomLog-datakälla som returneras i Get-AzOperationalInsightsDataSource har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1717">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-1718">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-1718">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-1719">Kommandot get-policy för IaaSVM:er har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1719">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-1720">Az.Resources</span></span>
    - <span data-ttu-id="27ffd-1721">Korrigera hjälptext för den översta parametern i Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="27ffd-1721">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="27ffd-1722">Lägg till växlingsstöd på klientsidan för Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="27ffd-1722">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="27ffd-1723">Lägg till nya parametrar för Set-AzPolicyAssignment, -PolicyParameters och -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="27ffd-1723">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="27ffd-1724">En mängd dokument- och exempeluppdateringar för Policy-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1724">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27ffd-1725">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27ffd-1725">Az.ServiceBus</span></span>
* <span data-ttu-id="27ffd-1726">Korrigering av problem #4938 – New-AzureRmServiceBusQueue returnerar BadRequest vid konfiguration av MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="27ffd-1726">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1727">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1727">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1728">Lägg till cmdletar för instansredundansgrupper från förhandsversion till offentlig version</span><span class="sxs-lookup"><span data-stu-id="27ffd-1728">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="27ffd-1729">Stöd för granskning för Azure SQL Server\Database med nya cmdletar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1729">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="27ffd-1730">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="27ffd-1730">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="27ffd-1731">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="27ffd-1731">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="27ffd-1732">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="27ffd-1732">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="27ffd-1733">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="27ffd-1733">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="27ffd-1734">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="27ffd-1734">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="27ffd-1735">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="27ffd-1735">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="27ffd-1736">Ta bort begränsningar för e-post från inställningarna för sårbarhetsbedömning</span><span class="sxs-lookup"><span data-stu-id="27ffd-1736">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-1737">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-1737">Az.Storage</span></span>
* <span data-ttu-id="27ffd-1738">Ändra två parametrar ”-IndexDocument” och ”-ErrorDocument404Path” från ”krävs” till ”valfri” i cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1738">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="27ffd-1739">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="27ffd-1739">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="27ffd-1740">Uppdatera hjälpen för Get-AzStorageBlobContent genom att lägga till ett exempel</span><span class="sxs-lookup"><span data-stu-id="27ffd-1740">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="27ffd-1741">Visa mer felinformation när cmdleten misslyckas med StorageException</span><span class="sxs-lookup"><span data-stu-id="27ffd-1741">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="27ffd-1742">Stöd för att skapa eller uppdatera lagringskonto med Azure Files AAD DS-autentisering</span><span class="sxs-lookup"><span data-stu-id="27ffd-1742">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="27ffd-1743">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-1743">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="27ffd-1744">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-1744">Set-AzStorageAccount</span></span>
* <span data-ttu-id="27ffd-1745">Stöd för att lista eller stänga filreferenser för en filresurs, filkatalog eller en fil</span><span class="sxs-lookup"><span data-stu-id="27ffd-1745">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="27ffd-1746">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27ffd-1746">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="27ffd-1747">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27ffd-1747">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27ffd-1748">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27ffd-1748">Az.StorageSync</span></span>
* <span data-ttu-id="27ffd-1749">Den här modulen ingår nu som en del av `Az`-sammanslagningsmodulen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1749">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="27ffd-1750">2.3.2 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1750">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-1751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-1751">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-1752">Åtgärda bugg med felaktiga webbadresser som i vissa fall användes för Functions-anrop</span><span class="sxs-lookup"><span data-stu-id="27ffd-1752">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="27ffd-1753">Mer information här: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="27ffd-1753">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="27ffd-1754">Åtgärda problem med alias från AzureRM i Az-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1754">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="27ffd-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="27ffd-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="27ffd-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="27ffd-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1757">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1758">Parameteruppsättningarna New-AzVm och New-AzVmss accepterar nu parametern ”ProximityPlacementGroup”.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1758">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="27ffd-1759">Stavfel i referensdokumentationen för ”New-AzVM” har korrigerats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1759">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="27ffd-1760">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="27ffd-1760">Az.Dns</span></span>
* <span data-ttu-id="27ffd-1761">Stavfel i hjälpexempel för ”Set-AzDnsZone” har korrigerats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1761">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27ffd-1762">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27ffd-1762">Az.EventGrid</span></span>
* <span data-ttu-id="27ffd-1763">Har uppdaterats för att använda API-versionen 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1763">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="27ffd-1764">Nya cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1764">New cmdlets:</span></span>
    - <span data-ttu-id="27ffd-1765">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="27ffd-1765">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="27ffd-1766">Skapar en ny Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1766">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="27ffd-1767">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="27ffd-1767">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="27ffd-1768">Hämtar information om en Event Grid-domän eller hämtar en lista med alla Event Grid-domäner i den aktuella Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1768">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="27ffd-1769">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="27ffd-1769">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="27ffd-1770">Tar bort en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1770">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="27ffd-1771">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="27ffd-1771">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="27ffd-1772">Återskapar nyckeln för delad åtkomst för en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1772">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="27ffd-1773">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="27ffd-1773">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="27ffd-1774">Hämtar de nycklar för delad åtkomst som används för att publicera händelser till en Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1774">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="27ffd-1775">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1775">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="27ffd-1776">Skapar ett nytt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1776">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="27ffd-1777">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="27ffd-1777">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="27ffd-1778">Hämtar information om ett Event Grid-domänämne eller hämtar en lista med alla Event Grid-domänämnen under en specifik Event Grid-domän i nuvarande Azure</span><span class="sxs-lookup"><span data-stu-id="27ffd-1778">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="27ffd-1779">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1779">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="27ffd-1780">Tar bort ett befintligt Azure Event Grid-domänämne.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1780">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="27ffd-1781">Uppdaterade cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1781">Updated cmdlets:</span></span>
    - <span data-ttu-id="27ffd-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="27ffd-1783">Lägg till nya obligatoriska parametrar för att stödja piping för den nya Event Grid-domänen och Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1783">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="27ffd-1784">Lägg till nya obligatoriska parametrar för att ange det nya Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att skapa nya händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1784">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="27ffd-1785">Lägg till ny parameteruppsättningar för domäner och domänämnen för att göra det möjligt att återanvända befintliga parametrar (t.ex. EndPointType, SubjectBeginsWith osv).</span><span class="sxs-lookup"><span data-stu-id="27ffd-1785">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="27ffd-1786">Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1786">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="27ffd-1787">Förfallodatum för händelseprenumeration</span><span class="sxs-lookup"><span data-stu-id="27ffd-1787">Event subscription expiration date,</span></span>
            - <span data-ttu-id="27ffd-1788">Avancerade filterparametrar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1788">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="27ffd-1789">Lägg till ny uppräkning för servicebusqueue som mål.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1789">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="27ffd-1790">Tillåt inte användning av ”Alla” i alternativet -IncludedEventType och ersätt det med</span><span class="sxs-lookup"><span data-stu-id="27ffd-1790">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="27ffd-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="27ffd-1792">Lägg till ny valfria parametrar (Top, ODataQuery och NextLink) för att stödja sidnumrering och filtrering av resultat.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1792">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="27ffd-1793">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="27ffd-1793">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="27ffd-1794">Lägg till nya obligatoriska parametrar för att stödja piping för en Event Grid-domän och Event Grid-domänämnen för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1794">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="27ffd-1795">Lägg till nya obligatoriska parametrar för att ange Event Grid-domännamnet och/eller namnet på Event Grid-domänämnet för att göra det möjligt att ta bort befintliga händelseprenumerationer under dessa resurser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1795">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27ffd-1796">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1796">Az.FrontDoor</span></span>
* <span data-ttu-id="27ffd-1797">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="27ffd-1797">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="27ffd-1798">Lägg till stöd för transformeringar och nytt värde för automatisk komplettering för operatorer (RegEx)</span><span class="sxs-lookup"><span data-stu-id="27ffd-1798">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="27ffd-1799">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="27ffd-1799">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="27ffd-1800">Lägg till nya värden för automatisk komplettering</span><span class="sxs-lookup"><span data-stu-id="27ffd-1800">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1801">Az.Network</span></span>
* <span data-ttu-id="27ffd-1802">Lägg till stöd för resurs för virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-1802">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="27ffd-1803">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1803">New cmdlets</span></span>
        - <span data-ttu-id="27ffd-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="27ffd-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="27ffd-1805">Lägg till AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="27ffd-1805">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="27ffd-1806">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1806">New cmdlets</span></span>
        - <span data-ttu-id="27ffd-1807">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="27ffd-1807">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="27ffd-1808">Lägg till PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27ffd-1808">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="27ffd-1809">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1809">New cmdlets</span></span>
        - <span data-ttu-id="27ffd-1810">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27ffd-1810">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27ffd-1811">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27ffd-1811">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27ffd-1812">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27ffd-1812">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27ffd-1813">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-1813">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="27ffd-1814">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1814">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="27ffd-1815">Lägg till PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ffd-1815">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="27ffd-1816">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1816">New cmdlets</span></span>
        - <span data-ttu-id="27ffd-1817">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ffd-1817">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27ffd-1818">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ffd-1818">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27ffd-1819">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ffd-1819">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27ffd-1820">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1820">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="27ffd-1821">Nedanstående kommandon för funktionen har uppdaterats: Flaggan UseLocalAzureIpAddress på VpnConnection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1821">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="27ffd-1822">New-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1822">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="27ffd-1823">Set-AzVpnConnection har uppdaterats: Den valfria parametern -UseLocalAzureIpAddress har lagts till för att visa att en lokal IP-adress i Azure ska användas som källadress när anslutningen initieras.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1823">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="27ffd-1824">Det skrivskyddade fältet PeeredConnections har lagts till i ExpressRoute-peering.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1824">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="27ffd-1825">Det skrivskyddade fältet GlobalReachEnabled har lagts till i ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1825">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="27ffd-1826">Ett attribut för icke-bakåtkompatibla ändringar har lagts till för att lyfta fram utfasning av fältet AllowGlobalReach i modellen ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="27ffd-1826">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="27ffd-1827">Problem 8756 har åtgärdats: Fel vid användning av TargetListenerID med AzApplicationGatewayRedirectConfiguration-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1827">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="27ffd-1828">En bugg i New-AzApplicationGatewayPathRuleConfig som gjorde att regeluppsättningen för att återskapa inte kunde anges har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1828">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="27ffd-1829">Visningen av VirtualNetworkTaps i NetworkInterfaceIpConfiguration har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1829">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="27ffd-1830">Cortex Get-cmdletar för att visa en lista med alla delar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1830">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="27ffd-1831">Funktionen för att skapa VirtualHub-referenser för ExpressRouteGateways och VpnGateway har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1831">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="27ffd-1832">Stöd för tillgänglighetszoner i AzureFirewall och NatGateway har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1832">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="27ffd-1833">Cmdleten Get-AzNetworkServiceTag har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1833">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="27ffd-1834">Lägg till stöd för flera offentliga IP-adresser för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="27ffd-1834">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="27ffd-1835">Cmdleten New-AzFirewall har uppdaterats:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1835">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="27ffd-1836">Parametern -PublicIpAddress som accepterar ett eller flera offentliga IP-adressobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1836">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="27ffd-1837">Parametern -VirtualNetwork som accepterar ett virtuellt nätverksobjekt har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-1837">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="27ffd-1838">Metoderna AddPublicIpAddress och RemovePublicIpAddress har lagts till på brandväggsobjekt – dessa accepterar ett offentligt IP-adressobjekt som indata</span><span class="sxs-lookup"><span data-stu-id="27ffd-1838">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="27ffd-1839">Inaktuella parametrar -PublicIpName och -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="27ffd-1839">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="27ffd-1840">Nedanstående kommandon för funktionen har uppdaterats: Ange autentiseringsalternativ för VpnClient AAD till resurser för virtuella nätverksgatewayer.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1840">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="27ffd-1841">New-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1841">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="27ffd-1842">Set-AzVirtualNetworkGateway har uppdaterats: De valfria parametrarna AadTenantUri, AadAudienceId och AadIssuerUri för att ange VpnClient AAD-autentiseringsalternativ på en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1842">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="27ffd-1843">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria växelparametern RemoveAadAuthentication som tar bort VpnClient AAD-autentiseringsalternativ från en gateway har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1843">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-1844">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-1844">Az.OperationalInsights</span></span>
* <span data-ttu-id="27ffd-1845">Aktivera prisnivån **pergb2018** i kommandot ”New-AzureRmOperationalInsightsWorkspace”</span><span class="sxs-lookup"><span data-stu-id="27ffd-1845">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-1846">Az.Resources</span></span>
* <span data-ttu-id="27ffd-1847">Stöd för ytterligare alternativ för att exportera en mall</span><span class="sxs-lookup"><span data-stu-id="27ffd-1847">Support for additional Template Export options</span></span>
    - <span data-ttu-id="27ffd-1848">Lägg till parametern ”-SkipResourceNameParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-1848">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="27ffd-1849">Lägg till parametern ”-SkipAllParameterization” till Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-1849">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="27ffd-1850">Lägg till parametern ”-Resource” till Export-AzResourceGroup för exporterad resursfiltrering</span><span class="sxs-lookup"><span data-stu-id="27ffd-1850">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27ffd-1851">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-1851">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-1852">Åtgärda att fel tumavtryck används vid tilläggning av certifikat i ByExistingKeyVault i vissa fall</span><span class="sxs-lookup"><span data-stu-id="27ffd-1852">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1853">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1854">Åtgärda suffix för lagringsslutpunkt i Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1854">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="27ffd-1855">Åtgärda att aktivering av Advanced Data Security åsidosätter Advanced Threat Protection-princip</span><span class="sxs-lookup"><span data-stu-id="27ffd-1855">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="27ffd-1856">Nya cmdletar för Management.Sql som gör att kunderna kan lägga till nycklar för transparent datakryptering (TDE) och ange TDE-skydd för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="27ffd-1856">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="27ffd-1857">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27ffd-1857">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="27ffd-1858">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27ffd-1858">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="27ffd-1859">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27ffd-1859">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="27ffd-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="27ffd-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="27ffd-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="27ffd-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-1862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-1862">Az.Storage</span></span>
* <span data-ttu-id="27ffd-1863">Stöd för typerna FileStorage och SkuName Premium_ZRS när lagringskonton skapas</span><span class="sxs-lookup"><span data-stu-id="27ffd-1863">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="27ffd-1864">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-1864">New-AzStorageAccount</span></span>
* <span data-ttu-id="27ffd-1865">Beskrivningen av cmdleten för bloboföränderlighet har förtydligats</span><span class="sxs-lookup"><span data-stu-id="27ffd-1865">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="27ffd-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-1867">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-1867">Az.Websites</span></span>
* <span data-ttu-id="27ffd-1868">Optimerar Get-AzWebAppCertificate för att filtrera efter resursgrupp på servern i stället för klienten</span><span class="sxs-lookup"><span data-stu-id="27ffd-1868">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="27ffd-1869">Lägger till växlingsparametern -UseDisasterRecovery till Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="27ffd-1869">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="27ffd-1870">2.2.0 – juni 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1870">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="27ffd-1871">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27ffd-1871">Az.Cdn</span></span>
* <span data-ttu-id="27ffd-1872">Uppdaterade cmdletar för att ge stöd för rulesEngine-funktion baserat på API-version 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1872">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1873">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1874">Lade till parameter `NoWait` som startar åtgärden och returnerar omedelbart, innan åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1874">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="27ffd-1875">Uppdaterade cmdletar:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="27ffd-1875">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27ffd-1876">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-1876">Az.EventHub</span></span>
* <span data-ttu-id="27ffd-1877">Korrigering för #9231 – Get-AzEventHubNamespace returnerar inga taggar</span><span class="sxs-lookup"><span data-stu-id="27ffd-1877">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="27ffd-1878">Korrigering för #9230 – Get-AzEventHubNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ffd-1878">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1879">Az.Network</span></span>
* <span data-ttu-id="27ffd-1880">Uppdatera ResourceId och InputObject för NAT-gateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-1880">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="27ffd-1881">Lägg till alias för ResourceId och InputObject</span><span class="sxs-lookup"><span data-stu-id="27ffd-1881">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27ffd-1882">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-1882">Az.PolicyInsights</span></span>
* <span data-ttu-id="27ffd-1883">Åtgärda Null-referensproblem i Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="27ffd-1883">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-1884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-1884">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-1885">Minsta kvarhållning för IaaSVM-policy i dagar ändrat till 7 från 1</span><span class="sxs-lookup"><span data-stu-id="27ffd-1885">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27ffd-1886">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27ffd-1886">Az.ServiceBus</span></span>
* <span data-ttu-id="27ffd-1887">Korrigering för ärende #9182 – Get-AzServiceBusNamespace returnerar ResourceGroup istället för ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ffd-1887">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27ffd-1888">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-1888">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-1889">Åtgärda stavfel i felmeddelandet för Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="27ffd-1889">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="27ffd-1890">Åtgärda saknat tecken i Service Fabric-kommandorader</span><span class="sxs-lookup"><span data-stu-id="27ffd-1890">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1891">Az.Sql</span></span>
* <span data-ttu-id="27ffd-1892">Lägg till parametern DnsZonePartner för New-AzureSqlInstance-cmdlet för att ge stöd för AutoDr för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1892">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="27ffd-1893">Avvecklar cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-1893">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="27ffd-1894">Döp om cmdletar för hotidentifiering till Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="27ffd-1894">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="27ffd-1895">Parametrarna New-AzSqlInstance -StorageSizeInGB och -LicenseType är nu valfria.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1895">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-1896">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-1896">Az.Websites</span></span>
* <span data-ttu-id="27ffd-1897">åtgärdar problemet där användningen av Set-AzWebApp och Set-AzWebAppSlot med -WebApp-egenskap tog bort taggarna</span><span class="sxs-lookup"><span data-stu-id="27ffd-1897">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="27ffd-1898">2.1.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-1898">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="27ffd-1899">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-1899">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-1900">Skapade nya cmdletar för att hantera diagnostik för global- och API-omfång</span><span class="sxs-lookup"><span data-stu-id="27ffd-1900">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="27ffd-1901">**Get-AzApiManagementDiagnostic** – Skaffa diagnostik konfigurerad för global- eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="27ffd-1901">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="27ffd-1902">**New-AzApiManagementDiagnostic** – Skapa ny diagnostik för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="27ffd-1902">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="27ffd-1903">**New-AzApiManagementHttpMessageDiagnostic** – Skapa diagnostikinställning om vilka rubriker som ska loggas och storleken på brödtextbyte</span><span class="sxs-lookup"><span data-stu-id="27ffd-1903">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="27ffd-1904">**New-AzApiManagementPipelineDiagnosticSetting** – Skapa diagnostikinställningar för inkommande/utgående HTTP-meddelanden till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1904">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="27ffd-1905">**New-AzApiManagementSamplingSetting** – Skapa samplinginställningar för begäranden/svar för en diagnostik</span><span class="sxs-lookup"><span data-stu-id="27ffd-1905">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="27ffd-1906">**Remove-AzApiManagementDiagnostic** – Ta bort en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="27ffd-1906">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="27ffd-1907">**Set-AzApiManagementDiagnostic** – Uppdatera en diagnostikenhet för globalt omfång eller api-omfång</span><span class="sxs-lookup"><span data-stu-id="27ffd-1907">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="27ffd-1908">Skapade nya cmdletar för hantering av cacheminne i ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="27ffd-1908">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="27ffd-1909">**Get-AzApiManagementCache** – Hämta information om cacheminnet som anges av identifierare eller alla cacheminnen</span><span class="sxs-lookup"><span data-stu-id="27ffd-1909">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="27ffd-1910">**New-AzApiManagementCache** – Skapa ett nytt default-cacheminne eller cacheminne i en viss Azure-region</span><span class="sxs-lookup"><span data-stu-id="27ffd-1910">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="27ffd-1911">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="27ffd-1911">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="27ffd-1912">**Remove-AzApiManagementCache** – Ta bort ett cacheminne</span><span class="sxs-lookup"><span data-stu-id="27ffd-1912">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="27ffd-1913">Skapade nya cmdletar för hantering av API-schema</span><span class="sxs-lookup"><span data-stu-id="27ffd-1913">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="27ffd-1914">**New-AzApiManagementSchema** – Skapa ett nytt schema för ett API</span><span class="sxs-lookup"><span data-stu-id="27ffd-1914">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="27ffd-1915">**Get-AzApiManagementSchema** – Hämta de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="27ffd-1915">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="27ffd-1916">**Remove-AzApiManagementSchema** – Ta bort de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="27ffd-1916">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="27ffd-1917">**Set-AzApiManagementSchema** – Uppdatera de scheman som konfigurerats i API:et</span><span class="sxs-lookup"><span data-stu-id="27ffd-1917">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="27ffd-1918">Skapa ny cmdlet för att generera en användartoken.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1918">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="27ffd-1919">**New-AzApiManagementUserToken** – Skapa en ny användartoken som enligt standardinställning är giltig i 8 timmar. Token för GIT-användaren kan skapas med den här cmdleten./</span><span class="sxs-lookup"><span data-stu-id="27ffd-1919">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="27ffd-1920">Skapade en ny cmdlet för att hämta nätverksstatus</span><span class="sxs-lookup"><span data-stu-id="27ffd-1920">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="27ffd-1921">**Get-AzApiManagementNetworkStatus** – Hämta nätverksstatusanslutningen för resurserna som API Management-tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1921">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="27ffd-1922">Det här är användbart när du distribuerar ApiManagement-tjänsten i ett virtuellt nätverk och validerar om något beroende är brutet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1922">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="27ffd-1923">Uppdaterade cmdlet **New-AzApiManagement** för att hantera ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="27ffd-1923">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="27ffd-1924">Lade till stöd för den nya SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="27ffd-1924">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="27ffd-1925">Aktiverade stöd för att slå på flaggan EnableClientCertificate för SKU:n Consumption</span><span class="sxs-lookup"><span data-stu-id="27ffd-1925">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="27ffd-1926">Den nya cmdleten **New-AzApiManagementSslSetting** gör det möjligt att ställa in TLS/SSL-inställningen på ”Backend” och ”Frontend” (serverdel och klientdel).</span><span class="sxs-lookup"><span data-stu-id="27ffd-1926">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="27ffd-1927">Det här kan också användas till att konfigurera chiffer som 3DES och ServerProtocols som Http2 för Frontend för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1927">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="27ffd-1928">Stöd har lagts till för att konfigurera värdnamnet DeveloperPortal på ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1928">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="27ffd-1929">Uppdaterade cmdletar **Get-AzApiManagementSsoToken** för att ta PsApiManagement-objekt som indata</span><span class="sxs-lookup"><span data-stu-id="27ffd-1929">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="27ffd-1930">Uppdaterad cmdleten för att visa infogade felmeddelanden</span><span class="sxs-lookup"><span data-stu-id="27ffd-1930">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="27ffd-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Felkod: Felmeddelande av typen ValidationError: Ett eller flera fält innehåller felaktiga värden: Felinformation:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="27ffd-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="27ffd-1932">Uppdaterade cmdlet **Export-AzApiManagementApi** för att exportera API:er i OpenApi 3.0-format</span><span class="sxs-lookup"><span data-stu-id="27ffd-1932">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="27ffd-1933">Uppdaterade cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="27ffd-1933">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="27ffd-1934">Importera API från dokumentspecifikationen OpenApi 3.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-1934">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="27ffd-1935">Om du vill åsidosätta egenskapen PsApiManagementSchema specificerad i ett dokument (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="27ffd-1935">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="27ffd-1936">Åsidosätta egenskapen ServiceUrl som specificeras i ett dokument.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1936">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="27ffd-1937">Uppdaterade cmdlet **Get-AzApiManagementPolicy** för att returnera policy i undantaget format av typen icke-XML med rawxml</span><span class="sxs-lookup"><span data-stu-id="27ffd-1937">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="27ffd-1938">Uppdaterade cmdlet **Set-AzApiManagementPolicy** för att godkänna policy i undantaget format av typen icke-XML med rawxml och XML undantaget med xml</span><span class="sxs-lookup"><span data-stu-id="27ffd-1938">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="27ffd-1939">Uppdaterad cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="27ffd-1939">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="27ffd-1940">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1940">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="27ffd-1941">Skapa ett API i ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1941">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="27ffd-1942">Klona ett API med SourceApiId och SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1942">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="27ffd-1943">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1943">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="27ffd-1944">Uppdaterad cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="27ffd-1944">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="27ffd-1945">Konfigurera API med OpenId auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1945">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="27ffd-1946">Uppdatera ett API till ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1946">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="27ffd-1947">Möjlighet att konfigurera SubscriptionRequired i API-omfattningen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1947">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="27ffd-1948">Uppdaterad cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="27ffd-1948">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="27ffd-1949">Klona en befintlig version med hjälp av SourceApiRevision (kopiera taggar, produkter, åtgärder och principer).</span><span class="sxs-lookup"><span data-stu-id="27ffd-1949">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="27ffd-1950">Den nya revisionen antar ApiId från den överordnade instansen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1950">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="27ffd-1951">Tillhandahålla ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="27ffd-1951">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="27ffd-1952">Åsidosätta ServiceUrl vid kloning av ett API.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1952">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="27ffd-1953">Uppdaterad cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="27ffd-1953">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="27ffd-1954">Konfigurera AAD eller AADB2C med en Authority</span><span class="sxs-lookup"><span data-stu-id="27ffd-1954">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="27ffd-1955">Konfigurera SignupPolicy, SigninPolicy, ProfileEditingPolicy och PasswordResetPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-1955">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="27ffd-1956">Uppdaterad cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="27ffd-1956">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="27ffd-1957">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="27ffd-1957">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="27ffd-1958">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="27ffd-1958">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="27ffd-1959">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1959">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="27ffd-1960">Uppdaterad cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="27ffd-1960">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="27ffd-1961">Kompensera för ny SubscriptonModel med Scope och UserId</span><span class="sxs-lookup"><span data-stu-id="27ffd-1961">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="27ffd-1962">Kompensera för gammal prenumerationsmodell med ProductId och UserId</span><span class="sxs-lookup"><span data-stu-id="27ffd-1962">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="27ffd-1963">Lägg till funktion för att aktivera AllowTracing på prenumerationsnivå.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1963">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="27ffd-1964">Uppdaterade följande cmdletar för att acceptera ResourceId som indata</span><span class="sxs-lookup"><span data-stu-id="27ffd-1964">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="27ffd-1965">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="27ffd-1965">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="27ffd-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="27ffd-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="27ffd-1967">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="27ffd-1967">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="27ffd-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="27ffd-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="27ffd-1969">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1969">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="27ffd-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="27ffd-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="27ffd-1971">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="27ffd-1971">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="27ffd-1972">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="27ffd-1972">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="27ffd-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="27ffd-1974">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="27ffd-1974">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="27ffd-1975">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-1975">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="27ffd-1976">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="27ffd-1976">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-1977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-1977">Az.Automation</span></span>
* <span data-ttu-id="27ffd-1978">Uppdaterade Get-AzAutomationJobOutputRecord för att hantera postvärden av typen JSON och Text.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1978">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="27ffd-1979">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="27ffd-1979">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="27ffd-1980">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="27ffd-1980">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="27ffd-1981">Ändrade beteende för Start-AzAutomationDscCompilationJob till att bara starta jobbet istället för att vänta på slutförandet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1981">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="27ffd-1982">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="27ffd-1982">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="27ffd-1983">Korrigering för Get-AzAutomationDscNode när using -Name returnerar alla noder.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1983">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="27ffd-1984">Nu returnerar den endast den matchande noden.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1984">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-1985">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-1985">Az.Compute</span></span>
* <span data-ttu-id="27ffd-1986">Lägg till parametrarna ProtectFromScaleIn och ProtectFromScaleSetAction i cmdleten Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="27ffd-1986">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="27ffd-1987">Nu är standardinställningen att vimpelparametern New-AzVM använder en tillgänglig plats om USA, östra inte stöds</span><span class="sxs-lookup"><span data-stu-id="27ffd-1987">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-1989">Uppdatera ADLS-sdk för att använda httpclient, integrera dataplanstestning med Azure-ramverk</span><span class="sxs-lookup"><span data-stu-id="27ffd-1989">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-1990">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-1990">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-1991">Korrigera felaktiga parameternamn i hjälpexempel</span><span class="sxs-lookup"><span data-stu-id="27ffd-1991">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-1992">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-1992">Az.Network</span></span>
* <span data-ttu-id="27ffd-1993">Lägg till flaggan DisableBgpRoutePropagation i utdata för effektiv routningstabell</span><span class="sxs-lookup"><span data-stu-id="27ffd-1993">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="27ffd-1994">Uppdaterad cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27ffd-1994">Updated cmdlet:</span></span>
        - <span data-ttu-id="27ffd-1995">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="27ffd-1995">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="27ffd-1996">Åtgärda dubbelstreck i dokumentationen New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="27ffd-1996">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-1997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-1997">Az.Resources</span></span>
* <span data-ttu-id="27ffd-1998">Lägg till ny cmdlet Get-AzureRmDenyAssignment för att hämta tilldelningsnekanden</span><span class="sxs-lookup"><span data-stu-id="27ffd-1998">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-1999">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2000">Döp om Advanced Threat Protection-cmdletar för Advanced Data Security och aktivera Vulnerability Assessment som standard</span><span class="sxs-lookup"><span data-stu-id="27ffd-2000">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="27ffd-2001">2.0.0 – maj 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2001">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2002">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-2003">Uppdatera autentiseringsbiblioteket för att åtgärda ADFS-problem med autentisering av användarnamn/lösenord</span><span class="sxs-lookup"><span data-stu-id="27ffd-2003">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-2004">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2004">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-2005">Visa endast Bing-ansvarsfriskrivning för Bing-sökningstjänster.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2005">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="27ffd-2006">Förbättra felmeddelande när det inte går att skapa konton.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2006">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2007">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2008">Funktion för närhetsplaceringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2008">Proximity placement group feature.</span></span>
    - <span data-ttu-id="27ffd-2009">Följande nya cmdletar har lagts till:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-2009">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="27ffd-2010">Den nya parametern ProximityPlacementGroupId har lagts till i följande cmdletar:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-2010">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="27ffd-2011">Parametern StorageAccountType har lagts till i New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2011">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="27ffd-2012">TargetRegion för New-AzGalleryImageVersion kan innehålla StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2012">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="27ffd-2013">Växlingsparametern SkipShutdown har lagts till i Stop-AzVM och Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27ffd-2013">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="27ffd-2014">Icke-bakåtkompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2014">Breaking changes</span></span>
    - <span data-ttu-id="27ffd-2015">Set-AzVMBootDiagnostics har ändrats till Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2015">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="27ffd-2016">Export-AzLogAnalyticThrottledRequests har ändrats till Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2016">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="27ffd-2017">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="27ffd-2017">Az.DeploymentManager</span></span>
* <span data-ttu-id="27ffd-2018">De första allmänt tillgängliga versionerna av cmdletar för Distributionshanteraren i Azure</span><span class="sxs-lookup"><span data-stu-id="27ffd-2018">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="27ffd-2019">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="27ffd-2019">Az.Dns</span></span>
* <span data-ttu-id="27ffd-2020">Automatisk delegering av DNS för NameServer</span><span class="sxs-lookup"><span data-stu-id="27ffd-2020">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="27ffd-2021">Det överordnade zonnamnet kan användas som ytterligare valfri parameter i cmdleten för att skapa DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2021">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="27ffd-2022">Lägger till NS-poster för en nyligen skapad underordnad zon i den överordnade zonen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2022">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27ffd-2023">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-2023">Az.FrontDoor</span></span>
* <span data-ttu-id="27ffd-2024">De första allmänt tillgängliga versionerna av cmdletar för Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-2024">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="27ffd-2025">Byt namn på WAF-cmdletar så att de omfattar ”Waf”</span><span class="sxs-lookup"><span data-stu-id="27ffd-2025">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-2026">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-2026">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-2027">Två cmdletar har tagits bort:</span><span class="sxs-lookup"><span data-stu-id="27ffd-2027">Removed two cmdlets:</span></span>
    - <span data-ttu-id="27ffd-2028">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27ffd-2028">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="27ffd-2029">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27ffd-2029">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="27ffd-2030">En ny cmdlet har lagts till, Set-AzHDInsightGatewayCredential, som ersätter Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27ffd-2030">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="27ffd-2031">Uppdatera cmdleten Get-AzHDInsightJobOutput för att skilja mellan läsarrollen och HDInsight-operatörsrollen:</span><span class="sxs-lookup"><span data-stu-id="27ffd-2031">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="27ffd-2032">Användare med läsarrollen måste uttryckligen ange parametern ”DefaultStorageAccountKey”, annars uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2032">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="27ffd-2033">Användare med HDInsight-operatörsrollen påverkas inte.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2033">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-2034">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-2035">Nya cmdletar för SQR API (schemalagd frågeregel)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2035">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="27ffd-2036">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="27ffd-2036">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="27ffd-2037">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-2037">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="27ffd-2038">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="27ffd-2038">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="27ffd-2039">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2039">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="27ffd-2040">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="27ffd-2040">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="27ffd-2041">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="27ffd-2041">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="27ffd-2042">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2042">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27ffd-2043">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2043">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27ffd-2044">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2044">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27ffd-2045">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2045">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27ffd-2046">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2046">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27ffd-2047">[Mer](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information om SQR API</span><span class="sxs-lookup"><span data-stu-id="27ffd-2047">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="27ffd-2048">Az.Monitor.md har uppdaterats för att omfatta cmdletar för måttbaserade aviseringsregler i GenV2 (inte klassiska)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2048">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-2049">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2049">Az.Network</span></span>
* <span data-ttu-id="27ffd-2050">Lägg till stöd för NAT Gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="27ffd-2050">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="27ffd-2051">Nya cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2051">New cmdlets</span></span>
        - <span data-ttu-id="27ffd-2052">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-2052">New-AzNatGateway</span></span>
        - <span data-ttu-id="27ffd-2053">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-2053">Get-AzNatGateway</span></span>
        - <span data-ttu-id="27ffd-2054">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-2054">Set-AzNatGateway</span></span>
        - <span data-ttu-id="27ffd-2055">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-2055">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="27ffd-2056">Uppdaterade cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2056">Updated cmdlets</span></span>
        - <span data-ttu-id="27ffd-2057">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="27ffd-2057">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="27ffd-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="27ffd-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="27ffd-2059">Nedanstående kommandon för funktionen har uppdaterats: Ange/ta bort anpassade vägar på Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2059">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="27ffd-2060">New-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ställa in adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2060">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="27ffd-2061">Set-AzVirtualNetworkGateway har uppdaterats: Den valfria parametern -CustomRoute har lagts till för att ange adressprefix som anpassade vägar för att ange gateway.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2061">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27ffd-2062">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-2062">Az.PolicyInsights</span></span>
* <span data-ttu-id="27ffd-2063">Stöd för att fråga efter information om principutvärdering.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2063">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="27ffd-2064">Lägg till parametern ”-Expand” för Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2064">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="27ffd-2065">Stöd för -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2065">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-2066">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2066">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-2067">Stöd för att dela prenumeration mellan Azure och Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2067">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="27ffd-2068">Markering av kommande icke-bakåtkompatibla ändringar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2068">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="27ffd-2069">Korrigering för återställningsplan och åtgärdsplan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2069">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="27ffd-2070">Korrigering för mappning av uppdateringsnätverk i Azure Site Recovery för Azure till Azure.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2070">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="27ffd-2071">Korrigering för instruktioner för uppdateringsskydd i Azure Site Recovery för Azure till Azure för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2071">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="27ffd-2072">Andra mindre korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2072">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="27ffd-2073">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="27ffd-2073">Az.Relay</span></span>
* <span data-ttu-id="27ffd-2074">Korrigera stavfel i kundriktade meddelanden</span><span class="sxs-lookup"><span data-stu-id="27ffd-2074">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27ffd-2075">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27ffd-2075">Az.ServiceBus</span></span>
* <span data-ttu-id="27ffd-2076">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="27ffd-2076">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2077">Az.Storage</span></span>
* <span data-ttu-id="27ffd-2078">Uppgradera till lagringsklientbiblioteket 10.0.1 (namnområdet för alla objekt från detta SDK ändras från ”Microsoft.WindowsAzure.Storage. *till ”Microsoft.Azure.Storage.* ”)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2078">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="27ffd-2079">Uppgradera till Microsoft.Azure.Management.Storage 11.0.0 för att stödja den nya API-versionen 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2079">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="27ffd-2080">Standardlagringskontot i Skapa lagringskonto ändras från ”Storage” till ”StorageV2”</span><span class="sxs-lookup"><span data-stu-id="27ffd-2080">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="27ffd-2081">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-2081">New-AzStorageAccount</span></span>
* <span data-ttu-id="27ffd-2082">Ändra lagringskontots cmdlet-utdata Sku.Name för att passa med indata-SkuName genom att lägga till ”-”. Till exempel ändras ”StandardLRS” till ”Standard_LRS”</span><span class="sxs-lookup"><span data-stu-id="27ffd-2082">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="27ffd-2083">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-2083">New-AzStorageAccount</span></span>
    - <span data-ttu-id="27ffd-2084">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-2084">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="27ffd-2085">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-2085">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-2086">Az.Websites</span></span>
* <span data-ttu-id="27ffd-2087">Egenskapen ”typ” konfigureras nu för PSSite-objekt som returneras av Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2087">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="27ffd-2088">Get-AzWebApp\*Metrics och Get-AzAppServicePlanMetrics markeras som inaktuella</span><span class="sxs-lookup"><span data-stu-id="27ffd-2088">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="27ffd-2089">1.8.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2089">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27ffd-2090">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2090">Highlights since the last major release</span></span>
* <span data-ttu-id="27ffd-2091">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2091">General availability of `Az` module</span></span>
* <span data-ttu-id="27ffd-2092">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="27ffd-2092">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="27ffd-2093">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="27ffd-2093">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="27ffd-2094">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2094">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="27ffd-2095">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2095">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27ffd-2096">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2096">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="27ffd-2097">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2097">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-2098">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2098">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-2099">Uppdatera Uninstall-AzureRm för att ta bort moduler i Mac på ett korrekt sätt</span><span class="sxs-lookup"><span data-stu-id="27ffd-2099">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27ffd-2100">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27ffd-2100">Az.Batch</span></span>
* <span data-ttu-id="27ffd-2101">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2101">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27ffd-2102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27ffd-2102">Az.Cdn</span></span>
* <span data-ttu-id="27ffd-2103">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2103">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-2104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2104">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-2105">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2105">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2106">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2106">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2107">Åtgärda problem med AEM-installationen om resurs-ID:n för diskar innehåller resourcegroups i gemener i resurs-ID:n</span><span class="sxs-lookup"><span data-stu-id="27ffd-2107">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="27ffd-2108">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2108">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27ffd-2109">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="27ffd-2109">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-2110">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-2111">Lägg till SsisProperties om NodeCount inte är null för hanterad integreringskörning.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2111">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-2112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-2112">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-2113">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27ffd-2114">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27ffd-2114">Az.EventGrid</span></span>
* <span data-ttu-id="27ffd-2115">Hjälptexten för slutpunkten har uppdaterats för att visa att resurser ska skapas innan cmdletarna för att skapa/uppdatera händelseprenumerationer används.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2115">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27ffd-2116">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-2116">Az.EventHub</span></span>
* <span data-ttu-id="27ffd-2117">Nya cmdletar har lagts till för NetworkRuleSet för namnområden</span><span class="sxs-lookup"><span data-stu-id="27ffd-2117">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27ffd-2118">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27ffd-2118">Az.HDInsight</span></span>
* <span data-ttu-id="27ffd-2119">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-2120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-2120">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-2121">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-2122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-2122">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-2123">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27ffd-2124">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="27ffd-2124">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="27ffd-2125">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="27ffd-2125">Az.MachineLearning</span></span>
* <span data-ttu-id="27ffd-2126">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="27ffd-2127">Az.Media</span><span class="sxs-lookup"><span data-stu-id="27ffd-2127">Az.Media</span></span>
* <span data-ttu-id="27ffd-2128">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-2129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-2129">Az.Monitor</span></span>
  * <span data-ttu-id="27ffd-2130">Nya cmdletar för måttbaserad aviseringsregel i GenV2 (inte klassisk)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2130">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="27ffd-2131">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="27ffd-2131">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="27ffd-2132">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="27ffd-2132">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="27ffd-2133">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="27ffd-2133">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="27ffd-2134">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="27ffd-2134">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="27ffd-2135">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="27ffd-2135">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="27ffd-2136">Monitor SDK har uppdaterats till version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="27ffd-2136">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-2137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2137">Az.Network</span></span>
* <span data-ttu-id="27ffd-2138">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27ffd-2139">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="27ffd-2139">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="27ffd-2140">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="27ffd-2140">Az.NotificationHubs</span></span>
* <span data-ttu-id="27ffd-2141">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-2142">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-2142">Az.OperationalInsights</span></span>
* <span data-ttu-id="27ffd-2143">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="27ffd-2144">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="27ffd-2144">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="27ffd-2145">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2145">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-2146">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2146">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-2147">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2147">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27ffd-2148">Tabellformatet för SQL i virtuella Azure-datorer har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2148">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="27ffd-2149">En alternativ metod för att hämta platser i AzureFileShare har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2149">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="27ffd-2150">ScheduleRunDays i SchedulePolicy-objekt har uppdaterats enligt tidszon</span><span class="sxs-lookup"><span data-stu-id="27ffd-2150">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27ffd-2151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27ffd-2151">Az.RedisCache</span></span>
* <span data-ttu-id="27ffd-2152">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2153">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2154">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="27ffd-2154">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2155">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2156">Ersätt Monitor SDK-beroende med vanlig kod</span><span class="sxs-lookup"><span data-stu-id="27ffd-2156">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="27ffd-2157">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27ffd-2158">Förbättrad process för klassificering av flera kolumner.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2158">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="27ffd-2159">Inkludera SKU-egenskaper (SKU-namn, serie, kapacitet) i svaret från Get-AzSqlServerServiceObjective och formatera som tabell som standard.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2159">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="27ffd-2160">Möjlighet att använda Get-AzSqlServerServiceObjective efter plats utan att behöva en redan befintlig server i regionen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2160">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="27ffd-2161">Stöd för tidszonsparametern när hanterade instanser skapas.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2161">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="27ffd-2162">Åtgärda dokumentationen för jokertecken</span><span class="sxs-lookup"><span data-stu-id="27ffd-2162">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-2163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-2163">Az.Websites</span></span>
* <span data-ttu-id="27ffd-2164">åtgärdar Set-AzWebApp och Set-AzWebAppSlot så att de inte tar bort taggar vid körning</span><span class="sxs-lookup"><span data-stu-id="27ffd-2164">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="27ffd-2165">Cmdletar med pluralsubstantiv har uppdaterats till singularis och namn i plural har gjorts inaktuella.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27ffd-2166">SDK för WebSites har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2166">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="27ffd-2167">Egenskapen AdminSiteName har tagits bort från PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2167">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="27ffd-2168">1.7.0 – april 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2168">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27ffd-2169">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2169">Highlights since the last major release</span></span>
* <span data-ttu-id="27ffd-2170">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2170">General availability of `Az` module</span></span>
* <span data-ttu-id="27ffd-2171">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="27ffd-2171">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="27ffd-2172">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="27ffd-2172">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="27ffd-2173">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2173">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="27ffd-2174">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2174">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27ffd-2175">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2175">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="27ffd-2176">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2176">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27ffd-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2177">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-2178">Add-AzEnvironment och Set-AzEnvironment har uppdaterats för att godkänna parametern AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="27ffd-2178">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27ffd-2179">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2179">Az.AnalysisServices</span></span>
* <span data-ttu-id="27ffd-2180">ServiceClient används i cmdletar för dataplan och den ursprungliga autentiseringslogiken har tagits bort</span><span class="sxs-lookup"><span data-stu-id="27ffd-2180">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="27ffd-2181">Add-AzureASAccount används för omslutning av Connect-AzAccount för att undvika en icke-bakåtkompatibel ändring</span><span class="sxs-lookup"><span data-stu-id="27ffd-2181">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-2182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-2182">Az.Automation</span></span>
* <span data-ttu-id="27ffd-2183">Buggen för cmdleten New-AzAutomationSoftwareUpdateConfiguration för inkluderingar har åtgärdats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2183">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="27ffd-2184">Nu bör parametern IncludedKbNumber och IncludedPackageNameMask fungera.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2184">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="27ffd-2185">Felkorrigering för dynamiska grupper i uppdateringshanteringen för azure automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-2185">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2186">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2187">Lägg till parametern HyperVGeneration i New-AzDiskConfig och New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-2187">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="27ffd-2188">Tillåt att virtuella datorer skapas med galleribilder från andra klientorganisationer.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2188">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="27ffd-2189">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27ffd-2189">Az.ContainerInstance</span></span>
* <span data-ttu-id="27ffd-2190">Ett problem har åtgärdats i parametern -Command för New-AzContainerGroup som lade till ett avslutande tomt argument</span><span class="sxs-lookup"><span data-stu-id="27ffd-2190">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-2191">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-2191">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-2192">ADF .Net SDK-versionen har uppdaterats till 3.0.2</span><span class="sxs-lookup"><span data-stu-id="27ffd-2192">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="27ffd-2193">Cmdleten Set-AzDataFactoryV2 har uppdaterats med extra parametrar för inställningar som rör RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2193">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2194">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2195">Förbättra hanteringen av providrar för Get-AzResource när parametrarna -ResourceId eller -ResourceGroupName, -Name och -ResourceType tillhandahålls</span><span class="sxs-lookup"><span data-stu-id="27ffd-2195">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="27ffd-2196">Förbättra felhanteringen för ”Test-AzDeployment” och ”Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-2196">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="27ffd-2197">Hantera fel utanför distributionsvalideringen och ta med dem i kommandoutdata istället</span><span class="sxs-lookup"><span data-stu-id="27ffd-2197">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="27ffd-2198">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="27ffd-2198">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="27ffd-2199">Lägg till växlingsparametern -IgnoreDynamicParameters till en uppsättning av cmdletar för distribution för att hoppa över fråga i skript och jobbscenarier</span><span class="sxs-lookup"><span data-stu-id="27ffd-2199">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="27ffd-2200">Mer information här: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="27ffd-2200">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2201">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2202">Stöd för dataklassificering av databaser.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2202">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-2203">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2203">Az.Storage</span></span>
* <span data-ttu-id="27ffd-2204">Rapportera detaljfel när lagringskontext skapas med parametern -UseConnectedAccount, men utan inloggning på Azure-kontot</span><span class="sxs-lookup"><span data-stu-id="27ffd-2204">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="27ffd-2205">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="27ffd-2205">New-AzStorageContext</span></span>
* <span data-ttu-id="27ffd-2206">Stöd för att hantera Blob Service-egenskaper för ett angivet lagringskonto med API:et för hanteringsplan</span><span class="sxs-lookup"><span data-stu-id="27ffd-2206">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="27ffd-2207">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="27ffd-2207">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="27ffd-2208">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="27ffd-2208">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="27ffd-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="27ffd-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="27ffd-2211">Stöd för -AsJob-cmdletar för att ladda upp och ladda ned blobar och filer</span><span class="sxs-lookup"><span data-stu-id="27ffd-2211">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="27ffd-2212">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27ffd-2212">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="27ffd-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27ffd-2213">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="27ffd-2214">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27ffd-2214">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="27ffd-2215">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27ffd-2215">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="27ffd-2216">1.6.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2216">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27ffd-2217">Höjdpunkter sedan den senaste större uppdateringen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2217">Highlights since the last major release</span></span>
* <span data-ttu-id="27ffd-2218">Allmän tillgänglighet för `Az`-modulen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2218">General availability of `Az` module</span></span>
* <span data-ttu-id="27ffd-2219">Mer information om `Az`-modulen finns här: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="27ffd-2219">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="27ffd-2220">Ifyllning för Location, ResourceGroup och ResourceName har lagts till: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="27ffd-2220">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="27ffd-2221">Stöd för jokertecken för Get-cmdletar för Az.Compute och Az.Network har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2221">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="27ffd-2222">Endast interaktiv autentisering och autentisering med användarnamn/lösenord för Windows PowerShell 5.1 har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2222">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27ffd-2223">Stöd för Python 2-runbookflöden i Az.Automation har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2223">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="27ffd-2224">Az.LogicApp: Nya cmdletar för integrationskontosammansättningar och batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2224">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-2225">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-2225">Az.Automation</span></span>
* <span data-ttu-id="27ffd-2226">Azure Automation – ändring av uppdateringshantering för stöd för de nya funktionerna:</span><span class="sxs-lookup"><span data-stu-id="27ffd-2226">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="27ffd-2227">Dynamisk gruppering</span><span class="sxs-lookup"><span data-stu-id="27ffd-2227">Dynamic grouping</span></span>
    * <span data-ttu-id="27ffd-2228">För-/efterskrift</span><span class="sxs-lookup"><span data-stu-id="27ffd-2228">Pre-Post script</span></span>
    * <span data-ttu-id="27ffd-2229">Inställning för omstart</span><span class="sxs-lookup"><span data-stu-id="27ffd-2229">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2230">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2231">Åtgärda problem med sökvägsmatchning i Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="27ffd-2231">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="27ffd-2232">Uppdatera Compute-klientbibliotek till 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2232">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-2233">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-2233">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-2234">Stöd för jokertecken för KeyVault-cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2234">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-2235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2235">Az.Network</span></span>
* <span data-ttu-id="27ffd-2236">Lägg till stöd för Threat Intelligence för Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="27ffd-2236">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="27ffd-2237">Lägg till resurs för brandväggsprincip på översta nivå och anpassade regler för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-2237">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-2238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2238">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-2239">SnapshotRetentionInDays har lagts till i Azure-principen för virtuella datorer för stöd av Instant RP</span><span class="sxs-lookup"><span data-stu-id="27ffd-2239">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="27ffd-2240">Pipe-stöd för avregistrering av container har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2240">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2241">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2242">Uppdatera stöd för jokertecken för Get-AzResource och Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="27ffd-2242">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="27ffd-2243">Uppdatera autentiseringsuppgifter som används vid allmänna anrop till ARM</span><span class="sxs-lookup"><span data-stu-id="27ffd-2243">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-2244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2244">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2245">Cmdlet-parametern (ExcludeDetectionType) för Hotidentifiering ändrades från DetectionType till sträng[] för att framtidssäkra den när nya DetectionTypes läggs till, och även för att stödja automatisk ifyllning.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2245">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-2246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2246">Az.Storage</span></span>
* <span data-ttu-id="27ffd-2247">Stöd för att hämta/ange/ta bort hanteringsprincip på ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-2247">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="27ffd-2248">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-2248">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="27ffd-2249">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-2249">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="27ffd-2250">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-2250">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="27ffd-2251">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="27ffd-2251">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="27ffd-2252">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="27ffd-2252">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="27ffd-2253">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2253">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-2254">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-2254">Az.Websites</span></span>
* <span data-ttu-id="27ffd-2255">Åtgärda fel med ARM-mall som avbryter kloning av alla platser med 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="27ffd-2255">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="27ffd-2256">1.5.0 – mars 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2256">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-2257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2257">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-2258">Lägg till kommandot Register-AzModule för stöd för AutoRest-genererade cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2258">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="27ffd-2259">Uppdatera exempel för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-2259">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-2260">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-2260">Az.Automation</span></span>
* <span data-ttu-id="27ffd-2261">Problem med att hämta vissa månadsscheman i flera Azure Automation-cmdletar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2261">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="27ffd-2262">Åtgärda problem med att Get-AzAutomationDscNode bara returnerar de 20 översta noderna.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2262">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="27ffd-2263">Nu returneras alla noder</span><span class="sxs-lookup"><span data-stu-id="27ffd-2263">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27ffd-2264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27ffd-2264">Az.Cdn</span></span>
* <span data-ttu-id="27ffd-2265">Nya Powershell-cmdletar för att aktivera/inaktivera anpassade domän-HTTPS har lagts till och de gamla har gjorts inaktuella</span><span class="sxs-lookup"><span data-stu-id="27ffd-2265">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2266">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2267">Lägg till stöd för jokertecken för Get-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2267">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-2268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-2268">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-2269">ADF .Net SDK-versionen har uppdaterats till 3.0.1</span><span class="sxs-lookup"><span data-stu-id="27ffd-2269">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27ffd-2270">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2270">Az.LogicApp</span></span>
* <span data-ttu-id="27ffd-2271">Åtgärda problemet med att ListWorkflows endast hämtar den första sidan med resultat</span><span class="sxs-lookup"><span data-stu-id="27ffd-2271">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-2272">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2272">Az.Network</span></span>
* <span data-ttu-id="27ffd-2273">Lägg till stöd för jokertecken för Network-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2273">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-2274">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2274">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-2275">Stöd har lagts till för SQL Server i virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="27ffd-2275">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="27ffd-2276">SDK-uppdatering</span><span class="sxs-lookup"><span data-stu-id="27ffd-2276">SDK Update</span></span>
* <span data-ttu-id="27ffd-2277">Get-ProtectableItem-incheckning i VMappContainer har tagits bort</span><span class="sxs-lookup"><span data-stu-id="27ffd-2277">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="27ffd-2278">Name och ServerName har lagts till som parametrar för Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="27ffd-2278">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2279">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2280">Lägg till parametern `-TemplateObject` i cmdletar för distribution</span><span class="sxs-lookup"><span data-stu-id="27ffd-2280">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="27ffd-2281">Mer information här: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="27ffd-2281">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="27ffd-2282">Åtgärda problem med piping av resultatet i `Get-AzResource` till `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="27ffd-2282">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="27ffd-2283">Mer information här: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="27ffd-2283">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="27ffd-2284">Åtgärda problem med ändring av JSON-datatyp när `Set-AzResource` körs</span><span class="sxs-lookup"><span data-stu-id="27ffd-2284">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="27ffd-2285">Mer information här: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="27ffd-2285">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-2286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2286">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2287">AuditingEndpointsCommunicator uppdateras.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2287">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="27ffd-2288">Åtgärdar beteendet hos ett gränsscenario när nya diagnostikinställningar skapas.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2288">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-2289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2289">Az.Storage</span></span>
* <span data-ttu-id="27ffd-2290">Stöd för BlockBlobStorage när Storage-konto skapas      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-2290">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="27ffd-2291">1.4.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2291">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="27ffd-2292">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2292">Az.AnalysisServices</span></span>
* <span data-ttu-id="27ffd-2293">Inaktuell AddAzureASAccount-cmdlet</span><span class="sxs-lookup"><span data-stu-id="27ffd-2293">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-2294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-2294">Az.Automation</span></span>
* <span data-ttu-id="27ffd-2295">Hjälpen för Import-AzAutomationDscNodeConfiguration har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2295">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="27ffd-2296">Konfigurationsnamnsvalidering har lagts till i cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2296">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="27ffd-2297">Förbättrad felhantering för cmdleten Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2297">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-2298">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2298">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-2299">CustomSubdomainName har lagts till som en ny valfri parameter för New-AzCognitiveServicesAccount, som används för att ange underdomän för resursen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2299">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2300">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2301">Problemet med ID-parameteruppsättningar har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2301">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="27ffd-2302">Get-AzVMExtension har uppdaterats så att alla installerade tillägg visas om parametern Name inte har angetts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2302">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="27ffd-2303">Parametrarna Tag och ResourceId har lagts till i cmdleten Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2303">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="27ffd-2304">Get-AzVmssVM utan instans-ID och med InstanceView kan visa virtuella VMSS-datorer med instansvyn.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2304">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-2305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-2305">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-2306">Cmdletar har lagts till för uppräkning och återställning av borttagna objekt i ADL</span><span class="sxs-lookup"><span data-stu-id="27ffd-2306">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27ffd-2307">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-2307">Az.EventHub</span></span>
* <span data-ttu-id="27ffd-2308">Ny boolesk egenskap SkipEmptyArchives har lagts till i Skip Empty Archives i CaptureDescription-klassen i Eventhub</span><span class="sxs-lookup"><span data-stu-id="27ffd-2308">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-2309">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-2309">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-2310">Taggning i Set-AzKeyVaultSecret har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2310">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27ffd-2311">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2311">Az.LogicApp</span></span>
* <span data-ttu-id="27ffd-2312">Grundläggande SKU har lagts till för Integrationskonton</span><span class="sxs-lookup"><span data-stu-id="27ffd-2312">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="27ffd-2313">XSLT 2.0, XSLT 3.0 och Flytande mappningstyper har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2313">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="27ffd-2314">Nya cmdletar för integrationskontosammansättningar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2314">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="27ffd-2315">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="27ffd-2315">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="27ffd-2316">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="27ffd-2316">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="27ffd-2317">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="27ffd-2317">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="27ffd-2318">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="27ffd-2318">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="27ffd-2319">Nya cmdletar för batchkonfiguration för integrationskonto</span><span class="sxs-lookup"><span data-stu-id="27ffd-2319">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="27ffd-2320">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2320">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="27ffd-2321">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2321">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="27ffd-2322">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2322">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="27ffd-2323">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2323">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="27ffd-2324">Logic App-SDK har uppdaterats till version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-2324">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27ffd-2325">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-2325">Az.Monitor</span></span>
* <span data-ttu-id="27ffd-2326">Hjälpen för Get-AzMetric har uppdaterats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2326">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-2327">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2327">Az.Network</span></span>
* <span data-ttu-id="27ffd-2328">Hjälpexempel för Add-AzApplicationGatewayCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2328">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="27ffd-2330">Ytterligare stöd för datakällorna New och Get ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2330">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="27ffd-2331">Ny ApplicationInsights-typ har lagts till för att ge stöd för ”Get specific” och ”Get all” för ApplicationInsights-datakällor för angiven arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2331">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="27ffd-2332">Cmdleten New-AzOperationalInsightsApplicationInsightsDataSource har lagts till för att skapa datakälla med angivna parametrar för Application Insights-resurs: subscription Id, resourceGroupName och name.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2332">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2333">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2334">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="27ffd-2334">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="27ffd-2335">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="27ffd-2335">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="27ffd-2336">Korrigering av problemet https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="27ffd-2336">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="27ffd-2337">Fel som gör att KeyCredentials inte kan skapas upprepade gånger har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2337">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2338">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2339">Lägg till stöd för hyperskalanivån för SQL DB</span><span class="sxs-lookup"><span data-stu-id="27ffd-2339">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="27ffd-2340">Ett fel har åtgärdats där återställningen kunde misslyckas på grund av onödiga inställningsegenskaper i restore-förfrågan</span><span class="sxs-lookup"><span data-stu-id="27ffd-2340">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-2341">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-2341">Az.Websites</span></span>
* <span data-ttu-id="27ffd-2342">Rätt exempel i Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="27ffd-2342">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="27ffd-2343">1.3.0 – februari 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2343">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-2344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2344">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-2345">Uppdatera till den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="27ffd-2345">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27ffd-2346">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2346">Az.AnalysisServices</span></span>
<span data-ttu-id="27ffd-2347">Allmän tillgänglighet för Az.AnalysisServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2347">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2348">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2349">AEM-tillägg: Lägg till stöd för UltraSSD-, P60-, P70- och P80-diskar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2349">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="27ffd-2350">Uppdatera hjälpbeskrivning för Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="27ffd-2350">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="27ffd-2351">Uppdatera hjälpbeskrivning och exempel för Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2351">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2352">Az.RecoveryServices</span></span>
<span data-ttu-id="27ffd-2353">Allmän tillgänglighet för Az.RecoveryServices-modulen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2353">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2354">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2355">Korrigera taggar för resursgrupper</span><span class="sxs-lookup"><span data-stu-id="27ffd-2355">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="27ffd-2356">Mer information här: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="27ffd-2356">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="27ffd-2357">Åtgärda problem där `Get-AzureRmRoleAssignment` inte respekterar -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="27ffd-2357">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="27ffd-2358">Mer information här: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="27ffd-2358">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-2359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2359">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2360">Lägga till Get/Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27ffd-2360">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="27ffd-2361">Åtgärda problem där ett nullref-undantag uppstår när du kör SQL-cmdletar och inte är inloggad på ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="27ffd-2361">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="27ffd-2362">Åtgärda nullref-undantag i Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="27ffd-2362">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="27ffd-2363">1.2.1 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2363">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-2364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2364">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-2365">Version med rätt version av autentisering</span><span class="sxs-lookup"><span data-stu-id="27ffd-2365">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27ffd-2366">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2366">Az.AnalysisServices</span></span>
* <span data-ttu-id="27ffd-2367">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="27ffd-2367">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="27ffd-2369">Version med uppdaterat autentiseringsberoende</span><span class="sxs-lookup"><span data-stu-id="27ffd-2369">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="27ffd-2370">1.2.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2370">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2371">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-2372">Lägga till interaktiv autentisering och autentisering med användarnamn/lösenord för endast Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="27ffd-2372">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27ffd-2373">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2373">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27ffd-2374">Lägga till varningsmeddelande i PS Core för Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="27ffd-2374">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="27ffd-2375">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27ffd-2375">Az.Aks</span></span>
* <span data-ttu-id="27ffd-2376">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2376">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27ffd-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-2377">Az.Automation</span></span>
* <span data-ttu-id="27ffd-2378">Stöd för Python 2-runbookflöden har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2378">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="27ffd-2379">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2379">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27ffd-2380">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27ffd-2380">Az.Cdn</span></span>
* <span data-ttu-id="27ffd-2381">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2381">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2382">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2383">Lägga till cmdleten Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2383">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="27ffd-2384">Lägga till TempDisk-parameter i Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27ffd-2384">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="27ffd-2385">Korrigera varningsmeddelande för New-AzVM</span><span class="sxs-lookup"><span data-stu-id="27ffd-2385">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="27ffd-2386">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27ffd-2386">Az.ContainerRegistry</span></span>
* <span data-ttu-id="27ffd-2387">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2387">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27ffd-2388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27ffd-2388">Az.DataFactory</span></span>
* <span data-ttu-id="27ffd-2389">ADF .Net SDK-versionen har uppdaterats till 3.0.0</span><span class="sxs-lookup"><span data-stu-id="27ffd-2389">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-2390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-2390">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-2391">Åtgärda problem med ADLS-slutpunkt vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="27ffd-2391">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="27ffd-2392">Mer information här: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="27ffd-2392">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="27ffd-2393">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2393">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-2394">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-2394">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-2395">Lägga till kodningsformat i cmdleten Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2395">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27ffd-2396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-2396">Az.KeyVault</span></span>
* <span data-ttu-id="27ffd-2397">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2397">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-2398">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2398">Az.Network</span></span>
* <span data-ttu-id="27ffd-2399">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2399">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2400">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2401">Åtgärda felaktiga exempel i referensdokumentationen ”New-AzADAppCredential” och ”New-AzADSpCredential”</span><span class="sxs-lookup"><span data-stu-id="27ffd-2401">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="27ffd-2402">Åtgärda problem där sökvägen för parametern ”-TemplateFile” inte omvandlas innan cmdletarna för distribution i resursgruppen körs</span><span class="sxs-lookup"><span data-stu-id="27ffd-2402">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="27ffd-2403">Az.Resources: Korrigera dokumentationen om standardvärdet för New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="27ffd-2403">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="27ffd-2404">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="27ffd-2404">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="27ffd-2405">Az.Resources: Korrigering av problemet https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="27ffd-2405">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="27ffd-2406">Åtgärda formateringsproblemet med objektet ”PSResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="27ffd-2406">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="27ffd-2407">Mer information här: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="27ffd-2407">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27ffd-2408">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-2408">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-2409">Återställ när ett certifikat läggs till i en Virtual Machine Scale Sets-modell men ett undantag genereras. Detta har gjorts för att åtgärda följande fel: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="27ffd-2409">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="27ffd-2410">Korrigera några felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2410">Fix some error messages.</span></span>
* <span data-ttu-id="27ffd-2411">Korrigering av skapande av kluster med ARM-mall som är standard för New-AzServiceFabriCluster som inte fungerade med migrering till Az.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2411">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="27ffd-2412">Korrigering av tilläggning av kluster/programcertifikat så att endast VM Scale Sets som motsvarar klustret läggs till genom att kontrollera ID för klustret i tillägget.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2412">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="27ffd-2413">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="27ffd-2413">Az.SignalR</span></span>
* <span data-ttu-id="27ffd-2414">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2414">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-2415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2415">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2416">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2416">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27ffd-2417">Uppdaterad parameterbeskrivning för LicenseType-parameter med möjliga värden</span><span class="sxs-lookup"><span data-stu-id="27ffd-2417">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="27ffd-2418">Korrigering för att uppdatera hanterad instansidentitet som inte fungerar när det är den enda uppdaterade egenskapen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2418">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="27ffd-2419">Stöd för anpassad sortering på hanterad instans</span><span class="sxs-lookup"><span data-stu-id="27ffd-2419">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-2420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2420">Az.Storage</span></span>
* <span data-ttu-id="27ffd-2421">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2421">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27ffd-2422">Tillhandahåll detaljerat felmeddelande när en användare försöker hämta/konfigurera klassisk loggning/mått på ett Premium Storage-konto eftersom Premium Storage-kontot inte har stöd för klassisk loggning/mått.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2422">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="27ffd-2423">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="27ffd-2423">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="27ffd-2424">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="27ffd-2424">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="27ffd-2425">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="27ffd-2425">Az.TrafficManager</span></span>
* <span data-ttu-id="27ffd-2426">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2426">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-2427">Az.Websites</span></span>
* <span data-ttu-id="27ffd-2428">Uppdatera felaktiga URL:er för onlinehjälp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27ffd-2429">Korrigerar ”New-AzWebAppSSLBinding” så att certifikatet laddas upp till rätt resursgrupp och plats om appen finns i en ASE.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2429">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="27ffd-2430">Korrigerar ”New-AzWebAppSSLBinding” så att taggarna inte skrivs över på en bindning av ett SSL-certifikat till en app</span><span class="sxs-lookup"><span data-stu-id="27ffd-2430">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="27ffd-2431">1.1.0 – januari 2019</span><span class="sxs-lookup"><span data-stu-id="27ffd-2431">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27ffd-2432">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2432">Az.Accounts</span></span>
* <span data-ttu-id="27ffd-2433">Lade till omfattningen ”Lokal” till Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="27ffd-2433">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2434">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2435">Namn är nu valfritt i ID-parametern för Restart/Start/Stop/Remove/Set-AzVM och Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2435">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="27ffd-2436">Uppdaterade beskrivningen av ID i hjälpfiler</span><span class="sxs-lookup"><span data-stu-id="27ffd-2436">Updated the description of ID in help files</span></span>
* <span data-ttu-id="27ffd-2437">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2437">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-2438">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-2438">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-2439">Uppdatera sdk-versionen av dataplanet till 1.1.14 för SDK-korrigeringar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2439">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="27ffd-2440">Korrigerade hanteringen av negativ accesstime och modificationtime för getfilestatus och liststatus; korrigera asynkront annulleringstoken</span><span class="sxs-lookup"><span data-stu-id="27ffd-2440">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27ffd-2441">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27ffd-2441">Az.EventGrid</span></span>
* <span data-ttu-id="27ffd-2442">Uppdaterat för användning av API-versionen 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2442">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="27ffd-2443">Uppdaterade följande cmdletar för att stödja nytt scenario i API-versionen 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="27ffd-2443">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="27ffd-2444">New-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="27ffd-2444">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="27ffd-2445">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="27ffd-2445">Event Time-To-Live,</span></span>
        - <span data-ttu-id="27ffd-2446">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="27ffd-2446">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="27ffd-2447">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2447">Dead letter endpoint.</span></span>
    - <span data-ttu-id="27ffd-2448">Update-AzureRmEventGridSubscription: Lade till ny valfria parametrar för att ange:</span><span class="sxs-lookup"><span data-stu-id="27ffd-2448">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="27ffd-2449">Time-To-Live för händelse,</span><span class="sxs-lookup"><span data-stu-id="27ffd-2449">Event Time-To-Live,</span></span>
        - <span data-ttu-id="27ffd-2450">Maximalt antal leveransförsök för händelserna,</span><span class="sxs-lookup"><span data-stu-id="27ffd-2450">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="27ffd-2451">Slutpunkt för obeställbar meddelanden.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2451">Dead letter endpoint.</span></span>
* <span data-ttu-id="27ffd-2452">Lade till nya enum-värden (storageQueue och hybridConnection) för alternativet EndpointType i cmdletarna New-AzureRmEventGridSubscription och Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2452">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="27ffd-2453">Visa varningsmeddelanden om skapande eller uppdatering av händelseprenumerationen förväntas medföra manuell åtgärd från användaren.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2453">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27ffd-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-2454">Az.IotHub</span></span>
* <span data-ttu-id="27ffd-2455">Har uppdaterats till den senaste versionen av SDK:n lotHub</span><span class="sxs-lookup"><span data-stu-id="27ffd-2455">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27ffd-2456">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2456">Az.LogicApp</span></span>
* <span data-ttu-id="27ffd-2457">Get-AzLogicApp visar en lista över alla som inte har angivet namn</span><span class="sxs-lookup"><span data-stu-id="27ffd-2457">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2458">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2459">Åtgärdade problem med parameteruppsättningen när parametrarna -ODataQuery och -ResourceId anges för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="27ffd-2459">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="27ffd-2460">Mer information här: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="27ffd-2460">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="27ffd-2461">Åtgärdade hantering av parametern -Custom i New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="27ffd-2461">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="27ffd-2462">Korrigerade stavfel i New-AzDeployment-dokumentationen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2462">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="27ffd-2463">Gjorde parametern -MailNickname obligatorisk för New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="27ffd-2463">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="27ffd-2464">Mer information här: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="27ffd-2464">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="27ffd-2465">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="27ffd-2465">Az.SignalR</span></span>
* <span data-ttu-id="27ffd-2466">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2466">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-2467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2467">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2468">Konverterade lagringshanteringsklientens beroende av den normala SDK-implementeringen.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2468">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27ffd-2469">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2469">Az.Storage</span></span>
* <span data-ttu-id="27ffd-2470">Angav StorageAccountName för lagringskontext som det verkliga namnet på lagringskontot när det skapas med Sas Token, OAuth eller Anonymous</span><span class="sxs-lookup"><span data-stu-id="27ffd-2470">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="27ffd-2471">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="27ffd-2471">New-AzStorageContext</span></span>
* <span data-ttu-id="27ffd-2472">Skapade Sas Token för Blob Snapshot-objekt med parametern -FullUri, åtgärdade den returnerade URI:n så att den blir URI för ögonblicksbild</span><span class="sxs-lookup"><span data-stu-id="27ffd-2472">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="27ffd-2473">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="27ffd-2473">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-2474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-2474">Az.Websites</span></span>
* <span data-ttu-id="27ffd-2475">Åtgärdade en bugg i datumparsningen i Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="27ffd-2475">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="27ffd-2476">Åtgärdade problemet med bakåtkompatibilitet med modulen Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2476">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="27ffd-2477">1.0.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="27ffd-2477">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="27ffd-2478">Allmänt</span><span class="sxs-lookup"><span data-stu-id="27ffd-2478">General</span></span>

- <span data-ttu-id="27ffd-2479">Allmän tillgänglighet för Az-modulen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2479">General Availability of Az Module</span></span>
- <span data-ttu-id="27ffd-2480">Onlinehjälp för varje modul</span><span class="sxs-lookup"><span data-stu-id="27ffd-2480">Online help for each module</span></span>
- <span data-ttu-id="27ffd-2481">Mer information och en översikt finns på [Az-informationssidan](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2481">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="27ffd-2482">Information om hur du migrerar från AzureRM finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2482">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="27ffd-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2483">Az.Accounts</span></span>
- <span data-ttu-id="27ffd-2484">Har ändrats från Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27ffd-2484">Changed from Az.Profile</span></span>
- <span data-ttu-id="27ffd-2485">Fasta tabellformat för profil- och kontexttyper</span><span class="sxs-lookup"><span data-stu-id="27ffd-2485">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="27ffd-2486">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-2486">Az.ApiManagement</span></span>
- <span data-ttu-id="27ffd-2487">Korrigeringar för #7002</span><span class="sxs-lookup"><span data-stu-id="27ffd-2487">Fixes for #7002</span></span>
- <span data-ttu-id="27ffd-2488">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2488">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="27ffd-2489">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27ffd-2489">Az.Batch</span></span>
- <span data-ttu-id="27ffd-2490">Lade till möjligheten att se vilken version av Azure Batch Node Agent som körs på var och en av de virtuella datorerna i en pool, via den nya egenskapen `NodeAgentInformation` på `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2490">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="27ffd-2491">Standarden `Caching` för `PSDataDisk` är nu `ReadWrite` i stället för `None`.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2491">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="27ffd-2492">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2492">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="27ffd-2493">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="27ffd-2493">Az.Billing</span></span>
- <span data-ttu-id="27ffd-2494">Kombinerar cmdletarna för fakturering, förbrukning och UsageAggregates. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2494">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="27ffd-2495">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2495">Az.CognitivServices</span></span>
- <span data-ttu-id="27ffd-2496">Lade till kompletterare för SkuName och Typem som är tillgängliga i New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-2496">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="27ffd-2497">Tog bort parameteruppsättningen GetSkusWithAccountParamSetName från Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="27ffd-2497">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="27ffd-2498">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27ffd-2498">Az.ContainerInstance</span></span>
- <span data-ttu-id="27ffd-2499">Stöd för ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="27ffd-2499">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="27ffd-2500">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="27ffd-2500">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="27ffd-2501">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2501">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-2502">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-2502">Az.DataLakeStore</span></span>
- <span data-ttu-id="27ffd-2503">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="27ffd-2504">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27ffd-2504">Az.Monitor</span></span>
- <span data-ttu-id="27ffd-2505">Döpte om Az.Insights till Az.Monitor och andra mindre icke-bakåtkompatibla ändringar. Mer information finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2505">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="27ffd-2506">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27ffd-2506">Az.KeyVault</span></span>
- <span data-ttu-id="27ffd-2507">Tog bort den inaktuella egenskapen PurgeDisabled från utdatatyper</span><span class="sxs-lookup"><span data-stu-id="27ffd-2507">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="27ffd-2508">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="27ffd-2508">Az.MachineLearning</span></span>
- <span data-ttu-id="27ffd-2509">Inkluderade cmdletarna från modulen Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2509">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="27ffd-2510">Az.Media</span><span class="sxs-lookup"><span data-stu-id="27ffd-2510">Az.Media</span></span>
- <span data-ttu-id="27ffd-2511">Tog bort inaktuella -Tags-alias från New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="27ffd-2511">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="27ffd-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2512">Az.Network</span></span>
<span data-ttu-id="27ffd-2513">Stöd har lagts till för konfiguration av RewriteRuleSets i Application Gateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-2513">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="27ffd-2514">Nya cmdletar har lagts till:</span><span class="sxs-lookup"><span data-stu-id="27ffd-2514">New cmdlets added:</span></span>
        - <span data-ttu-id="27ffd-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27ffd-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27ffd-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27ffd-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27ffd-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27ffd-2520">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2520">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="27ffd-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="27ffd-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="27ffd-2523">Cmdletar har uppdaterats med den valfria parametern -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27ffd-2523">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="27ffd-2524">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27ffd-2524">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="27ffd-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="27ffd-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="27ffd-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="27ffd-2527">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-2527">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="27ffd-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="27ffd-2529">New-AzureRmApplicationGatewayUrlPathMapConfig har lagt till KeyVault-stöd för Application Gateway med Identity.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2529">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="27ffd-2530">Cmdletar har uppdaterats med den valfria parametern -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="27ffd-2530">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="27ffd-2531">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="27ffd-2531">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="27ffd-2532">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="27ffd-2532">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="27ffd-2533">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="27ffd-2533">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="27ffd-2534">Cmdleten New-AzApplicationGateway har uppdaterats med den valfria parametern -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="27ffd-2534">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="27ffd-2535">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="27ffd-2536">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-2536">Az.OperationalInsights</span></span>
- <span data-ttu-id="27ffd-2537">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="27ffd-2538">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27ffd-2538">Az.Profile</span></span>
- <span data-ttu-id="27ffd-2539">Modulnamnet har ändrats till Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2539">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-2540">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2540">Az.RecoveryServices</span></span>
- <span data-ttu-id="27ffd-2541">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2541">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="27ffd-2542">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2542">Az.Resources</span></span>
- <span data-ttu-id="27ffd-2543">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="27ffd-2544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-2544">Az.ServiceFabric</span></span>
- <span data-ttu-id="27ffd-2545">Stöd för specificering av certifikat efter eget namn och tumavtryck</span><span class="sxs-lookup"><span data-stu-id="27ffd-2545">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="27ffd-2546">Information om fler icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2546">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="27ffd-2547">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="27ffd-2547">Az.SIgnalR</span></span>
- <span data-ttu-id="27ffd-2548">Allmän tillgänglighet för PowerShell-cmdletar för SIgnalR</span><span class="sxs-lookup"><span data-stu-id="27ffd-2548">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="27ffd-2549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2549">Az.Sql</span></span>
- <span data-ttu-id="27ffd-2550">Lade till de nya identifieringstyperna Data_Exfiltration och Unsafe_Action i Threat Detection-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2550">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="27ffd-2551">Uppdaterade dokumentationsexempel för Sql Auditing-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2551">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="27ffd-2552">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="27ffd-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2553">Az.Storage</span></span>
- <span data-ttu-id="27ffd-2554">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="27ffd-2555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-2555">Az.Websites</span></span>
- <span data-ttu-id="27ffd-2556">Mer information om mindre icke-bakåtkompatibla ändringar finns i [Migreringsguiden](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="27ffd-2557">0.7.0 – december 2018</span><span class="sxs-lookup"><span data-stu-id="27ffd-2557">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="27ffd-2558">Allmänt</span><span class="sxs-lookup"><span data-stu-id="27ffd-2558">General</span></span>

* <span data-ttu-id="27ffd-2559">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="27ffd-2559">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="27ffd-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2560">Az.Compute</span></span>

* <span data-ttu-id="27ffd-2561">Lade till stöd för UltraSSD och Galleriavbildningar i de enkla parameteruppsättningarna för `New-AzVm(ss)`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2561">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-2562">Az.DataLakeStore</span></span>

* <span data-ttu-id="27ffd-2563">Åtgärdade avslutande snedstreck i domänen för adls-konto</span><span class="sxs-lookup"><span data-stu-id="27ffd-2563">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="27ffd-2564">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27ffd-2564">Az.FrontDoor</span></span>

* <span data-ttu-id="27ffd-2565">Brutna länkar korrigerades</span><span class="sxs-lookup"><span data-stu-id="27ffd-2565">Fixed some broken links</span></span>
    - <span data-ttu-id="27ffd-2566">I artiklarna New-AzureRmFrontDoor och Set-AzureRmFrontDoor artiklar korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2566">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="27ffd-2567">I artikeln New-AzureRmFrontDoorManagedRuleObject korrigerades länken till artikeln om cmdleten New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2567">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="27ffd-2568">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2568">Az.RecoveryServices</span></span>

* <span data-ttu-id="27ffd-2569">Lade till valideringar på klientsidan för Azure-filresurs med återställningsåtgärder.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2569">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="27ffd-2570">Gjorde storageAccountName och storageAccountResourceGroupName valfritt för afs-återställning.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2570">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="27ffd-2571">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2571">Az.Resources</span></span>

* <span data-ttu-id="27ffd-2572">Korrigering för https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="27ffd-2572">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="27ffd-2573">Uppdaterade Get-AzureRmRoleAssignment så att prenumerationsomfattningen används om den anges vid begäran om klassiska administratörer.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2573">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="27ffd-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2574">Az.Sql</span></span>

* <span data-ttu-id="27ffd-2575">Mindre ändringar för kommande övergång från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="27ffd-2575">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="27ffd-2576">Korrigerade ett problem med Get-AzureRmSqlDatabaseVulnerabilityAssessment med DotNet-kärna</span><span class="sxs-lookup"><span data-stu-id="27ffd-2576">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="27ffd-2577">Ändrade dokumentationen för hjälpmeddelanden som rör SQL Auditing-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2577">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="27ffd-2578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2578">Az.Storage</span></span>

* <span data-ttu-id="27ffd-2579">Lade till -EnableHierarchicalNamespace i New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-2579">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="27ffd-2580">Åtgärdade problemet med att cmdleten Copy File inte kunde återanvända källkontexten på målet om inte -DestContext angetts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2580">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="27ffd-2581">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="27ffd-2581">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="27ffd-2582">Stöd för statisk webbplatskonfiguration</span><span class="sxs-lookup"><span data-stu-id="27ffd-2582">Support Static Website configuration</span></span>
    - <span data-ttu-id="27ffd-2583">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="27ffd-2583">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="27ffd-2584">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="27ffd-2584">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="27ffd-2585">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-2585">Az.Websites</span></span>

* <span data-ttu-id="27ffd-2586">Set-AzureRmWebApp och Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="27ffd-2586">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="27ffd-2587">Ny parameter (-AzureStoragePath) har lagts till för att ange att Azure Storage-sökvägar ska monteras i containerappar i Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2587">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="27ffd-2588">Använder utdata från den nya cmdleten New-AzureRmWebAppAzureStoragePath som en parameter för att ange sökvägar för Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2588">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="27ffd-2589">0.6.1 – november 2018</span><span class="sxs-lookup"><span data-stu-id="27ffd-2589">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="27ffd-2590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27ffd-2590">Az.ApiManagement</span></span>
* <span data-ttu-id="27ffd-2591">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="27ffd-2591">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="27ffd-2592">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27ffd-2592">Az.Automation</span></span>
* <span data-ttu-id="27ffd-2593">Swagger baserade Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2593">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="27ffd-2594">Cmdletar för Uppdateringshantering har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2594">Added Update Management cmdlets</span></span>
* <span data-ttu-id="27ffd-2595">Cmdletar för källkontroll har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2595">Added Source Control cmdlets</span></span>
* <span data-ttu-id="27ffd-2596">Remove-AzureRmAutomationHybridWorkerGroup-cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2596">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="27ffd-2597">Kommandot för DSC-registreringsnod har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2597">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="27ffd-2598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2598">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2599">Problem med SystemAssigned-identitet har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2599">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="27ffd-2600">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="27ffd-2600">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="27ffd-2601">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27ffd-2601">Az.ContainerInstance</span></span>
* <span data-ttu-id="27ffd-2602">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="27ffd-2602">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="27ffd-2603">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="27ffd-2603">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="27ffd-2604">uppdatera exempelbeskrivningen för marketplace-cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2604">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="27ffd-2605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2605">Az.Network</span></span>
* <span data-ttu-id="27ffd-2606">Cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomErreller Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2606">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="27ffd-2607">ICMP tillbaka till stöd för Azure Firewall-nätverksprotokoll har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2607">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="27ffd-2608">Uppdatera cmdlet Test-AzureRmNetworkWatcherConnectivity, lägga till verifiering av mål-id, adress och port.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2608">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="27ffd-2609">Åtgärda problem med minnesanvändning i VirtualNetwork-karta</span><span class="sxs-lookup"><span data-stu-id="27ffd-2609">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="27ffd-2610">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="27ffd-2610">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="27ffd-2611">Åtgärda för att ändra principen för en skyddad fildelning.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2611">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="27ffd-2612">Tidszonsprincipen har konverterats till versaler.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2612">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="27ffd-2613">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="27ffd-2613">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="27ffd-2614">Exempel i New-AzureRmRecoveryServicesAsrProtectableItem har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2614">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="27ffd-2615">Uppdatera beroenden för problemet med typmappning</span><span class="sxs-lookup"><span data-stu-id="27ffd-2615">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="27ffd-2616">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="27ffd-2616">Az.Relay</span></span>
* <span data-ttu-id="27ffd-2617">Valfri parameter -KeyValue till New-AzureRmRelayKey cmdlet har lagts till, vilket gör det möjligt för användare att tillhandahålla KeyValue.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2617">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="27ffd-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2618">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2619">Uppdatera hjälpdokumentation för resursidentitet kopplad till parametrar i `New-AzureRmPolicyAssignment` och `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="27ffd-2619">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="27ffd-2620">Lägg till ett exempel för New-AzureRmPolicyDefinition som använder -Metadata</span><span class="sxs-lookup"><span data-stu-id="27ffd-2620">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="27ffd-2621">Korrigera så att skiftläge behålls i taggnycklar i NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="27ffd-2621">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="27ffd-2622">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-2622">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-2623">Lägg till utfasningsmeddelanden för kommande icke-kompatibla ändringar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2623">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="27ffd-2624">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2624">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2625">Nya cmdletar för CRUD-åtgärder på Azure Sql Database-hanterad instans och Azure Sql-hanterad databas</span><span class="sxs-lookup"><span data-stu-id="27ffd-2625">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="27ffd-2626">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27ffd-2626">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27ffd-2627">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27ffd-2627">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27ffd-2628">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27ffd-2628">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27ffd-2629">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27ffd-2629">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27ffd-2630">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="27ffd-2630">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="27ffd-2631">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="27ffd-2631">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="27ffd-2632">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="27ffd-2632">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="27ffd-2633">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="27ffd-2633">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="27ffd-2634">Hantering av utökad granskningsprincip på en server eller en databas har aktiverats.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2634">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="27ffd-2635">Ny parameter (PredicateExpression) har lagts till för att aktivera filtrering av granskningsloggar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2635">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="27ffd-2636">Cmdletar har ändrats så att de använder SQL-klienter i stället för äldre klienter.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2636">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="27ffd-2637">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2637">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="27ffd-2638">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2638">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="27ffd-2639">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2639">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="27ffd-2640">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2640">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="27ffd-2641">Problem med att använda Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings med lagringskontots namnparameter har korrigerats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2641">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="27ffd-2642">0.5.0 – november 2018</span><span class="sxs-lookup"><span data-stu-id="27ffd-2642">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="27ffd-2643">Allmänt</span><span class="sxs-lookup"><span data-stu-id="27ffd-2643">General</span></span>
* <span data-ttu-id="27ffd-2644">Lade till resurskompletterare till många kärn-cmdletar – dessa gör att du kan stega genom befintliga resursnamn med TABB vid interaktiva anrop till cmdletar</span><span class="sxs-lookup"><span data-stu-id="27ffd-2644">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="27ffd-2645">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27ffd-2645">Az.Profile</span></span>
* <span data-ttu-id="27ffd-2646">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="27ffd-2646">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="27ffd-2647">Bytte namn på parametern TenantId i cmdleten Connect-AzAccount till Tenant och lade till ett alias för TenantId</span><span class="sxs-lookup"><span data-stu-id="27ffd-2647">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="27ffd-2648">Uppdaterade TenantId-beskrivningen för Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="27ffd-2648">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="27ffd-2649">Åtgärda felmeddelande för misslyckad inloggning när du tillhandahåller klientdomän</span><span class="sxs-lookup"><span data-stu-id="27ffd-2649">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="27ffd-2650">Åtgärda problem med att kontextnamn hamnar i konflikt för konton utan prenumerationer i klientorganisationen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2650">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="27ffd-2651">Åtgärda problem med DataLake-slutpunkter vid användning av MSI</span><span class="sxs-lookup"><span data-stu-id="27ffd-2651">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="27ffd-2652">Åtgärdade problem med att Disconnect-AzAccount kastades om den inte anslöts</span><span class="sxs-lookup"><span data-stu-id="27ffd-2652">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-2653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2653">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-2654">Lade till åtgärden Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2654">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2655">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2656">Lade till cmdletarna Add-AzVmssVMDataDisk och Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="27ffd-2656">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="27ffd-2657">Get-AzVMImage visar AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="27ffd-2657">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="27ffd-2658">Åtgärdade att värdena för alternativen SetAzVMChefExtension -BootstrapOptions och -JsonAttribute inte angavs i json-format.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2658">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-2659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-2659">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-2660">Uppdatera DataLake-paketet till 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2660">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="27ffd-2661">Lägg till standardsamtidighet för flertrådade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2661">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="27ffd-2662">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="27ffd-2662">Az.Insights</span></span>
* <span data-ttu-id="27ffd-2663">Åtgärdade problem #7267 (autoskalningsområde)</span><span class="sxs-lookup"><span data-stu-id="27ffd-2663">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="27ffd-2664">Problem med att uppräknade parametrar inte ställdes in ordentligt när du skapade en ny autoskalningsregel (de ställdes alltid in med standardvärdet).</span><span class="sxs-lookup"><span data-stu-id="27ffd-2664">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="27ffd-2665">Åtgärdade problem #7513 [Insights] Set-AzDiagnosticSetting kräver uttrycklig specifikation av kategorier när inställningar skapas</span><span class="sxs-lookup"><span data-stu-id="27ffd-2665">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="27ffd-2666">Nu kräver inte cmdleten uttrycklig anvisning av kategorierna för att aktiveras under skapande, d.v.s. den fungerar enligt beskrivning</span><span class="sxs-lookup"><span data-stu-id="27ffd-2666">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-2667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2667">Az.Network</span></span>
* <span data-ttu-id="27ffd-2668">PeeringType ändrades till en obligatorisk parameter för följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="27ffd-2668">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="27ffd-2669">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="27ffd-2669">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="27ffd-2670">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="27ffd-2670">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="27ffd-2671">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="27ffd-2671">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="27ffd-2672">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="27ffd-2672">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="27ffd-2673">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="27ffd-2673">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="27ffd-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="27ffd-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27ffd-2675">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27ffd-2675">Az.PolicyInsights</span></span>
* <span data-ttu-id="27ffd-2676">Cmdletar för principreparation har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2676">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2677">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2678">Korrigering för https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="27ffd-2678">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="27ffd-2679">Tillåt att resurser listas med parametern -ResourceId för Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="27ffd-2679">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27ffd-2680">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27ffd-2680">Az.ServiceBus</span></span>
* <span data-ttu-id="27ffd-2681">Skrivskyddad MigrationState-egenskap har lagts till i PSServiceBusMigrationConfigurationAttributes, som hjälper till att hålla koll på migreringstillståndet.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2681">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27ffd-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27ffd-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="27ffd-2683">Åtgärda att lägga till certifikat till Linux-Vmss.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2683">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="27ffd-2684">Åtgärdade Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="27ffd-2684">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="27ffd-2685">Använd rätt tumavtryck från nya certifikat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="27ffd-2685">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="27ffd-2686">Visa undantag korrekt (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="27ffd-2686">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="27ffd-2687">Åtgärdade Update-AzServiceFabricDurability så att klusterkonfigurationen uppdateras innan Vmss-åtgärden CreateOrUpdate påbörjas.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2687">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="27ffd-2688">0.4.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="27ffd-2688">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="27ffd-2689">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27ffd-2689">Az.Profile</span></span>
* <span data-ttu-id="27ffd-2690">Åtgärdade problemet med Get-AzSubscription i CloudShell</span><span class="sxs-lookup"><span data-stu-id="27ffd-2690">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="27ffd-2691">Uppdatera gemensam kod så att den använder den senaste versionen av ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="27ffd-2691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2692">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2692">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2693">Nya storlekar lades till i listan över godkända VM-storlekar för vilka accelererat nätverk kommer att aktiveras vid användning av den enkla parameteruppsättningen för New-AzVm</span><span class="sxs-lookup"><span data-stu-id="27ffd-2693">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="27ffd-2694">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2694">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27ffd-2695">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27ffd-2695">Az.DataLakeStore</span></span>
* <span data-ttu-id="27ffd-2696">Lägger till stöd för regler för virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="27ffd-2696">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="27ffd-2697">Get-AzDataLakeStoreVirtualNetworkRule: Hämtar eller listar regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2697">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="27ffd-2698">Add-AzDataLakeStoreVirtualNetworkRule: Lägger till en regel för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2698">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="27ffd-2699">Set-AzDataLakeStoreVirtualNetworkRule: Ändrar den angivna regeln för virtuellt nätverk i det angivna Data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2699">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="27ffd-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Tar bort en regel för virtuellt nätverk i Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-2701">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2701">Az.Network</span></span>
* <span data-ttu-id="27ffd-2702">Skicka protokollvärdet till serverdelen för att uppdatera cmdleten Test-AzNetworkWatcherConnectivity.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2702">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="27ffd-2703">Argumentslutförare för ResourceName har lagts till i alla cmdletar.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2703">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2704">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2705">Åtgärdade problem där Get-AzRoleDefinition genererar ett oläsligt undantag (när standardprofilen inte innehåller någon prenumeration och ingen omfattning har angetts) genom att lägga till ett beskrivande undantag i scenariot.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2705">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="27ffd-2706">Ställ in ”RoleDefinitionNameParameterSet” som standardparameteruppsättning.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2706">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="27ffd-2707">0.3.0 – oktober 2018</span><span class="sxs-lookup"><span data-stu-id="27ffd-2707">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="27ffd-2708">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2708">Azure.Storage</span></span>
* <span data-ttu-id="27ffd-2709">Åtgärda fel där Kopiera blob/fil inte kopierar metadata när målplatsen har ett problem med metadata</span><span class="sxs-lookup"><span data-stu-id="27ffd-2709">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="27ffd-2710">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27ffd-2710">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="27ffd-2711">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="27ffd-2711">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="27ffd-2712">Stöd för att hämta användningsinformation om en Storage-resurs för en specifik plats och för att lägga till ett varningsmeddelande för att hämta användningsinformation om en global Storage-resurs är inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2712">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="27ffd-2713">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="27ffd-2713">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27ffd-2714">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27ffd-2714">Az.CognitiveServices</span></span>
* <span data-ttu-id="27ffd-2715">Stöd för Get-AzCognitiveServicesAccountSkus utan ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2715">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27ffd-2716">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27ffd-2716">Az.Compute</span></span>
* <span data-ttu-id="27ffd-2717">Åtgärdade fel där Get-AzVM -ResourceGroupName <rg> returnerar fler än 50 resultat om det behövs</span><span class="sxs-lookup"><span data-stu-id="27ffd-2717">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="27ffd-2718">Lade till ett exempel för SimpleParameterSet i hjälpen för cmdleten New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2718">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="27ffd-2719">Ett stavfel i förloppsmeddelandet för Azure Disk Encryption har korrigerats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2719">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="27ffd-2720">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="27ffd-2720">Az.DataFactoryV2</span></span>
* <span data-ttu-id="27ffd-2721">ADF .Net SDK-versionen har uppdaterats till 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2721">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27ffd-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27ffd-2722">Az.Network</span></span>
* <span data-ttu-id="27ffd-2723">Funktionalitet för NetworkProfile har lagts till.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2723">Added NetworkProfile functionality.</span></span> <span data-ttu-id="27ffd-2724">nya cmdletar har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2724">new cmdlets added</span></span>
    - <span data-ttu-id="27ffd-2725">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27ffd-2725">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="27ffd-2726">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27ffd-2726">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="27ffd-2727">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27ffd-2727">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="27ffd-2728">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27ffd-2728">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="27ffd-2729">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-2729">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="27ffd-2730">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="27ffd-2730">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="27ffd-2731">Länk för tjänstassociering på modell för undernät har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2731">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="27ffd-2732">Cmdletarna New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap och Remove-AzVirtualNetworkTap har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2732">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="27ffd-2733">Cmdletarna Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig och Remove-AzNEtworkInterfaceTapConfig har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2733">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27ffd-2734">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27ffd-2734">Az.RedisCache</span></span>
* <span data-ttu-id="27ffd-2735">Tillåt att alla strängar används som storleksparametrar framöver.</span><span class="sxs-lookup"><span data-stu-id="27ffd-2735">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="27ffd-2736">Lägg till P5 i popup-fönstret PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="27ffd-2736">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="27ffd-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27ffd-2737">Az.Resources</span></span>
* <span data-ttu-id="27ffd-2738">Parametern -Mode som saknades i Set-AzPolicyDefinition har lagts till</span><span class="sxs-lookup"><span data-stu-id="27ffd-2738">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="27ffd-2739">Åtgärdade buggen för cmdleten Get-AzProviderOperation för åtgärder med ursprung som innehåller användare</span><span class="sxs-lookup"><span data-stu-id="27ffd-2739">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="27ffd-2740">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27ffd-2740">Az.Sql</span></span>
* <span data-ttu-id="27ffd-2741">Ett problem där vissa cmdletar för säkerhetskopiering inte kunde identifiera den aktuella azure-prenumerationen har åtgärdats</span><span class="sxs-lookup"><span data-stu-id="27ffd-2741">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27ffd-2742">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27ffd-2742">Az.Websites</span></span>
* <span data-ttu-id="27ffd-2743">Ny cmdlet: Get-AzWebAppContainerContinuousDeploymentUrl – Hämtar webhook-URL:en för kontinuerlig distribution av container</span><span class="sxs-lookup"><span data-stu-id="27ffd-2743">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="27ffd-2744">Nya cmdletar: New-AzWebAppContainerPSSession och Enter-WebAppContainerPSSession – Startar en PowerShell-fjärrsession i en containerapp för windows</span><span class="sxs-lookup"><span data-stu-id="27ffd-2744">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="27ffd-2745">0.2.0 – september 2018</span><span class="sxs-lookup"><span data-stu-id="27ffd-2745">0.2.0 - September 2018</span></span>
 <span data-ttu-id="27ffd-2746">Första versionen</span><span class="sxs-lookup"><span data-stu-id="27ffd-2746">Initial Release</span></span>
